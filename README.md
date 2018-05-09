# pure_data_stuff
This is where I put my Pure Data patches. Use 'em if you want 'em

piano phase - outputs midi arpeggios at slightly different metros,
replicating a section of steve reich's piano phase. i use loopbe1
to route midi from pd to ableton all the time. it's fun!

ev-xs_map - this is a map of my Evolution X-Session MIDI controller.
This could be useful for anyone who has one of these things and wants
sixteen knobs, a slider that I haven't gotten to work as a crossfader
yet, and ten buttons for sample triggering. (Pd recognizes the
controller as two different controllers if you have a keyboard plugged
into the MIDI IN, so set it up accordingly in your MIDI settings

am sweep with midi control - messing around with amplitude modulation.
phasor~ modulates osc~. i really need to add adsr to this...

markov am synth - this really is just the second stage of an experiment
where it was 3:00 am on a weeknight, and i had to be at work in six
hours, and i was wide awake, staring at a simple osc~ noisemaker and
i thought "hmm, what would happen i plug the output of a phasor~ into
this inlet and HOLY SHIT THAT'S INCREDIBLE!!! and the next day looking
at a random thing about pd and realizing that what i did was am
synthesis! cool! fast forward to a couple of nights ago, and there i was
again, following along with this tutorial on algorithmic composition
using a markov chain:

http://www.algorithmiccomposer.com/2010/05/algorithmic-composition-tutorial-markov.html

and here i am tonight, thinking "hmm, what would happen if i put this
am synth at the end of this... well, damn!" so this is the beginning of
an insane project where more will be added, I'm sure... oh yeah, you'll
need to install zexy and cyclone (i think) for this to work,.

effects wrapper with signal bypass - useful for modular abstractions, and
especially useful for guitarists. based on the main patch abstraction
from the guitar extended blog

dataplayer - this uses the soundfiler object to open _any_ file and play it
as sound. sometimes this sounds awesome. sometimes not. your mileage may vary.

greenwood - yep. it's exactly what you think it is.
