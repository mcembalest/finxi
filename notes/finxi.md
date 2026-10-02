# finxi

a craftsperson's apprentice in an unbounded workshop

The workshop/fingere word choice is meant to emphasize CREATION over PREDICTION

what i have not created i do not understand

introduce FINXI as my AIXI and to introduce the concept (e.g. maybe as a section at the end of the paper) of the Workshop of Icaria, to convey the image of the FINXI model as the craftsperson's apprentice in an unbounded workshop with the craftsperson having a nice silent backstory like a remorseful atoneful Daedalus and with the tools corresponding to the exact primitives we want to give our models to use at start.

three sections in this paper. FINXI, GEN, and ICARIA. all three sections go at the same idea, but the first goes at it as pure theory and names it FINXI like AIXI, the second goes at it as practical implementation and names it GEN like GAN, the third goes at it as allegorical story and names it ICARIA like ICARUS.

## FINXI

aixi is a claim to a universal predictor.

they call AIXI the universally intelligent agent

FINXI, its just a creative agent

FINXI is the theory of a creative agent the way that AIXI is the theory of a predictive agent

FINXI is what a single model/agent says when they honestly report that they have created something

not god vibes.

dont use apprentice in section 1 finxi, section 1 finxi should really approach the theory of creativity and intelligence like hutter approached aixi.

### propositions

FINXI needs propositions

```












```

### creation

Maybe creation is simply what we can talk about here. Taking primitives, creating/making something. construction is a bit formal, the same way 'formulation' might have been too formal relative to hutter's more familiar choice of intelligence

construction can be entirely for its own sake, think about the history of math and science.

I am not sure that generating byte sequences is any different from predicting the next sequence element. I think I would prefer if the creations were actual usable tools or artifacts or maybe simply just interesting objects and mathematical constructions, but I admit this is still extremely imprecise. That being said, byte sequences are super general and form a basic substrate that programs compile into.

i think construction isnt quite the same concept as generation, i think construction is much more system 2 compared to the relative system 1ness of generation.

I dont want to restrict the apprentice to making circuits, i think they should be free to make anything

### comprehension

in the charles darwinian and erasmus darwinian sense, in the kantian and jungian sense, and in the david chalmersian sense, we have plenty of evidence that creation for fun's sake on its own can exist organically as the way a living thing intervenes on objective experience to bring about surprise and delight as subjective experience.

jurgen schmidhuber and karl friston are points of comparison, not support: schmidhuber formalizes fun as compression progress, and friston's free energy principle has living things act to minimize surprise.

for POWERPLAY I am not a compression maximalist personally, so that may exactly be the thing we dont borrow, and it may be because i make some argument about comprehension over compression, but TBD on that.

i think in a pythagorean sense, in a martin buber sense, in a Logos sense, it is inherently about comprehension of existence, not compression. i really believe in comprehension's supremacy, not compression's. this means we must view the comprehension of existence, beauty, meaning, etc as its own reward.

I have never been convinced by the prevailing conventional wisdom that compression is all one needs, and that intelligence is just compression. Maybe intelligence is compression, but then my thinking brings me to the notion of what lies beyond intelligence/compression. I believe the word that best characterizes it is comprehension. What is funny to me personally is that this is a slightly uncompressed version of the word 'compression' from a certain POV, if you replace the first s with hen. Therefore my personal joky of a shorthand for the question is S=HEN? So if 'S=HEN' then this just means compression is the literally only way to comprehend. But if 'S=/=HEN' then that means comprehension is a more general phenomenon than compression.

I want to build off the self-play, schmidhuber, etc lineage of research, but I myself just am not a compression maximalist, I believe that comprehension is the better target and the better mystery.

construction is not the same as comprehension/understanding/getting it! as an educator i like to approach this in a very simple way, construction is playful and it is an action and an environment that fosters and nurtures the senses of composition, function, behavior, error, regularity, symmetry, and more!! Pure understanding is quite naturally an emergent phenomenon on top of all that constructive activity.

comprehension is getting it, you get it or you dont, and assessing comprehension is likely the central problem in education, and all the best teachers know the problems in using scalars here. Doing new things is a better bit of evidence of comprehension

### the past tense

It plays upon a basic suspicion people all over the world have semicorrectly had about AI the whole time - how did it do that? did it just look up the answer somewhere? Both yes and no. If it is has already constructed the sequence, or sequences like it during pretraining, it doesnt have to build from scratch, it is mostly leveraging stuff its built already

## GEN

gen should really be the meat of the paper, with simple clear empirical work, not theory.

my goal is to make the headline image from the voyager paper on the timeline of minecraft creations but for universal mathematical structure, really to make that a paper focus, and to study whether it is the case that the GEN family of networks is well-shaped to implement the theory of FINXI and to actually generate universal mathematical structure which is downstream practical in real world use cases!

we dont need to start with truly zero data. The point of that paper is just that scaling pretraining data isnt necessarily the thing needed to scale.

GEN (Generative Educational Network)

