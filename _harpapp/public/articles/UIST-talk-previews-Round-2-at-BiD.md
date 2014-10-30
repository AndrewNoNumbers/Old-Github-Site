UIST talk previews Round 2 at BiD
==================================

Feedback: goo.gl/GwQQ4m


###Talk 1: Jonathan Harper (advisor Maneesh Agrawal)
*Deconstructing and Restyling d3 Visualizations*

exposing the data from the visualization

Savva uses computer vision and heuristics to extract data from bitmap bar charts, pies etc.

provide a GUI for restyling the data so end-users can use it

since it's d3, we're using SVGs, meaning we can take stuff from that
the data in a d3 visualization is actually stored alongside the SVG nodes, thus we can traverse the nodes and collect all the data

Feedback:
How prevalent is D3? Give some statistics.
you talk about several reasons for getting at the data - each of these reasons needs its own slide to illustrate the point

have to explain earlier on how D3 works in the beginning - this SVG tree came out of nowhere
7: It sounds like you are relying on data binding and tree ordering to get useful data - but I didn’t understand whether these *always* work, or if they *sometimes* work if developers happen to stick to certain conventions.

have to explain earlier on how D3 works in the beginning - this SVG tree came out of nowhere
7: It sounds like you are relying on data binding and tree ordering to get useful data - but I didn’t understand whether these *always* work, or if they *sometimes* work if developers happen to stick to certain conventions.

less of just a demo, more of why it matters and how it differentiates 
much too much mechanics and details (it's pretty obvious); need a bigger picture at the beginning - what makes this problem challenging and worthwhile to solve

When you are done say “Thank you,” it cues people to clap.

Bjoern
Kristin ksteph@cs.berkeley.edu

###Talk 2: Joanne Lo (advisor Eric Paulos)
3rd year Ph.D.
*ShrinkyCircuits: Sketching, shrinking, and formgiving of electric circuits*

after sketching stage, you generally have to put it into a PCB program (like Eagle), then have it printed somewhere, then you put it in a housing

Prestressed polystyrene (this is actually what ShrinkyDinks are)
shrinks at heat, goes from flexible cardstock-like form to a thicker piece

draw your circuit with a  conductive pen
conductive ink actually becomes more conductive as side effect of heating process 11.84Ω to 1.4Ω

Circuit boards as final design form (can be assembled into 3D shapes, used as crafts etc.)


Feedback: 

add slide numbers - especially for practice talks so people can refer to it, give feedback on it

The conductivity improvement is AWESOME. But you could have covered this in 30 seconds.

Should know the shrinking factor, and the tolerance on that, or else we don't know if a component we want to put on later will actually fit 


Motivation/background
Our process
Results
Limitations


###Talk 3: Steve Rubin (advisor Maneesh Agrawal)

Why does music work so well with auditory stories?
music activates reward, emotion, pain etc.

how do we create a musical score for the story?
we often have to rearrange and cut a musical score to have the emotion match the parts of the story

first step is emotional labeling of the musical score
In psychology: valence-arousal graph (so nervous-calm on y-axis and sad-happy on x-axis)

How do we do this?
Hand-labeling
crowd-labeling
automatic-labeling (trained with a Turk data set)

we've talked to producers about their scoring techniques, and saw what limitations we had here
added some constraints (such as avoid looping, add pauses, constrain duration of music) etc. to make it sound more natural

kept musical score consistently 12dB below oral track

Got feedback on quality of different labeling techniques vs no music

Perhaps four color feedback is too coarse
Perhaps need a smooth spectrum within a story

Show how it might apply in real use, like a children's story and or podcast
How automated is all the steps, how can a user maybe approach it

How does it compare to professionally-scored audio story

