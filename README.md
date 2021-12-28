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

ontherun - i threw this together rather haphazardly to demo my raspberry
pi-based pure data box. two wavetable oscillators (sine/square/saw/tri/random
voices) and a vcf~ playing the 8-note sequence from pink floyd's "on the run"
at 90 ms/note, or 666 bpm. spooooky!

aphex twin logo in comments - i'm saving this just in case i do something in pd
that sounds really awesome and my sidekick keeps saying "APHEX TWIN ALREADY DID
IT!"

drunk filtersweeps - a simple example of sending the output of a random walk up and
down the number line to MIDI CC using ctlout. in this example i have two drunk objects
sending data to CC numbers 3 and 9, which i had mapped to an ableton auto filter
effect.

31 C chords - a compositional/educational tool for people like me who can't play
keyboards worth a shit and want to know what a C6/9 or Cm7b5 chord sounds like. MIDI
notes are packed in an organized display of messages, each with its own bang for
previewing. all the heavy lifting is done in subpatches; controls for note velocity,
note duration, and key transposition are in the main patch. (note: this only outputs
MIDI, not audio. you'll need some way to send MIDI from your PC to a synth or a DAW.
on windows i use loopbe1 -> ableton.)

masterclock - this is a cleaned-up version of an abstraction i've been using in some
algorithmic MIDI projects i've been working on. it's a fairly straightforward clock
divider-based "multi-channel metro" that outputs bangs on whole, half, quarter, eighth,
and sixteenth notes (the expr object actually runs on thirtysecond notes, but that
was too fast for what i was using it for - just run another patch cable from the counter
output without a select for 32nds). lately i've been using pd to control a small eurorack
setup, so i added a MIDI beat clock to this.

up-down counter - a simple float counter that starts at 0, and counts backwards to 0 once
it reaches an upper limit. useful for parameter sweeps in DAWs. i use a couple of these at
different metro speeds to sweep a filter module in my eurorack.

drum grid - this is a 16-step MIDI drum sequencer. in its current state it's designed to
work with an ableton drum rack set on MIDI channel 1, and triggers kick, snare, closed hat
and open hat. i wasn't sure how to go about doing something like this at first, so i
peeked inside automatonism's trigger sequencer module, said "so that's how this works!"
and went from there. lots of spigots are involved. adjustable bpm with built-in MIDI
clock for syncing with a DAW. user can randomize and clear each or all of the grid rows
with the click of a bang object. eight presets are included. i dunno; i think this is
an easier method of drum rack programming. i hate the ableton piano roll. (this patch
uses a "counter" object, so you'll need the cyclone library for it to work.)

drum grid dsp - same idea, but with synthesized drum sounds and the ability to record
a single 16-step sequence to an audio file that can be imported into a DAW or sampler.