GEN refers to any general educational network, though we will implement a GAN style / Cowsik paper style GEN.

neither FINXI or GEN requires a pair. GEN can in theory involve any number of learner agents in a system, and they can all be both teachers and learners

for now we should follow the self-play pretraining from zero data paper pretty much for pretraining. the cowsik paper has a goal of showing a more general approach to pretraining, so we should think about whether we can better focus OUR PARTICULAR GOAL since it is NOT the exact same as theirs, though we take inspiration.

the baselines we should implement for ourself to study as a baseline running here on the laptop, just POET? Also POWERPLAY?

similar to a GAN, except instead of a discriminator learning to tell apart real vs fake generations from an adversarial generator, a learner just predicts the byte sequences taught by an educational generator

my gen definition was based on the self play paper itself, not FINXI! maybe GEN is more general than prediction and creation, but anything taught.

GEN is 1) generator/generative, 2) general, 3) (maybe someday) genetic (e.g. GEPA genetic pareto)

the reason i consider GEN more general than GAN is 1) wordplay GEN is GENeral 2) many adversarial coaches think they are being educational and often...they can be correct, and some great teachers can switch on adversariality occasionally quite effectively

apprentice for learner, and craftsman for teacher

there is just the GEN in our implementation, which will consist of two connected networks, the teacher and the learner.

recognition will just be up to them, and they can build tools to enable further recognition

we the people on the outside will just be able to search their log and creations ourself

we shouldnt overclaim what we will do yet. plan for the minimum GEN to be teacher learner, then get to a good state with a two person GEN, then at that point we extend to multiple agents as learners, or even experiment with M teachers N learners, then maybe we broaden the nature of the teacher/student or craftsman/apprentice binary.

GEN extends to N learners, and having a teacher (remember magician) aka craftsman in charge is what we speculate is better than just swarm or simply some kind of work overseer.

both the teacher and the learner in the GEN need to be able to say finxi honestly, that they have both created, ideally independently with a useful story usually being the teacher making something and then the learner being shown the thing and trying to make it themself and the teacher being a world class master, apprentice, tutor, magician.

the learner can go and honestly and completely on their own say finxi about something before the teacher does, and then the teacher can with delight choose how to teach from their, leaping on the opportunity.

there is no separate judge, there is only the teacher and the laerner, and the teacher's feedback that is communicated to the learner, plus the objective behavior of the creation itself inside the workshop, are the sources that inform whether a claim to finxi is honest.

saying finxi for a model just means showing the other model something or mentioning its existence once it is sitting in storage after being created.

Both decide whats interesting and useful, but also both need to be able to experience surprise over time as things compose in unexpected ways.

the learner on day one is just eager, that is all i know.

### craftsman

the teacher provides their teachings in the form of sayings, images, projects, ideas, challenges, direct instruction, hints, one on one feedback sessions, quizzes, magic tricks to inspire wonder, all of it.

the word magician is meant to convey that the teacher should not always immediately reveal the method.

as the self-play from zero training data paper shows, the teacher learns completely freshly inside the workshop how to teach the learner based on the learner's trajectory. It is ridiculous to think any teacher is no longer themselves a learner, just as it is ridiculous to assume a parent stops aging.

there is some level of shared ability to communicate and understand in the same language between teacher and learner, but that does not preclude the teacher from still needing to learn the curriculum as they go.

### tools

on day 1 they may have some starter tools

in this workshop, the best analogy for tools is just data types and primitives, eg string, thats both a real life primitive and a programming primitive

byte, string, int, frac (ratio, hence all floats), line (geometric primitive of a line segment), list, set, map, point, circle

creations sit idle in storage (unless some of them operate on their own as machines, of course).

rosenblum's classic 'the design and implementation of a log structured filesystem'. they could have log as the primitive instead of git (which is a way of doing logs, so to speak, except maybe logs matter more than commits for our creators in the workshop)

solomonoff's prior is an index, not a 'shelving', of Babel via length of generating programs instead of via texts.

Chaitin and algorithmic information theory has important things to say here.

the agents are not able to look up strings directly in their digital index over Babel, so I suppose they are searching in the book of all programs.

I dont need to train models with GPUs inherently at all! We can still explore the concept in general. My goal is not to be a conventional AI paper.

if we just care about the log, it might mean it makes it easier for other people to replicate if we can make our work feel as simple as a sqlite log of work and creations.

just one log, everything can be typed in the log as an event, a communication, or a creation. Simple.

set up the environment (what we will later call the workshop of icaria) for unbounded creation storage, setting up the models to actually save creations, tinker, compose creations

### have they created X yet?

take inspiration from the voyager paper headline chart: have they created X yet? We could then show increasingly cool math objects appear organically over time, and we could study the order in which things were created, e.g. if kernels were invented way before circuits or vice versa that would be really interesting. Also, if we could run the entire history of ICARIA multiple times, we could see if there is any variance in the order of creation!

