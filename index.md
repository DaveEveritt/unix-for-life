# Basics of the Unix Philosophy for life

{:toc}

## Modularity: Write simple parts connected by simple language

> The only way to tackle complex issues that won’t fall apart is to keep global complexity down. Instead, foster simple parts connected by well-defined communication channels and understandable language, so most problems are local to a specific area and there are opportunities for updating one part without breaking the whole.

## Clarity: Clarity is better than cleverness

> Write policies as if the most important communication they have is not to the system but to the people who will live them out, implement and maintain them in future (including yourself). Make the key points graceful and clear to ensure that they’re less likely to be interpreted wrongly.

## Composition: Create systems to be connected to other programs

> To make systems composable, decouple them. A system or individual at one end of a process should know only what is *absolutely necessary* about the processes of the system at the other end—they should not depend on it. It should be easy to replace one end with a newer, updated or different system without disturbing the other end.

## Separation: Separate policy from implementation; separate idealism from action

> Policy and implementation tend to mutate at different timescales, with policy changing much faster than the ability to implement it. Political and social trends and fashions come and go, but basic human needs, methods of implementation and psychology change very little. Respect inertia to policy changes that happens too often or too quickly.

## Simplicity: Design for simplicity; add complexity only where you must

> encourage a culture that knows that small is beautiful, that actively resists bloat and complexity: a tradition that puts a high value on simple solutions, that looks for ways to break systems up into small cooperating pieces, and that reflexively fights attempts to add anything that has no beauty, meaning or function.

## Parsimony: Create big things only when it is clear by demonstration that nothing else will do

> *Big* means both large in volume, and by internal complexity. Allowing structures—social or material—to get too large hurts maintainability. People are reluctant to throw away the visible product or time investment put into what they work on and with, but overly large structures invite over-investment in approaches that can fail spectacularly or become suboptimal and hard to update. If a big centralised system breaks, it will bring down eveything else.

## Transparency: Design for visibility to make inspection and correction easier

> A system is transparent when you can look at it and immediately understand what it is doing and how. It is discoverable when it has facilities for monitoring and can display its internal state so that it not only functions well, but can be *seen* to function well. Use the principle of least surprise by appealing to peoples’ pre-existing knowledge and assumptions. Don’t confuse things by being too clever.

## Robustness: The child of transparency and simplicity

> Large systems tend to be fragile and error-prone because they’re too complicated for human understanding to grasp all at once. When the internal workings of a system are obscure or not open to scrutiny, you can’t be sure it’s fair, or see how to fix it if it’s broken. Systems are most robust when they’re uncomplicated enough for people to reason about their processes without struggling to understand them. If no-one can work out what’s gone wrong, no-one can fix the problem.

## Representation: Fold knowledge into data so people don’t need to work out what to do

> Hide complexity in data, but keep procedures on data simple (e.g. make it easy to edit). Store acquired knowledge as data for others to access—for instance, staff turnover can lose valuable experience and wisdom if this on-the-ground knowledge is not captured. Plain, well-structured data is easier to understand than complex procedures. Simplify presentation into unabmiguous chunks that can be seen at a glance. We don’t always need to grasp every detail, but where more knowledge is requested, provide pointers that enable people to travel from any facet to specific in-depth details.

## Silence: When there’s nothing surprising to say, say nothing

> when a system has nothing interesting or surprising to say, it should shut up. Well-behaved systems (and departments) do their jobs unobtrusively, with a minimum of fuss and bother. Important information should not be polluted by verbosity about what’s happening at every moment, or about internal organisational behavior, catchphrases, acronyms, congratulations, personal messages and so on. People don’t need any more information than what they need to know art any given time, so share only what’s crucial and essential.

## Repair: When something fails, make it fail noisily and as soon as possible

> Don’t conceal errors—the sooner they’re revealed, the quicker they can be fixed. If something doesn’t work as expected, make the issue public to prevent it escalating to other areas. If the cause appears to be generated by people, presume that they’re being misled into making a mistake. Encourage error-reporting so people can share problems they’re having. Shift repsonsibility towards the system as the point of failure. People don’t need to feel “stupid for making a mistake” if a system *allows mistakes* to be made. Every confused user who reports a problem is a valuable ally towards improvement in quality.

## Economy: person-time is expensive, conserve it in preference to time spent on system administration

> Don’t laboriously undertake tasks manually when they can be handled at a less complex level. Create routines that automate repetitive tasks, or offer step-by-step guides to cognitively-demanding jobs so that others can follow them easily without learning everything about how they work (unless that’s part of their job). Wherever tedious administration can be automated, make it possible either for someone to instruct a machine to do the work, following a previously-tested procedure, or set up a machine to check for certain triggers (e.g. time- or date-sensitive) and then initiates and completes this administration automatically, possibly informing someone afterwards who can ensure that it’s done.
> 
> This leads to…

## Generation: Avoid guesswork when creating automated processes, ensure they produce error-free outcomes and can be undone if in error

> Human beings are notoriously bad at processing details… any kind of procedure that depends on individual input is a rich source of delays and errors. The simpler and more abstracted the guidelines, the more likely it is that the human designer will get it right. Time-tested automated procedures (at every level) are almost always cheaper and more reliable than hand-operated ones. So use automated generators of output or simple guides whenever they can raise the level of abstraction; that is, when the guidelines to operate an automated process are made simpler than the underlying process itself. No-one needs to be held back by unecessary details that can be automated. To be absolutely sure, before executing a change, store or record the current state to enable a “rollback”, just in case.

## Optimization: Prototype things as soon as possible; get stuff working instead of trying to make it perfect

> don’t delay by planning every detail of something top-down from the start—you won’t be able to predict what might need to be done once other people or teams get involved. Get things up and running, then invite those who will use the system/thing/process to try it out and give feedback. Resist changing anything until there’s enough concrete input from those involved to ensure that any change *improves* the service or process, or enhances people’s experience of it. To sum up: “Make it work, then make it right, then make it easy”. Delivering 90% of something is better than failing to deliver anything at all. After adjustments made from feedback, invite them try it again, and repeat. Make them part of the process.

## Diversity: Distrust all claims for “one true way”, embrace the excluded and uninvited

> There is rarely a single correct way of doing things, because there is never a way to anticipate eveything that might happen, or how people might respond to a system, a group or a person. If there are no channels of communication a system or organisation becomes isolated, over-confident, self-referential and prone to arrogance, as well as liable to subjective error and the exclusion of those outside its own boundaries. We need to remain open to unexpectied and diverse inputs, multiple responses and approaches, and unforeseen interactions.

## Extensibility: Anticipate the future, because it will be here sooner than you think

> Never assume something is completely finished. Leave room for a system to grow… make sure there’s a record of each stable state. Then, if things are added or changed, when and what they are can be recorded in self-contained explanations that don’t depend on anything else or confuse the original system. Enable old methods to be replaced by new ones without confusion. Anticipate the future by making connections between different components clear and yet flexible. Add comments like “If you ever need to…” in any documentation. Above all, make a system resistant to complete rebuilds by using modular elements that can be updated or replaced without disrupting what already works well, so new functions can be plugged in without having to scrap and rebuild everything. When you design for the future, the sanity you save may be your own. Presume that you might be the one making future changes.
