use_synth :piano
use_bpm 100


live_loop :calcifer do
  1.times do
    play :d4
    sleep 1
    play :g4
    sleep 1
    play :bb4
    sleep 1
  end
  stop
end

live_loop :my_cymbal  do
  sleep 3
  9.times do
    sample :drum_cymbal_closed
    sleep 1
  end
  stop
end

define :howlsmovingcastle do
  sleep 3
  play :d4
  play :bb4
  play :g4
  play :eb4
  sleep 2
  play :d4
  sleep 1
  
  play :c4
  sleep 1
  play :bb4
  sleep 1
  play :a4
  sleep 1
  play :d4
  play :g4
  play :bb4
  sleep 3
  
  play :g4
  sleep 0.5
  play :b4
  sleep 0.5
  play :d5
  sleep 0.5
  play :g4
  play :b4
  play :d5
  play :g5
  sleep 3
  play :g5
  sleep 1
  
  play :g5
  sleep 1
  play :f5
  sleep 1
  play :e5
  sleep 1
  play :f5
  play :d5
  play :a4
end

with_fx :compressor do
  howlsmovingcastle
end