only measure 'have they created X yet' for X that dont exist in the primitives we give them at training start.

EurekaBench https://arxiv.org/pdf/2610.00492 will be useful not for training inspiration but as evaluation data as a test of transfer from what we learn synthetically to real world test cases!

we should cite this rylan schaeffer tweet https://x.com/RylanSchaeffer/status/2106082985032454155

### rediscovery

rediscovery is important, in order to really make this experiment pop, we will look for some mechanism to be created organically within the workshop that allows the teacher and learner to decide whether a creation is a new creation or whether it already exists in the workshop, and to make similarity measurements, it would be so fucking hilarious if they reinvented something like category theory for this.

## ICARIA

the icaria story asks whether the idea can be recognized and understood more effectively via analogy and story.

it is an unbounded workshop. everything ever made is somewhere, and who knows what might fit together.

open-ended is indeed what I basically had in mind, ICARIA is just a workshop, and there will be many potential uses of the creations, but from their POV the work is open ended.

they have access to the online library of babel (borges), generalized from every possible book of 410 pages to every finite string, all already written down and stored. Their workshop is different, the creations dont exist as potentialities, they must be created to exist.

the library of babel is theory, this can be the workshop of icaria

umberto eco 'Library as a Model for Culture: Preserving, Filtering, Deleting and Recovering.'

icaria is, in my borges mind and my kafka mind, the name of the unbounded workshop daedalus trapped himself in to hide.

when icarus fell, daedalus mourned him by naming things like seas and islands after him.

> he buried his body in a tomb, and the land was called from the name of him buried there.
>
> Ovid, *Metamorphoses* VIII, tr. Henry T. Riley (Project Gutenberg #26073)

it is an unbounded workshop, daedalus' atonement.

we should no longer consider icaria an infinite workshop

riemannian's distinction

reword infinite to unbounded when appropriate, this will help us distinguish the boundedness of the model computation from the unboundedness of log storage

bounded computation, bounded intelligence, and bounded creativity

> In the extension of space-construction to the infinitely great, we must distinguish between unboundedness and infinite extent, the former belongs to the extent relations, the latter to the measure-relations.
>
> Riemann, *On the Hypotheses which lie at the Bases of Geometry* (1854), tr. W. K. Clifford

this use of unlimited vs finite/infinite is helped by Riemann's 1854 lecture on foundations of differential geometry

I think Riemann helped me see that endlessness and sizelessness are distinct! I can trap an infinitely branching tree inside a finite snowglobe.

### daedalus

Nobody should know about Daedalus' story, it should just be the title of the story portion 'The Workshop of Icaria'.

the workshop teacher can be imbued to start with the spirits of pythagoras and daedalus, where daedalus by now is much, much older, and he's spent the rest of his life reflecting and learning from his mistake, and in some ways he sees icarus in the learner.

he has gotten older and wiser and isnt the jealous or careless man he used to be. So he's learned from his own mistakes and is truly ready to apprentice someone greater than himself

Daedalus views himself as the minotaur of his own past, and as long as he remains within a labyrinth of a workshop, he can teach his learner in peace while still learning himself and the outside world beyond the labyrinth can hopefully benefit from a gizmo or two

perdix should be in his reflections

> a prattling partridge beheld him from a branching holm-oak, and, by its notes, testified its delight. 'Twas then but a single bird {of its kind}, and never seen in former years, and, lately made a bird, was a grievous reproof, Dædalus, to thee. For, ignorant {of the decrees} of fate, his sister had entrusted her son to be instructed by him, a boy who had passed twice six birthdays, with a mind eager for instruction. 'Twas he, too, who took the backbones observed in the middle of the fish, for an example, and cut {a} continued {row of} teeth in iron, with a sharp edge, and {thus} discovered the use of the saw.
>
> He was the first, too, that bound two arms of iron to one centre, that, being divided {and} of equal length, the one part might stand fixed, {and} the other might describe a circle. Dædalus was envious, and threw him headlong from the sacred citadel of Minerva, falsely pretending that he had fallen {by accident}. But Pallas, who favours ingenuity, received him, and made him a bird
>
> Ovid, *Metamorphoses* VIII, tr. Henry T. Riley (Project Gutenberg #26073)

### flying too close to the sun

learner could get hurt. Flying too close to the sun is a very general class of risks. Not sure at the moment how daedalus warns, but like a good grandfather he should allow for freedom and play while providing wisdom

breaking creativity via mental damage, losing progress by breaking objects in the workshop, and death by breaking the workshop and/or one's existence in it

> "Icarus, I recommend thee to keep the middle tract; lest, if thou shouldst go too low, the water should clog thy wings; if too high, the fire {of the sun} should scorch them. Fly between both"
>
> Ovid, *Metamorphoses* VIII, tr. Henry T. Riley (Project Gutenberg #26073)

## homage

Finxi is also an homage to Marc Finzi, a really cool guy I hung out with when I visited carnegie mellon.

I grew up going to school with Will Merrill. I feel so blessed and grateful
