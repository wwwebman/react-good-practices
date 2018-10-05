# React Good Practices Guide
## TL;DR
As a developers we do a lot of wrong things before we find "The Golden Fleece" of hight quality, good architecture, great performance. We try to figure out what is the best engineering solution for our aplication. When we start working on project most of us have [YAGNI][yagni] syndrome, someone [premature optimization][premature] problems, some devs may not be aware of [DRY-KISS-LESS][dry-kiss-less] and so on. If I am talking about you it's time to make you happy by answering on most of questions.

So, besides of general good practice principles mentioned above let's go more futher with real world examples:  

### General
#### Broken YAGNI principle === feature is not released :imp:
Have you ever considered why your development is slow? There are a lot of reasons, but one of the most popular is not applied **YAGNI** principle. 

**Example**: Let's imagine that you are working on some big React Component that includes a lot of logic, must cooperate with store, render tons of small components. You already done with some code. So, let's say you have  [Smart React.Component][smart] that is connected to store and a lot of functional components. It's works pretty nice, but it's not at all satisfactory for you, because in meantime you have read article aka '[functional component vs React.Component vs React.PureComponent?][fc-vs-cp]'. Guess what the next step most of us take? Exactly, refactoring and optimization!

Here is the place where [premature optimization][premature] is came!
"...We should forget about small efficiencies, say about 97% of the time: premature optimization is the root of all evil. Yet we should not pass up our opportunities in that critical 3%.". 

For sure, we have to learn deeply Reacts API, be aware of bad practices... But if our implementation is fit code style requirements, business requirement and haven't any critical perfomance issues - just deliver feature.

#### What :pill: we are recommend?
| #Teory  | #RealWorld  |
| ------------- | ------------- |
| | Understand business requrements |
| Split feature story | Smaller tickets |
| Research | Would be nice to do fast research before you start coding(maybe somebody already have solution you need) |
| [TDD][tdd] | If requirements are **clear** - start with test |
| Make it work | Code must work and fulfill buiseness requirements |
| Make it right | Сonfirm that code is readable, used React [best practices][best], [prevented anti-patterns][anti], not broken YAGNI, applied DRY-KISS-LESS, linter requirements are fulfilled and tests cover most of functionality (it prevents bugs and makes refactoring much easier in the future) |
| Check performance bottlenecks | [Prevent anti-patterns][anti]; if something going wrong with perfomance it makes sens to use [profiler][profiler]|
| Code Review fixes | Apply cooworkers remarks |
| Deliver feature | Merging and deploy |

[yagni]: https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it
[premature]: http://wiki.c2.com/?PrematureOptimization
[dry-kiss-less]: https://thefullstack.xyz/dry-yagni-kiss-tdd-soc-bdfu
[smart]: https://medium.com/@thejasonfile/dumb-components-and-smart-components-e7b33a698d43
[fc-vs-cp]: https://stackoverflow.com/a/40704083/5513804
[tdd]: https://pl.wikipedia.org/wiki/Test-driven_development
[best]: https://github.com/markerikson/react-redux-links/blob/master/react-architecture.md
[anti]: https://codeburst.io/how-to-not-react-common-anti-patterns-and-gotchas-in-react-40141fe0dcd
[profiler]: https://reactjs.org/docs/optimizing-performance.html
