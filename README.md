# pure_data_stuff
This is where I put my Pure Data patches. Use 'em if you want 'em

piano phase - outputs midi arpeggios at slightly different metros,
replicating a section of steve reich's piano phase. i use loopbe1
to route midi from pd to ableton all the time. it's fun!

ev-xs_map - this is a map of my Evolution X-Session MIDI controller.
This could be useful for anyone who has one of these things wants
sixteen knobs, a slider that I haven't gotten to work as a crossfader
yet, and ten buttons for sample triggering. (Pd recognizes the
controller as two different controllers if you have a keyboard plugged
into the MIDI IN, so set it up accordingly in your MIDI settings

am sweep with midi control - messing around with amplitude modulation.
phasor~ modulates osc~. i really need to add adsr to this...
