# finxi

a craftsperson's apprentice in an unbounded workshop

what i have not created i do not understand

introduce FINXI as my AIXI and to introduce the concept (e.g. maybe as a section at the end of the paper) of the Workshop of Icaria, to convey the image of the FINXI model as the craftsperson's apprentice in an unbounded workshop with the craftsperson having a nice silent backstory like a remorseful atoneful Daedalus and with the tools corresponding to the exact primitives we want to give our models to use at start.

three sections in this paper. FINXI, GEN, and ICARIA. all three sections go at the same idea, but the first goes at it as pure theory and names it FINXI like AIXI, the second goes at it as practical implementation and names it GEN like GAN, the third goes at it as allegorical story and names it ICARIA like ICARUS.

## FINXI

aixi is a claim to a universal predictor.

they call AIXI the universally intelligent agent

FINXI, its just a creative agent

not god vibes.

dont use apprentice in section 1 finxi, section 1 finxi should really approach the theory of creativity and intelligence like hutter approached aixi.

### creation

Maybe creation is simply what we can talk about here. Taking primitives, creating/making something. construction is a bit formal, the same way 'formulation' might have been too formal relative to hutter's more familiar choice of intelligence

construction can be entirely for its own sake, think about the history of math and science.

I am not sure that generating byte sequences is any different from predicting the next sequence element. I think I would prefer if the creations were actual usable tools or artifacts or maybe simply just interesting objects and mathematical constructions, but I admit this is still extremely imprecise. That being said, byte sequences are super general and form a basic substrate that programs compile into.

i think construction isnt quite the same concept as generation, i think construction is much more system 2 compared to the relative system 1ness of generation.

I dont want to restrict the apprentice to making circuits, i think they should be free to make anything

### comprehension

aixi was always flawed and so was anything that ever tried to monomaniacally impose an idea of scalar utility or reward. i think in the jurgen schmidhuberian sense, in the karl fristonian sense, in the david chalmersian sense, in the charles darwinian and erasmus darwinian sense, in the kantian and jungian sense, we have plenty of evidence that creation for fun's sake on its own can exist organically as the way a living thing intervenes on objective experience to bring about surprise and delight as subjective experience.

i think in a pythagorean sense, in a martin buber sense, in a Logos sense, it is inherently about comprehension of existence, not compression. i really believe in comprehension's supremacy, not compression's. this means we must view the comprehension of existence, beauty, meaning, etc as its own reward.

construction is not the same as comprehension/understanding/getting it! as an educator i like to approach this in a very simple way, construction is playful and it is an action and an environment that fosters and nurtures the senses of composition, function, behavior, error, regularity, symmetry, and more!! Pure understanding is quite naturally an emergent phenomenon on top of all that constructive activity.

comprehension is getting it, you get it or you dont, and assessing comprehension is likely the central problem in education, and all the best teachers know the problems in using scalars here. Doing new things is a better bit of evidence of comprehension

### the past tense

It plays upon a basic suspicion people all over the world have semicorrectly had about AI the whole time - how did it do that? did it just look up the answer somewhere? Both yes and no. If it is has already constructed the sequence, or sequences like it during pretraining, it doesnt have to build from scratch, it is mostly leveraging stuff its built already

## GEN

gen should really be the meat of the paper, with simple clear empirical work, not theory.

GEN (Generative Educational Network). Thats the pair. maybe the interesting exploration is whether a GEN in practice can one day be the most creative agent in the form of the apprentice (FINXI)

similar to a GAN, except instead of a discriminator learning to tell apart real vs fake generations from an adversarial generator, a learner just predicts the byte sequences taught by an educational generator

my gen definition was based on the self play paper itself, not FINXI! maybe GEN is more general than prediction and creation, but anything taught.

GEN is 1) generator/generative, 2) general, 3) (maybe someday) genetic (e.g. GEPA genetic pareto)

the reason i consider GEN more general than GAN is 1) wordplay GEN is GENeral 2) many adversarial coaches think they are being educational and often...they can be correct, and some great teachers can switch on adversariality occasionally quite effectively

apprentice for learner, and craftsman for teacher

there is just the GEN in our implementation, which will consist of two networks, the teacher and the learner. I dont know if the right thing to say is if they are two halves of the same network, or if they are two connected networks.

recognition will just be up to them, and they can build tools to enable further recognition

we the people on the outside will just be able to search their log and creations ourself

only one teacher and one learner

both the teacher and the learner in the GEN need to be able to say finxi honestly, that they have both created, ideally independently with a useful story usually being the teacher making something and then the learner being shown the thing and trying to make it themself and the teacher being a world class master, apprentice, tutor, magician.

the learner can go and honestly and completely on their own say finxi about something before the teacher does, and then the teacher can with delight choose how to teach from their, leaping on the opportunity.

there is no separate judge, there is only the teacher and the laerner, and the teacher's feedback that is communicated to the learner, plus the objective behavior of the creation itself inside the workshop, are the sources that inform whether a claim to finxi is honest.

saying finxi for a model just means showing the other model something or mentioning its existence once it is sitting in storage after being created.

the agents' objectives are nonscalar, but all their measurements with their own creations and primitives and data types are of course numerical in some sense or in a direct sense.

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

rosenblum's classic 'the design and implementation of a log structured filesystem'. in addition to some digital library of babel where they can look up all possible strings, they could have log as the primitive instead of git (which is a way of doing logs, so to speak, except maybe logs matter more than commits for our creators in the workshop)

solomonoff's prior is an index, not a 'shelving', of Babel via length of generating programs instead of via texts.

Chaitin and algorithmic information theory has important things to say here.

the agents are not able to look up strings directly in their digital index over Babel, so I suppose they are searching in the book of all programs.

I dont need to train models with GPUs inherently at all! We can still explore the concept in general. My goal is not to be a conventional AI paper.

if we just care about the log, it might mean it makes it easier for other people to replicate if we can make our work feel as simple as a sqlite log of work and creations. its possible a sqlite of pointers to sqlites (durable objects made simple) is the simplest thing here.

set up the environment (what we will later call the workshop of icaria) for unbounded creation storage, setting up the models to actually save creations, tinker, compose creations

### have they created X yet?

take inspiration from the voyager paper headline chart: have they created X yet? We could then show increasingly cool math objects appear organically over time, and we could study the order in which things were created, e.g. if kernels were invented way before circuits or vice versa that would be really interesting. Also, if we could run the entire history of ICARIA multiple times, we could see if there is any variance in the order of creation!

### rediscovery

rediscovery is important, in order to really make this experiment pop, we will look for some mechanism to be created organically within the workshop that allows the teacher and learner to decide whether a creation is a new creation or whether it already exists in the workshop, and to make similarity measurements, it would be so fucking hilarious if they reinvented something like category theory for this.

## ICARIA

the icaria story asks whether the idea can be recognized and understood more effectively via analogy and story.

it is an unbounded workshop. everything ever made is somewhere, and who knows what might fit together.

they have access to the online library of babel (borges) where every sequence that could exist has already been written down and is stored. Their workshop is different, the creations dont exist as potentialities, they must be created to exist.

the library of babel is theory, this can be the workshop of icaria

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
