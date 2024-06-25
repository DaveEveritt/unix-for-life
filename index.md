# Basics of the Unix Philosophy for life

([GitHub repo](https://github.com/DaveEveritt/unix-for-life))

* auto-gen TOC:
{:toc}

## Modularity: Write simple parts connected by simple language

> The only way to tackle complex issues that won’t fall apart is to keep global complexity down. Instead, foster simple parts connected by well-defined communication channels and understandable language, so most problems are local to a specific area and there are opportunities for updating one part without breaking the whole.

## Clarity: Clarity is better than cleverness

> Write policies as if the most important communication they have is not to the system but to the people who will implement and maintain them in future (including yourself). Make the key points graceful and clear to ensure that they’re less likely to be misinterpreted.

## Composition: Create systems to be connected to other programs

> To make systems composable, decouple them. A system or individual at one end of a process should know only what is *absolutely necessary* about the processes at the other end—they should not depend on it. Make it easy to replace one end with a newer, updated or different system without disturbing the other end.

## Separation: Separate policy from implementation; separate idealism from action

> Policy and implementation mutate at different timescales—policy changes much faster than the ability to implement it. Political and social trends and fashions come and go, but basic human needs, methods of implementation and psychology change very little. Respect inertia to policy changes that happen too often or too quickly.

## Simplicity: Design for simplicity; add complexity only where you must

> encourage a culture that knows that small is beautiful, that actively resists bloat and complexity: a tradition that puts a high value on simple solutions, looks for ways to break systems up into small cooperating pieces, and reflexively fights attempts to add anything that has no elegance, meaning or function.

## Parsimony: Create big things only when it is demonstrably clear that nothing else will do

> *Big* means both large in volume, and internal complexity. Allowing structures—social or material—to get too big hurts maintainability. People resist throwing away the visible product or time investment put into what they work on and with, but too-large structures invite over-investment in approaches that can fail spectacularly or become suboptimal and hard to update. If a big centralised system breaks, it brings down everything else.

## Transparency: Design for visibility to make inspection and correction easier

> A system is *transparent* when you can look at it and immediately understand what it is doing and how. It is *discoverable* when it has facilities for monitoring and can display its internal state so that it not only functions well, but can be *seen* to function well. Use the principle of least surprise by appealing to peoples’ pre-existing knowledge and assumptions. Don’t confuse things by being too clever.

## Robustness: The child of transparency and simplicity

> Large systems tend to be fragile and error-prone because they’re too complicated for human understanding to grasp all at once. When the internal workings of a system are obscure or not open to scrutiny, you can’t be sure it’s fair, or see how to fix what’s broken. Systems are most robust when uncomplicated enough for people to reason about their processes without struggling to understand them. If no-one can work out what’s gone wrong, no-one can fix the problem.

## Representation: Fold knowledge into data so people don’t need to work out what to do

> Hide complexity in data, but keep *procedures on data* simple (e.g. easy to update or retrieve). Store acquired knowledge as data for others to access—for instance, staff turnover loses valuable experience and on-the-ground wisdom if this isn’t captured. Plain, well-structured data is easier to understand than complex procedures. Simplify data presentation in unambiguous at-a-glance chunks. We don’t always want every detail, but where more knowledge is requested, enable people to to open in-depth specifics from any facet.

## Silence: When there’s nothing surprising to say, say nothing

> when a system has nothing interesting or surprising to say, it should shut up. Well-behaved systems (and departments) do their jobs unobtrusively, with a minimum of fuss and bother. Important information should not be polluted by verbosity about what’s happening at every moment, or about internal organisational behavior, catchphrases, acronyms, congratulations, personal messages and so on. People don’t need any more information than what is required at any given time, so share only what’s crucial and essential.

## Repair: When something fails, make it fail noisily and as soon as possible

> Don’t conceal errors and mistakes—the sooner they’re revealed, the quicker they can be fixed. If something doesn’t work as expected, make the issue public to prevent it escalating elsewhere. If the cause appears to be human error, presume that they’re being misled into making a mistake. Encourage error-reporting so people share problems they’re having. Shift responsibility towards the system as the point of failure. Don’t make people feel stupid for making a mistake if a system *allows mistakes*. Every confused user who reports a problem is a valuable ally towards improvement.

## Economy: person-time is expensive, conserve it over system administration

> Don’t laboriously undertake manual tasks that can be handled at a less complex level. Create routines to automate repetitive tasks, or offer step-by-step guides to cognitively-demanding jobs for others to follow easily without learning how they work (unless that’s their job). Where tedious administration can be automated, set up a machine to do the work, following a previously-tested procedure, or enable a machine to check for certain triggers (e.g. time- or date-sensitive) that initiate and complete tasks automatically, optionally informing someone afterwards who can ensure that it’s done.
> 
> This leads to…

## Generation: Avoid guesswork when automating, check for error-free outcomes, enable reversal if wrong

> Human beings are bad at processing details; individual input is a rich source of delay and error. The simpler the guidelines, the more likely the operator will get it right. Time-tested automated procedures (at every level) are almost always cheaper and more reliable than hand-operated ones. So use automated output generators or simple guides whenever they raise the level of abstraction; that is, make guidelines to *operate* a process simpler than the process itself. Don’t clutter things with unnecessary details that can be automated. As a failsafe, preserve the current state to enable a “rollback”.

## Optimization: Prototype things as soon as possible; just get stuff working instead aiming for perfection

> don’t plan every detail top-down from the start—you can’t predict what might need to be done once people and teams get involved. Once up and running, invite users to try it and give feedback. Resist demands for changes until there’s enough input from those involved to guarantee *improvements* of the service or process, or people’s experience of it. To sum up: “Make it work, then make it right, then make it easy”. Delivering 90% of something is better than failing to deliver at all. After feedback-informed adjustments, invite people to try it again, and repeat. Make them part of the process.

## Diversity: Distrust all claims for “one true way”, embrace the excluded and uninvited

> There is rarely a single correct way of doing things, because there is never a way to anticipate everything that might happen, or how people might respond to a system, a group or a person. If there are no channels of communication, a system or organisation becomes isolated, over-confident, self-referential and prone to arrogance, as well as liable to subjective error and the exclusion of those outside its own boundaries. We need to remain open to unexpected and diverse inputs, multiple responses and approaches, and unforeseen interactions.

## Extensibility: Anticipate the future, because it will be here sooner than you think

> Never assume something is finished—leave room to grow, but keep records of each stable state. If adding or changing anything, record when and what they are in self-contained documents independent of the original system. Enable old methods to be replaced by new ones without conflict, making connections between different components clear and yet flexible. In documentation, use comments like “If you ever need to…”. Above all, make a system resistant to complete rebuilds by using modular elements that can be updated or replaced without disrupting what already works well, so new functions can be plugged in without having to rebuild everything. When you design for the future, the sanity you save may be your own—you might be the one making the changes.
