# Basics of the Unix Philosophy for life

## Modularity: Write simple parts connected by simple language

> The only way to tackle complex issues that won't fall apart is to hold global complexity down — to foster simple parts connected by well-defined communication channels and understandable language, so most problems are local to a specific part and there's some hope of updating one without breaking the whole.

## Clarity: Clarity is better than cleverness

> Write policies as if the most important communication they have is not to the system but to the people who will implement, live them out and maintain them in future (including yourself). Making the key points graceful and clear... means they're less likely to be interpreted wrongly.

## Composition: Create systems to be connected to other programs

> To make systems composable, decouple them. A system at one end of a process should know only what is necessary about the processes of the system at the other end—it should not depend on it. It should be easy to replace one end with a newer, updated or different system without disturbing the other.

## Separation: Separate policy from implementation; separate idealism from action

> Policy and implementation tend to mutate at different timescales, with policy changing much faster than the ability to implement it. Political and social trends may come and go, but basic human needs, methods of implementation and psychology change very little.

## Simplicity: Design for simplicity; add complexity only where you must

> encourage a culture that knows that small is beautiful, that actively resists bloat and complexity: a tradition that puts a high value on simple solutions, that looks for ways to break systems up into small cooperating pieces, and that reflexively fights attempts to add anything that has no beauty, meaning or function.

## Parsimony: Create big things only when it is clear by demonstration that nothing else will do

> ‘Big’ = both large in volume and internal complexity. Allowing structures—social or material—to get too large hurts maintainability. People are reluctant to throw away the visible product of lots of work, but overly large structures invite over-investment in approaches that are failed or suboptimal.

## Transparency: Design for visibility to make inspection and debugging easier

> A system is transparent when you can look at it and immediately understand what it is doing and how. It is discoverable when it has facilities for monitoring and can display its internal state so that it not only functions well, but can be *seen* to function well.

## Robustness: the child of transparency and simplicity.

> Large systems tend to be fragile and error-prone because they're too complicated for human understanding to grasp all at once. When you can't understand the internal workings of a system, you can't be sure it's fair, or fix it if it's broken. Systems are simple when they're uncomplicated enough for people to reason about their processes without struggling to understand them.

** ============== DONE TO HERE ============== **

## Representation: Fold knowledge into data so program logic can be stupid and robust.

(data can be complex, but the handling and presentation of data needs to be understandable—shift complexity towards data, keep it away from the handling and presentation fo that data. Make the handling and presentation of complex data simple and robust)

> Data is more tractable than program logic. It follows that where you see a choice between complexity in data structures and complexity in code, choose the former. More: in evolving a design, you should actively seek ways to shift complexity from code to data. C's facility at manipulating pointers has encouraged the use of dynamically-modified reference structures at all levels of coding from the kernel upward. Simple pointer chases in such structures frequently do duties that implementations in other languages would instead have to embody in more elaborate procedures.

## Repair: When you must fail, fail noisily and as soon as possible.

> It's best when software can cope with unexpected conditions by adapting to them, but the worst kinds of bugs are those in which the repair doesn't succeed and the problem quietly causes corruption that doesn't show up until much later. Therefore, write your software to cope with incorrect inputs and its own execution errors as gracefully as possible. But when it cannot, make it fail in a way that makes diagnosis of the problem as easy as possible. Design for generosity rather than compensating for inadequate standards with permissive implementations (e.g. HTML tag soup).

## Economy: Programmer time is expensive; conserve it in preference to machine time.

(don't laboriously undertake tasks manually when they can be handled at a less complex level)

> If we took this maxim really seriously... most applications would be written in higher-level languages like Perl, Tcl, Python, Java, Lisp and even shell — languages that ease the programmer's burden by doing their own memory management. One other obvious way to conserve programmer time is to teach machines how to do more of the low-level work of programming. This leads to...

## Generation: Avoid hand-hacking; write programs to write programs when you can.

(in creating processes that automate other processes, ensure that they generate error-free outcomes)

> Human beings are notoriously bad at sweating the details... any kind of hand-hacking of programs is a rich source of delays and errors. The simpler and more abstracted your program specification can be, the more likely it is that the human designer will have gotten it right. Generated code (at every level) is almost always cheaper and more reliable than hand-hacked. It pays to use code generators when they can raise the level of abstraction — that is, when the specification language for the generator is simpler than the generated code... (code generators are heavily used to automate error-prone detail work. Parser/lexer generators are the classic examples; makefile generators and GUI interface builders are newer ones.)

## Optimization: Prototype before polishing. Get it working before you optimize it.

(don't plan every detail from the start - you won;t be able to predict what needs to be done. Get things up and running, then bring in the people who will use a system to try it out and give you feedback)

> Kernighan & Plauger's; “90% of the functionality delivered now is better than 100% of it delivered never”. premature local optimization actually hinders global optimization (and hence reduces overall performance). A prematurely optimized portion of a design frequently interferes with changes that would have much higher payoffs across the whole design, so you end up with both inferior performance and excessively complex code. ‘Extreme programming' guru Kent Beck: “Make it run, then make it right, then make it fast”. ...tune systematically, looking for the places where you can buy big performance wins with the smallest possible increases in local complexity.
> 
>>	"it is much easier to judge whether a prototype does what you want than it is to read a long specification. I remember one development manager at Bellcore who fought against the “requirements” culture years before anybody talked about “rapid prototyping” or “agile development”. He wouldn't issue long specifications; he'd lash together some combination of shell scripts and awk code that did roughly what was needed, tell the customers to send him some clerks for a few days, and then have the customers come in and look at their clerks using the prototype and tell him whether or not they liked it. If they did, he would say “you can have it industrial strength so-many-months from now at such-and-such cost”. His estimates tended to be accurate, but he lost out in the culture to managers who believed that requirements writers should be in control of everything." - Mike Lesk 

## Diversity: Distrust all claims for “one true way”.

> Nobody is smart enough to optimize for everything, nor to anticipate all the uses to which their software might be put. Designing rigid, closed software that won't talk to the rest of the world is an unhealthy form of arrogance. ...the Unix tradition [...] embraces multiple languages, open extensible systems, and customization hooks everywhere.

## Extensibility: Design for the future, because it will be here sooner than you think.

> Never assume you have the final answer. Therefore, leave room for your data formats and code to grow... Always, always either include a version number, or compose the format from self-contained, self-describing clauses in such a way that new clauses can be readily added and old ones dropped without confusing format-reading code. Make data layouts self-describing... When you design code, organize it so future developers will be able to plug new functions into the architecture without having to scrap and rebuild the architecture. Make the joints flexible, and put “If you ever need to...” comments in your code. When you design for the future, the sanity you save may be your own.
