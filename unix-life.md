# Basics of the Unix Philosophy for life

I rediscovered the eternal "Basics of the Unix Philosophy", buried in my files today. I immediately thought how good it would be to adapt a version for use as a political model or a way of being, and thought (as it often the case) "I'll make a repo for that"…

It's something I'd forgotten, but absorbed so internally I try to follow it in actual life, without even realising what I'm doing.

So (to adapt the first few from [Eric Raymond's version](http://www.catb.org/~esr/writings/taoup/html/))…

### Modularity: Write simple parts connected by simple language

> The only way to tackle complex issues that won't fall apart is to hold global complexity down — to foster simple parts connected by well-defined communication channels and understandable language, so most problems are local to a specific part and there's some hope of updating one without breaking the whole.

### Clarity: Clarity is better than cleverness

> Write policies as if the most important communication they have is not to the system but to the people who will implement, live them out and maintain them in future (including yourself). Making the key points graceful and clear... means they're less likely to be interpreted wrongly.

### Composition: Create systems to be connected to other programs

> To make systems composable, decouple them. A system at one end of a process should know only what is necessary about the processes of the system at the other end—it should not depend on it. It should be easy to replace one end with a newer, updated or different system without disturbing the other.

### Separation: Separate policy from implementation; separate idealism from action

> Policy and implementation tend to mutate at different timescales, with policy changing much faster than the ability to implement it. Political and social trends may come and go, but basic human needs, methods of implementation and psychology change very little.