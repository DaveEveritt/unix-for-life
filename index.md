# Basics of the Unix Philosophy for life
{: .no_toc}

([GitHub repo](https://github.com/DaveEveritt/unix-for-life))

* auto-gen TOC:
{:toc}

## Modularity: Write Simple Parts Connected by Simple Language

> To tackle complex issues that won’t fall apart, keep global complexity down. Instead, foster simple parts connected by well-defined communication channels and clear language, so problems remain local to a specific area, and it’s possible to update one part without breaking the whole.

## Clarity: Clarity is Better Than Cleverness

> Write policies as if the most important communication is not to the system but to the people who will implement and maintain them in future (including yourself). Make key points graceful and clear to reduce the chance of misinterpretation.

## Composition: Create Systems to be Connected to Other Programs

> To make systems composable, decouple them. A system—or individual—at one end of a process only needs to know what is *absolutely necessary* about processes at the other end—they should not depend on it. Make it easy to replace one end with a newer, updated or different system without disturbing the other end.

## Separation: Separate Policy From Implementation; Separate Idealism From Action

> Policy and implementation of policy operate at different timescales. Policy can change faster than the ability to implement it. Political and social trends come and go but basic human needs and ways of working change very little. Respect inertia to changes that happen too often or too quickly.

## Simplicity: Design For Simplicity; Add Complexity Only Where You Must

> encourage a “small is beautiful” culture that actively resists bloat and complexity, puts a high value on simple solutions, finds ways to break systems up into small cooperating pieces, and fights attempts to add anything lacking elegance, meaning or function.

## Parsimony: Create Big Things Only When Demonstrably Clear Nothing Else Will Do

> Allowing structures—social or material—to get too big in volume and/or internal complexity harms maintainability. People resist discarding visible products or time investments in the familiar, but big structures accumulate over-investment in things that can fail spectacularly, become inefficient or hard to update. Centralised system collapses bring down everything else.

## Transparency: Design For Visibility to Make Inspection And Correction Easier

> A system is *transparent* when you can immediately understand what it’s doing and how. It is *discoverable* when its internal state can be monitored and displayed. If it functions well, it needs to be *seen* to function well. Use the principle of least surprise by appealing to pre-existing knowledge and assumptions. Don’t be too clever.

## Robustness: The Child of Transparency And Simplicity

> Large systems tend to be fragile and error-prone because they’re too complicated to understand all at once. When internal workings are obscure or not open to scrutiny, it’s hard to tell if it’s fair, or to fix what’s broken. Uncomplicated systems are robust when people can reason about their processes easily. If no-one can work out what’s gone wrong, no-one can fix the problem.

## Representation: Fold Knowledge Into Data so People Don’t Need to Work Out What to do

> Hide complexity in data, but keep *procedures on data* simple (e.g. easy to update or retrieve). Store acquired knowledge as data for others to access—for instance, staff changes lose valued experience and acquired wisdom unless this is captured. Well-structured data are easier to understand than complex procedures. Simplify data presentation in at-a-glance chunks, but enable access to in-depth specifics at any point.

## Silence: When There’s Nothing Surprising to Say, Say Nothing

> when a system has nothing interesting or surprising to say, it should shut up. Well-behaved systems (and departments) are unobtrusive. Don’t pollute important information with unnecessary verbosity, internal organisational behavior, catchphrases, acronyms, congratulations, personal messages etc. Avoid pushing more information than required—share only what’s crucial and essential.

## Repair: When Something Fails, Make it Fail Noisily And as Soon as Possible

> Reveal errors and mistakes immediately for rapid fixing. Encourage error-reporting and problem-sharing. If something doesn’t work, prevent escalation by making it public. Presume that apparent human errors are from being misled—if a system *allows mistakes*, don’t make people feel stupid—see the system as the point of failure. MAke every confused user an ally for improvement.

## Economy: Person-time is Expensive, Conserve it Over System Administration

> Don’t laboriously undertake manual or repetitive tasks; create automated routines or, for more demanding jobs, offer step-by-step guides for others to follow without learning how they work. Where automation is possible, set up machines to follow previously-tested procedures, or enable them to check for certain triggers (e.g. time- or date-sensitive) and initiate automatic tasks, optionally informing someone afterwards to validate the outcome.
> 
> This leads to…

## Generation: Avoid Guesswork When Automating, Check For Error-Free Outcomes And Enable Reversal

> Individual human input is a source of delay and error. Simpler guidelines make it more likely the operator will get it right. Time-tested automated procedures are almost always more reliable than hand-operated ones. Use automation or simple guides where they aid abstraction i.e make guidelines to *operate* a process simpler than the process itself. Avoid unnecessary details. Before any change, preserve the current state to enable a “rollback”.

## Optimization: Prototype Early; Get Stuff Working Instead Aiming For Perfection

> Don’t plan every detail top-down; you can’t predict what might happen in actual practice. Invite people to try things early and give feedback, yet resist demands for change until there’s enough input to guarantee improvement or better user experience. “Make it work, then make it right, then make it easy”. Delivering 90% of something is better than failing to deliver at all. After adjustments, invite people to try again, and repeat—make them part of the process.

## Diversity: Distrust All Claims For One True Way”, Embrace the Excluded and Uninvited

> There is rarely a single correct approach, because there is no way to anticipate everything, or forecast how people will respond to systems, groups or individuals. Without good channels of communication, systems or organisations become isolated, over-confident, self-referential, prone to arrogance and liable to subjective error, partly from the exclusion of anyone outside its boundaries. Remain open to unexpected and diverse inputs, multiple responses and approaches, and unforeseen interactions.

## Extensibility: Anticipate the Future, Because it Will be Here Sooner Than You Think

> Never assume something is finished—leave room to grow, but preserve each stable state. Record full details of additions or changes in self-contained documents independent of the system. Use comments like “If you ever need to…”. clear yet flexible connections between different components enable new methods to replace old ones without conflict. Above all, avoid complete rebuilds by using modular elements that can be updated or replaced independently without disrupting what already works. New functions should plug in without disruption. When future-proofing, you will also save your own sanity if you end up being the one making the changes!
