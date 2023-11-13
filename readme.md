# Basics of the Unix Philosophy

> Be generous in what you accept, rigorous in what you emit.  
> —[Chapter 1](https://paulvanderlaken.com/2019/09/17/17-principles-of-unix-software-design/)

I rediscovered the timeless *Basics of the Unix Philosophy* buried in my files awhile ago, and immediately thought how good it would be to adapt them for use as a human rather than a machine. So I made a repo for it, because I’d absorbed the document internally and realised that I follow some of the principles in actual life without even thinking about it. So in the Unix spirit of sharing, here’s my attempt to translate these principles to human life.

---

Adapted from [Eric Raymond's version](http://www.catb.org/~esr/writings/taoup/html/) [and this version](https://www.arp242.net/the-art-of-unix-programming/)

From: [Chapter 1. Philosophy](http://www.faqs.org/docs/artu/ch01s06.html)

The Unix philosophy is not a formal design method. It wasn't handed down from the high fastnesses of theoretical computer science as a way to produce theoretically perfect software. Nor is it that perennial executive's mirage, some way to magically extract innovative but reliable software on too short a deadline from unmotivated, badly managed, and underpaid programmers.

The Unix philosophy (like successful folk traditions in other engineering disciplines) is bottom-up, not top-down. It is pragmatic and grounded in experience. It is not to be found in official methods and standards, but rather in the implicit half-reflexive knowledge, the expertise that the Unix culture transmits. It encourages a sense of proportion and skepticism — and shows both by having a sense of (often subversive) humor.

> "Write programs that do one thing and do it well. Write programs to work together. Write programs to handle text streams, because that is a universal interface."  <small>Doug McIlroy, inventor of Unix pipes and one of the founders of the Unix tradition, in Peter H. Salus. A Quarter-Century of Unix. Addison-Wesley. 1994. ISBN 0-201-54777-5.</small>

---

## Rule of:

**Modularity:** Write simple parts connected by clean interfaces.  
	The only way to write complex software that won't fall on its face is to hold its global complexity down — to build it out of simple parts connected by well-defined interfaces, so that most problems are local and you can have some hope of upgrading a part without breaking the whole.

**Clarity:** Clarity is better than cleverness.  
	write programs as if the most important communication they do is not to the computer that executes them but to the human beings who will read and maintain the source code in the future (including yourself). Code that is graceful and clear… is less likely to break

**Composition:** Design programs to be connected to other programs.  
	To make programs composable, make them independent. A program on one end of a text stream should care as little as possible about the program on the other end. It should be made easy to replace one end with a completely different implementation without disturbing the other.

**Separation:** Separate policy from mechanism; separate interfaces from engines.  
	policy and mechanism tend to mutate on different timescales, with policy changing much faster than mechanism. Fashions in the look and feel of GUI toolkits may come and go, but raster operations and compositing are forever.

**Simplicity:** Design for simplicity; add complexity only where you must.  
	encourage a software culture that knows that small is beautiful, that actively resists bloat and complexity: an engineering tradition that puts a high value on simple solutions, that looks for ways to break program systems up into small cooperating pieces, and that reflexively fights attempts to gussy up programs with a lot of chrome.

**Parsimony:** Write a big program only when it is clear by demonstration that nothing else will do.  
	‘Big’ = both large in volume of code and of internal complexity. Allowing programs to get large hurts maintainability. Because people are reluctant to throw away the visible product of lots of work, large programs invite overinvestment in approaches that are failed or suboptimal.

**Transparency:** Design for visibility to make inspection and debugging easier.  
	A software system is transparent when you can look at it and immediately understand what it is doing and how. It is discoverable when it has facilities for monitoring and display of internal state so that [it] not only functions well but can be seen to function well.

**Robustness:** Robustness is the child of transparency and simplicity.  
	Most software is fragile and buggy because most programs are too complicated for a human brain to understand all at once. When you can't reason correctly about the guts of a program, you can't be sure it's correct, and you can't fix it if it's broken. […] software… is simple when what is going on is uncomplicated enough for a human brain to reason about all the potential cases without strain.

**Representation:** Fold knowledge into data so program logic can be stupid and robust.  
	Data is more tractable than program logic. It follows that where you see a choice between complexity in data structures and complexity in code, choose the former. More: in evolving a design, you should actively seek ways to shift complexity from code to data. C's facility at manipulating pointers has encouraged the use of dynamically-modified reference structures at all levels of coding from the kernel upward. Simple pointer chases in such structures frequently do duties that implementations in other languages would instead have to embody in more elaborate procedures.

**Least Surprise:** In interface design, always do the least surprising thing.  
	the easiest programs to use … connect to the user's pre-existing knowledge. …your expected audience… may be end users, other programmers, or system administrators. What is least surprising can differ among these groups. It's often better to make things distinctly different than to make them almost the same.

**Silence:** When a program has nothing surprising to say, it should say nothing.  
	when a program has nothing interesting or surprising to say, it should shut up. Well-behaved Unix programs do their jobs unobtrusively, with a minimum of fuss and bother. …important information should not be mixed in with verbosity about internal program behavior.

**Repair:** When you must fail, fail noisily and as soon as possible.  
	It's best when software can cope with unexpected conditions by adapting to them, but the worst kinds of bugs are those in which the repair doesn't succeed and the problem quietly causes corruption that doesn't show up until much later. Therefore, write your software to cope with incorrect inputs and its own execution errors as gracefully as possible. But when it cannot, make it fail in a way that makes diagnosis of the problem as easy as possible. Design for generosity rather than compensating for inadequate standards with permissive implementations (e.g. HTML tag soup).

**Economy:** Programmer time is expensive; conserve it in preference to machine time.  
	If we took this maxim really seriously… most applications would be written in higher-level languages like Perl, Tcl, Python, Java, Lisp and even shell — languages that ease the programmer's burden by doing their own memory management. One other obvious way to conserve programmer time is to teach machines how to do more of the low-level work of programming. This leads to…

**Generation:** Avoid hand-hacking; write programs to write programs when you can.  
	Human beings are notoriously bad at sweating the details… any kind of hand-hacking of programs is a rich source of delays and errors. The simpler and more abstracted your program specification can be, the more likely it is that the human designer will have gotten it right. Generated code (at every level) is almost always cheaper and more reliable than hand-hacked. It pays to use code generators when they can raise the level of abstraction — that is, when the specification language for the generator is simpler than the generated code… (code generators are heavily used to automate error-prone detail work. Parser/lexer generators are the classic examples; makefile generators and GUI interface builders are newer ones.)

**Optimization:** Prototype before polishing. Get it working before you optimize it.  
	Kernighan & Plauger's; “90% of the functionality delivered now is better than 100% of it delivered never”. premature local optimization actually hinders global optimization (and hence reduces overall performance). A prematurely optimized portion of a design frequently interferes with changes that would have much higher payoffs across the whole design, so you end up with both inferior performance and excessively complex code. ‘Extreme programming' guru Kent Beck: “Make it run, then make it right, then make it fast”. …tune systematically, looking for the places where you can buy big performance wins with the smallest possible increases in local complexity.
	"it is much easier to judge whether a prototype does what you want than it is to read a long specification. I remember one development manager at Bellcore who fought against the “requirements” culture years before anybody talked about “rapid prototyping” or “agile development”. He wouldn't issue long specifications; he'd lash together some combination of shell scripts and awk code that did roughly what was needed, tell the customers to send him some clerks for a few days, and then have the customers come in and look at their clerks using the prototype and tell him whether or not they liked it. If they did, he would say “you can have it industrial strength so-many-months from now at such-and-such cost”. His estimates tended to be accurate, but he lost out in the culture to managers who believed that requirements writers should be in control of everything." - Mike Lesk 

**Diversity:** Distrust all claims for “one true way”.  
	Nobody is smart enough to optimize for everything, nor to anticipate all the uses to which their software might be put. Designing rigid, closed software that won't talk to the rest of the world is an unhealthy form of arrogance. …the Unix tradition […] embraces multiple languages, open extensible systems, and customization hooks everywhere.

**Extensibility:** Design for the future, because it will be here sooner than you think.  
	Never assume you have the final answer. Therefore, leave room for your data formats and code to grow… Always, always either include a version number, or compose the format from self-contained, self-describing clauses in such a way that new clauses can be readily added and old ones dropped without confusing format-reading code. …(make) data layouts self-describing… When you design code, organize it so future developers will be able to plug new functions into the architecture without having to scrap and rebuild the architecture. […] Make the joints flexible, and put “If you ever need to…” comments in your code. When you design for the future, the sanity you save may be your own.

All the philosophy really boils down to one iron law, the hallowed ‘KISS principle’ of master engineers everywhere: Keep It Simple, Stupid!

---

http://www.faqs.org/docs/artu/ch01s09.html

(don’t) rush into *coding* when you should be *thinking*: you’ll carelessly complicate when you should be relentlessly simplifying.

value your own time enough never to waste it. If someone has already solved a problem once, don’t let pride or politics suck you into solving it a second time rather than re-using. And never work harder than you have to; work smarter instead… Lean on your tools and automate everything you can.

Software design and implementation should be a joyous art, a kind of high-level play. If this attitude seems preposterous or vaguely embarrassing to you, stop and think; ask yourself what you've forgotten. To do the Unix philosophy right, you need to have (or recover) that attitude. You need to *care*. You need to *play*. You need to be willing to *explore*.
