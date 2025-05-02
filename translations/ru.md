<h1 align="center"><a href="https://hacker-laws.com" target="_blank">hacker-laws</a></h1>
<h4 align="center">🧠 Законы, теории, принципы и паттерны, которые полезно знать участникам разработки ИТ-продуктов.</h4>

---

<!-- vim-markdown-toc GFM -->

- [Введение](#введение)
- [Законы](#законы)
    - [Принцип 90–9–1 (правило 1%)](#принцип-9091-правило-1)
    - [Правило 90–90](#правило-9090)
    - [Закон Амдала](#закон-амдала)
    - [Теория разбитых окон](#теория-разбитых-окон)
    - [Закон Брукса](#закон-брукса)
    - [Теорема CAP / Теорема Брюера](#теорема-cap--теорема-брюера))
    - [Три закона Кларка](#три-закона-кларка)
    - [Закон Конвея](#закон-конвея)
    - [Закон Каннингема](#закон-каннингема)
    - [Число Данбара](#число-данбара)
    - [Эффект Даннинга — Крюгера](#эффект-даннинга--крюгера)
    - [Закон Фиттса](#закон-фиттса)
    - [Закон Галла](#закон-галла)
    - [Закон Гудхарта](#закон-гудхарта)
    - [Бритва Хэнлона](#бритва-хэнлона)
    - [Закон Хика / Закон Хика — Хаймана)](#закон-хика--закон-хика--хаймана)
    - [Закон Хофштадтера](#закон-хофштадтера)
    - [Закон Хатбера](#закон-хатбера)
    - [Цикл хайпа / Закон Амара](#цикл-хайпа--закон-амара))
    - [Закон Хайрама / Закон неявных интерфейсов)](#закон-хайрама--закон-неявных-интерфейсов)
    - [Модель вход-процесс-выход (IPO)](#модель-вход-процесс-выход-ipo))
    - [Закон Кернигана](#закон-кернигана)
    - [Закон Куми](#закон-куми)
    - [Закон Линуса](#закон-линуса)
    - [Закон Меткалфа](#закон-меткалфа)
    - [Закон Мура](#закон-мура)
    - [Закон Мерфи / Закон подлости](#закон-мерфи--закон-подлости)
    - [Бритва Оккама](#бритва-оккама)
    - [Закон Паркинсона](#закон-паркинсона)
    - [Преждевременная оптимизация](#преждевременная-оптимизация)
    - [Закон Патта](#закон-патта)
    - [Закон Рида](#закон-рида)
    - [Горький урок Ричарда Саттона](#горький-урок-ричарда-саттона)
    - [Эффект Рингельмана](#эффект-рингельмана)
    - [Закон сохранения сложности / Закон Теслера](#закон-сохранения-сложности--закон-теслера)
    - [Закон Деметры](#закон-деметры)
    - [Закон дырявых абстракций](#закон-дырявых-абстракций)
    - [Закон инструмента / Закон молотка / Золотой молоток / Молоток Маслоу](#закон-инструмента--закон-молотка--золотой-молоток--молоток-маслоу)
    - [Закон тривиальности](#закон-тривиальности)
    - [Философия Unix](#философия-unix)
    - [Правило бойскаута](#правило-бойскаута)
    - [Модель Spotify](#модель-spotify)
    - [Правило двух пицц](#правило-двух-пицц)
    - [Закон Тваймана](#закон-тваймана)
    - [Закон Уодлера](#закон-уодлера)
    - [Закон Уитона](#закон-уитона)
- [Принципы](#принципы)
    - [Все модели неверны / Закон Джорджа Бокса](#все-модели-неверны--закон-джорджа-бокса)
    - [Забор Честертона](#забор-честертона)
    - [Принцип Керкгоффса](#принцип-керкгоффса)
    - [Эффект Мёртвого моря](#эффект-мёртвого-моря)
    - [Принцип Дилберта](#принцип-дилберта)
    - [Закон Парето / Правило 80/20](#закон-парето--правило-8020)
    - [Принцип Ширки](#принцип-ширки)
    - [Принцип Питера](#принцип-питера)
    - [Принцип надежности / Закон Постела](#принцип-надежности--закон-постела)
    - [SOLID](#solid)
    - [Принцип единственной ответственности](#принцип-единственной-ответственности)
    - [Принцип открытости/закрытости](#принцип-открытостизакрытости)
    - [Принцип подстановки Лисков](#принцип-подстановки-лисков)
    - [Принцип разделения интерфейса](#принцип-разделения-интерфейса)
    - [Принцип инверсии зависимостей](#принцип-инверсии-зависимостей)
    - [DRY / Принцип «не повторяйся»](#dry--принцип-не-повторяйся)
    - [Принцип KISS](#принцип-kiss)
    - [YAGNI](#yagni)
    - [Заблуждения о распределённых вычислениях](#заблуждения-о-распределённых-вычислениях)
    - [Принцип наименьшего удивления](#принцип-наименьшего-удивления)
- [Литература](#литература)
- [Онлайн ресурсы](#онлайн-ресурсы)
- [PDF версия](#pdf-версия)
- [Подкаст](#подкаст)

<!-- vim-markdown-toc -->

## Введение

Существует много законов, которые люди обсуждают, говоря о разработке. В этом репозитории собраны ссылки и обзоры наиболее распространённых. Пожалуйста, делитесь им и присылайте PR'ы!

Предупреждение: этот репозиторий содержит объяснения некоторых законов, принципов и паттернов, но не _агитирует_ ни за один из них. Вопрос о том, стоит ли их применять, всегда будет предметом споров, и ответ на него в значительной степени зависит от того, над чем вы работаете.

## Законы

Законы могут быть как мнениями о неизбежном в мире разработки программного обеспечения так и ироничными замечаниями о неизбежных реалиях.

### Принцип 90–9–1 (правило 1%)

[Правило одного процента на Википедии](https://ru.wikipedia.org/wiki/Правило_одного_процента)

Правило описывает неравномерность участия интернет-аудитории в создании содержимого: 90% участников только потребляют контент, 9% редактируют или изменяют контент и только 1% участников создает контент.

Примеры из жизни:

- Исследование четырех социальных сетей в сфере здравоохранения, проведенное в 2014 году, показало, что 1% самых популярных пользователей создали 73% публикаций, на следующие 9% пришлось в среднем около 25%, а на оставшиеся 90% пришлось в среднем 2%. ([Источник (en)](https://www.jmir.org/2014/2/e33))

См. также:

- [Закон Парето / Правило 80/20](#закон-парето--правило-8020)

### Правило 90–90

[90-90 Rule on Wikipedia](https://en.wikipedia.org/wiki/Ninety%E2%80%93ninety_rule)

> The first 90 percent of the code accounts for the first 90 percent of the development time. The remaining 10 percent of the code accounts for the other 90 percent of the development time.

A wry reinterpretation of the [Pareto Principe (or 80-20 rule)](#закон-парето--правило-8020) that highlights the real-world challenges of completing engineering work. This sentiment is also echoed in [Hofstadter's Law](#hofstadters-law).

См. также:

- [Закон Хофштадтера](#закон-хофштадтера)
- [Закон Парето / Правило 80/20](#закон-парето--правило-8020)

### Закон Амдала

[Amdahl's Law on Wikipedia](https://en.wikipedia.org/wiki/Amdahl%27s_law)

> Amdahl's Law is a formula which shows the _potential speedup_ of a computational task which can be achieved by increasing the resources of a system. Normally used in parallel computing, it can predict the actual benefit of increasing the number of processors, which is limited by the parallelisability of the program.

Best illustrated with an example. If a program is made up of two parts, part A, which must be executed by a single processor, and part B, which can be parallelised, then we see that adding multiple processors to the system executing the program can only have a limited benefit. It can potentially greatly improve the speed of part B - but the speed of part A will remain unchanged.

The diagram below shows some examples of potential improvements in speed:

<img width="480px" alt="Diagram: Amdahl's Law" src="./images/amdahls_law.png" />


As can be seen, even a program which is 50% parallelisable will benefit very little beyond 10 processing units, whereas a program which is 95% parallelisable can still achieve significant speed improvements with over a thousand processing units.

As [Moore's Law](#закон-мура) slows, and the acceleration of individual processor speed slows, parallelisation is key to improving performance. Graphics programming is an excellent example - with modern Shader based computing, individual pixels or fragments can be rendered in parallel - this is why modern graphics cards often have many thousands of processing cores (GPUs or Shader Units).

См. также:

- [Закон Брукса](#закон-брукса)
- [Закон Мура](#закон-мура)

### Теория разбитых окон

[The Broken Windows Theory on Wikipedia](https://en.wikipedia.org/wiki/Broken_windows_theory)

The Broken Windows Theory suggests that visible signs of crime (or lack of care of an environment) lead to further and more serious crimes (or further deterioration of the environment).

This theory has been applied to software development, suggesting that poor quality code (or [Technical Debt](#TODO)) can lead to a perception that efforts to improve quality may be ignored or undervalued, thus leading to further poor quality code. This effect cascades leading to a great decrease in quality over time.

См. также:

- [Технический долг](#TODO)

Examples:

- [The Pragmatic Programming: Software Entropy](https://flylib.com/books/en/1.315.1.15/1/)
- [Coding Horror: The Broken Window Theory](https://blog.codinghorror.com/the-broken-window-theory/)
- [OpenSource: Joy of Programming - The Broken Window Theory](https://opensourceforu.com/2011/05/joy-of-programming-broken-window-theory/)

### Закон Брукса

[Brooks' Law on Wikipedia](https://en.wikipedia.org/wiki/Brooks%27s_law)

> Adding human resources to a late software development project makes it later.

This law suggests that in many cases, attempting to accelerate the delivery of a project which is already late, by adding more people, will make the delivery even later. Brooks is clear that this is an over-simplification, however, the general reasoning is that given the ramp-up time of new resources and the communication overheads, in the immediate short-term velocity decreases. Also, many tasks may not be divisible, i.e. easily distributed between more resources, meaning the potential velocity increase is also lower.

The common phrase in delivery "Nine women can't make a baby in one month" relates to Brooks' Law, in particular, the fact that some kinds of work are not divisible or parallelisable.

This is a central theme of the book '[The Mythical Man Month](#литература)'.

См. также:

- [Марши смерти](#todo)
- [Литература: Мифический человеко-месяц](#литература)

### Теорема CAP / Теорема Брюера

The CAP Theorem (defined by Eric Brewer) states that for a distributed data store only two out of the following three guarantees (at most) can be made:

- Consistency: when reading data, every request receives the _most recent_ data or an error is returned
- Availability: when reading data, every request receives _a non error response_, without the guarantee that it is the _most recent_ data
- Partition Tolerance: when an arbitrary number of network requests between nodes fail, the system continues to operate as expected

The core of the reasoning is as follows. It is impossible to guarantee that a network partition will not occur (see [The Fallacies of Distributed Computing](#заблуждения-о-распределённых-вычислениях)). Therefore in the case of a partition we can either cancel the operation (increasing consistency and decreasing availability) or proceed (increasing availability but decreasing consistency).

The name comes from the first letters of the guarantees (Consistency, Availability, Partition Tolerance). Note that it is very important to be aware that this does _not_ relate to [_ACID_](#TODO), which has a different definition of consistency. More recently, [PACELC](#TODO) theorem has been developed which adds constraints for latency and consistency when the network is _not_ partitioned (i.e. when the system is operating as expected).

Most modern database platforms acknowledge this theorem implicitly by offering the user of the database the option to choose between whether they want a highly available operation (which might include a 'dirty read') or a highly consistent operation (for example a 'quorum acknowledged write').

Real world examples:

- [Inside Google Cloud Spanner and the CAP Theorem](https://cloud.google.com/blog/products/gcp/inside-cloud-spanner-and-the-cap-theorem) - Goes into the details of how Cloud Spanner works, which appears at first to seem like a platform which has _all_ of the guarantees of CAP, but under the hood is essentially a CP system.

См. также:

- [ACID](#TODO)
- [Заблуждения о распределённых вычислениях](#заблуждения-о-распределённых-вычислениях)
- [PACELC](#TODO)

### Три закона Кларка

[Clarke's three laws on Wikipedia](https://en.wikipedia.org/wiki/Clarke's_three_laws)

Arthur C. Clarke, an british science fiction writer, formulated three adages that are known as Clarke's three laws. The third law is the best known and most widely cited.  

These so-called laws are:

- When a distinguished but elderly scientist states that something is possible, they are almost certainly right. When they state that something is impossible, they are very probably wrong.
- The only way of discovering the limits of the possible is to venture a little way past them into the impossible.
- Any sufficiently advanced technology is indistinguishable from magic.


### Закон Конвея

[Conway's Law on Wikipedia](https://en.wikipedia.org/wiki/Conway%27s_law)

This law suggests that the technical boundaries of a system will reflect the structure of the organisation. It is commonly referred to when looking at organisation improvements, Conway's Law suggests that if an organisation is structured into many small, disconnected units, the software it produces will be. If an organisation is built more around 'verticals' which are oriented around features or services, the software systems will also reflect this.

См. также:

- [Модель Spotify](#модель-spotify)

### Закон Каннингема

[Cunningham's Law on Wikipedia](https://en.wikipedia.org/wiki/Ward_Cunningham#Cunningham's_Law)

> The best way to get the right answer on the Internet is not to ask a question, it's to post the wrong answer.

According to Steven McGeady, Ward Cunningham advised him in the early 1980s: "The best way to get the right answer on the Internet is not to ask a question, it's to post the wrong answer." McGeady dubbed this Cunningham's law, though Cunningham denies ownership calling it a "misquote." Although originally referring to interactions on Usenet, the law has been used to describe how other online communities work (e.g., Wikipedia, Reddit, Twitter, Facebook).

See also:

- [XKCD 386: "Duty Calls"](https://xkcd.com/386/)

### Число Данбара

[Dunbar's Number on Wikipedia](https://en.wikipedia.org/wiki/Dunbar%27s_number)

"Dunbar's number is a suggested cognitive limit to the number of people with whom one can maintain stable social relationships— relationships in which an individual knows who each person is and how each person relates to every other person." There is some disagreement to the exact number. "... [Dunbar] proposed that humans can comfortably maintain only 150 stable relationships." He put the number into a more social context, "the number of people you would not feel embarrassed about joining uninvited for a drink if you happened to bump into them in a bar." Estimates for the number generally lay between 100 and 250.

Like stable relationships between individuals, a developer's relationship with a codebase takes effort to maintain. When faced with large complicated projects, or ownership of many projects, we lean on convention, policy, and modeled procedure to scale. Dunbar's number is not only important to keep in mind as an office grows, but also when setting the scope for team efforts or deciding when a system should invest in tooling to assist in modeling and automating logistical overhead. Putting the number into an engineering context, it is the number of projects (or normalized complexity of a single project) for which you would feel confident in joining an on-call rotation to support.

См. также:

- [Закон Конвея](#закон-конвея)


### Эффект Даннинга — Крюгера

[The Dunning-Kruger Effect on Wikipedia](https://en.wikipedia.org/wiki/Dunning%E2%80%93Kruger_effect)

> If you're incompetent, you can't know you're incompetent... The skills you need to produce a right answer are exactly the skills you need to recognize what a right answer is.
>
> ([David Dunning](https://en.wikipedia.org/wiki/David_Dunning))

The Dunning–Kruger effect is a theoretical cognitive bias which was described by David Dunning and Justin Kruger in a 1999 psychological study and paper. The study suggests that people with a low level of ability at a task are likely to overestimate their ability of the task. The proposed reason for this bias is that a sufficient _awareness_ of the complexity of a problem or domain is required for a person to be able to make an informed opinion of their capability to work in that domain.

The Dunning-Kruger effect has sometimes been used to describe a related, but not necessarily implied effect which could be described as "The less a person understands a domain, the more they are likely to believe they can easily solve problems in that domain, as they are more likely to see the domain as _simple_". This more general effect is highly relevant in technology. It would suggest that people who are less familiar with a domain, such as non-technical team members or less experienced team members, are more likely to _underestimate_ the effort required to solve a problem in this space.

As a person's understanding and experience in a domain grows, they may well encounter another effect, which is that they tend to _overestimate_ the ability of _others_ or _underestimate_ their own ability, as they are have become so experienced in the domain. In all cases these effects are _cognitive biases_. As with any bias, an understanding that it may be present will often be sufficient to help avoid the challenges — as when there is awareness of a bias, more inputs and opinions can be included to attempt to eliminate these biases. A closely related bias is that of [Illusory superiority](https://en.wikipedia.org/wiki/Illusory_superiority).

Real-world examples:


### Закон Фиттса

[Fitts' Law on Wikipedia](https://en.wikipedia.org/wiki/Fitts%27s_law)

Fitts' law predicts that the time required to move to a target area is a function of the distance to the target divided by the width of the target.

<img width="300px" alt="Diagram: Fitts Law" src="./images/Fitts_Law.svg" />


The consequences of this law dictate that when designing UX or UI, interactive elements should be as large as possible and the distance between the users attention area and interactive element should be as small as possible. This has consequences on design, such as grouping tasks that are commonly used with one another close.

It also formalises the concept of 'magic corners', the corners of the screen to which a user can 'sweep' their mouse to easily hit - which is where key UI elements can be placed. The Windows Start button is in a magic corner, making it easy to select, and as an interesting contrast, the MacOS 'close window' button is _not_ in a magic corner, making it hard to hit by mistake.

See also:

- [The information capacity of the human motor system in controlling the amplitude of movement.](https://www.semanticscholar.org/paper/The-information-capacity-of-the-human-motor-system-Fitts/634c9fde5f1c411e4487658ac738dcf18d98ea8d)

### Закон Галла

[Gall's Law on Wikipedia](https://en.wikipedia.org/wiki/John_Gall_(author)#Gall's_law)

> A complex system that works is invariably found to have evolved from a simple system that worked. A complex system designed from scratch never works and cannot be patched up to make it work. You have to start over with a working simple system.
>
> ([John Gall](https://en.wikipedia.org/wiki/John_Gall_(author)))

Gall's Law implies that attempts to _design_ highly complex systems are likely to fail. Highly complex systems are rarely built in one go, but evolve instead from more simple systems.

The classic example is the world-wide-web. In its current state, it is a highly complex system. However, it was defined initially as a simple way to share content between academic institutions. It was very successful in meeting these goals and evolved to become more complex over time.

См. также:

- [Принцип KISS (Keep It Simple, Stupid)](#принцип-kiss)

### Закон Гудхарта

[The Goodhart's Law on Wikipedia](https://en.wikipedia.org/wiki/Goodhart's_law)

> Any observed statistical regularity will tend to collapse once pressure is placed upon it for control purposes.
>
> _Charles Goodhart_

Also commonly referenced as:

> When a measure becomes a target, it ceases to be a good measure.
>
> _Marilyn Strathern_

The law states that the measure-driven optimizations could lead to devaluation of the measurement outcome itself. Overly selective set of measures ([KPIs](https://en.wikipedia.org/wiki/Performance_indicator)) blindly applied to a process results in distorted effect. People tend to optimize locally by "gaming" the system in order to satisfy particular metrics instead of paying attention to holistic outcome of their actions.

Real-world examples:
- Assert-free tests satisfy the code coverage expectation, despite the fact that the metric intent was to create well-tested software.
- Developer performance score indicated by the number of lines committed leads to unjustifiably bloated codebase.

See also:
- [Goodhart’s Law: How Measuring The Wrong Things Drive Immoral Behaviour](https://coffeeandjunk.com/goodharts-campbells-law/)
- [Dilbert on bug-free software](https://dilbert.com/strip/1995-11-13)

### Бритва Хэнлона

[Hanlon's Razor on Wikipedia](https://en.wikipedia.org/wiki/Hanlon%27s_razor)

> Never attribute to malice that which is adequately explained by stupidity.
>
> Robert J. Hanlon

This principle suggests that actions resulting in a negative outcome were not a result of ill will. Instead the negative outcome is more likely attributed to those actions and/or the impact being not fully understood.

### Закон Хика / Закон Хика — Хаймана

[Hick's law on Wikipedia](https://en.wikipedia.org/wiki/Hick%27s_law)

> Decision time grows logarithmically with the number of options you can choose from.
>
> William Edmund Hick and Ray Hyman

In the equation below, `T` is the time to make a decision, `n` is the number of options, and `b` is a constant which is determined by analysis of the data.

![Hicks law](./images/hicks_law.svg)


This law only applies when the number of options is _ordered_, for example, alphabetically. This is implied in the base two logarithm - which implies the decision maker is essentially performing a _binary search_. If the options are not well ordered, experiments show the time taken is linear.

This is has significant impact in UI design; ensuring that users can easily search through options leads to faster decision making.

A correlation has also been shown in Hick's Law between IQ and reaction time as shown in [Speed of Information Processing: Developmental Change and Links to Intelligence](https://www.sciencedirect.com/science/article/pii/S0022440599000369).

См. также:

- [Закон Фиттса](#закон-фиттса)

### Закон Хофштадтера

[Hofstadter's Law on Wikipedia](https://en.wikipedia.org/wiki/Hofstadter%27s_law)

> It always takes longer than you expect, even when you take into account Hofstadter's Law.
>
> (Douglas Hofstadter)

You might hear this law referred to when looking at estimates for how long something will take. It seems a truism in software development that we tend to not be very good at accurately estimating how long something will take to deliver.

This is from the book '[Gödel, Escher, Bach: An Eternal Golden Braid](#литература)'.

См. также:

- [Литература: Гёдель, Эшер, Бах: эта бесконечная гирлянда](#литература)

### Закон Хатбера

[Hutber's Law on Wikipedia](https://en.wikipedia.org/wiki/Hutber%27s_law)

> Improvement means deterioration.
>
> ([Patrick Hutber](https://en.wikipedia.org/wiki/Patrick_Hutber))

This law suggests that improvements to a system will lead to deterioration in other parts, or it will hide other deterioration, leading overall to a degradation from the current state of the system.

For example, a decrease in response latency for a particular end-point could cause increased throughput and capacity issues further along in a request flow, affecting an entirely different sub-system.

### Цикл хайпа / Закон Амара

[The Hype Cycle on Wikipedia](https://en.wikipedia.org/wiki/Hype_cycle)

> We tend to overestimate the effect of a technology in the short run and underestimate the effect in the long run.
>
> (Roy Amara)

The Hype Cycle is a visual representation of the excitement and development of technology over time, originally produced by Gartner. It is best shown with a visual:

![The Hype Cycle](./images/gartner_hype_cycle.png)


In short, this cycle suggests that there is typically a burst of excitement around new technology and its potential impact. Teams often jump into these technologies quickly, and sometimes find themselves disappointed with the results. This might be because the technology is not yet mature enough, or real-world applications are not yet fully realised. After a certain amount of time, the capabilities of the technology increase and practical opportunities to use it increase, and teams can finally become productive. Roy Amara's quote sums this up most succinctly - "We tend to overestimate the effect of a technology in the short run and underestimate in the long run".

### Закон Хайрама / Закон неявных интерфейсов

[Hyrum's Law Online](http://www.hyrumslaw.com/)

> With a sufficient number of users of an API,
> it does not matter what you promise in the contract:
> all observable behaviours of your system
> will be depended on by somebody.
>
> (Hyrum Wright)


См. также:

- [Закон дырявых абстракций](#закон-дырявых-абстракций)
- [XKCD 1172](https://xkcd.com/1172/)

### Модель вход-процесс-выход (IPO)

[Input–Process–Output on Wikipedia](https://en.wikipedia.org/wiki/IPO_model)

Systems can be incredibly complex, but can typically be broken down into smaller parts that follow a simple pattern:

1. Input is provided
2. Some kind of processing or transformation is performed
3. Output is returned

A sort function in a programming language or system could be a classic example of the IPO pattern; where arbitrary input is sorted based on a predicate and returned back. A web server could be modelled as an IPO system, where HTTP requests are transformed into HTTP responses. A highly complex Generative AI system could likewise be modelled in this way, with user input being passed through a complex model and a response being generated.

The IPO pattern is present in different forms across almost all technological domains, from [functional programming](https://en.wikipedia.org/wiki/Functional_programming) languages that explicitly follow IPO patterns to [The Unix Philosophy](#философия-unix), which suggests that highly complex systems can be built by chaining together many simple IPO programs.

См. также:

- [Философия Unix](#философия-unix)

### Закон Кернигана

> Debugging is twice as hard as writing the code in the first place. Therefore, if you write the code as cleverly as possible, you are, by definition, not smart enough to debug it.
>
> (Brian Kernighan)

Kernighan's Law is named for [Brian Kernighan](https://en.wikipedia.org/wiki/Brian_Kernighan) and derived from a quote from Kernighan and Plauger's book [The Elements of Programming Style](https://en.wikipedia.org/wiki/The_Elements_of_Programming_Style):

> Everyone knows that debugging is twice as hard as writing a program in the first place. So if you're as clever as you can be when you write it, how will you ever debug it?

While hyperbolic, Kernighan's Law makes the argument that simple code is to be preferred over complex code, because debugging any issues that arise in complex code may be costly or even infeasible.

См. также:

- [Принцип KISS](#принцип-kiss)
- [Философия Unix](#философия-unix)
- [Бритва Оккама](#бритва-оккама)

### Закон Куми

[Koomey's Law on Wikipedia](https://en.wikipedia.org/wiki/Koomey%27s_law)

> ...at a fixed computing load, the amount of battery you need will fall by a factor of two every year and a half.
>
> (Jonathan Koomey)

In 2010 Professor Jonathan Koomey discovered that the trend in number of computations per joule of energy dissipated had been remarkably stable. This trend became known as Koomey's Law - that the amount of battery needed for a given computing load would half each 2.5 years.

Koomey performed a follow-up analysis in 2010 and found that this trend had slowed, similar to how [Moore's Law](#закон-мура) had slowed. This seemed to be related to limitations around how small transistors can be made, as well as [Dennard Scaling](https://en.wikipedia.org/wiki/Dennard_scaling).

См. также:

- [Закон Мура](#закон-мура)
- [Dennard Scaling](https://en.wikipedia.org/wiki/Dennard_scaling)

### Закон Линуса

[Linus's Law on Wikipedia](https://en.wikipedia.org/wiki/Linus%27s_law)

> Given enough eyeballs, all bugs are shallow.
>
> _Eric S. Raymond_

This law simply states that the more people who can see a problem, the higher the likelihood that someone will have seen and solved the problem before, or something very similar.

Although it was originally used to describe the value of open-source models for projects it can be accepted for any kind of software project. It can also be extended to processes - more code reviews, more static analysis and multi-disciplined test processes will make the problems more visible and easy to identify.

A more formal statement can be:

> Given a large enough beta-tester and co-developer base, almost every problem will be characterized quickly and can be solved by someone who has encountered a similar problem before.

This law was named in honour of [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds) in Eric S. Raymond's book "[The Cathedral and the Bazaar](https://en.wikipedia.org/wiki/The_Cathedral_and_the_Bazaar)".

### Закон Меткалфа

[Metcalfe's Law on Wikipedia](https://en.wikipedia.org/wiki/Metcalfe's_law)

> In network theory, the value of a system grows as approximately the square of the number of users of the system.

This law is based on the number of possible pairwise connections within a system and is closely related to [Reed's Law](#закон-рида). Odlyzko and others have argued that both Reed's Law and Metcalfe's Law overstate the value of the system by not accounting for the limits of human cognition on network effects; see [Dunbar's Number](#число-данбара).

См. также:

- [Закон Рида](#закон-рида)
- [Число Данбара](#число-данбара)

### Закон Мура

[Moore's Law on Wikipedia](https://en.wikipedia.org/wiki/Moore%27s_law)

> The number of transistors in an integrated circuit doubles approximately every two years.

Often used to illustrate the sheer speed at which semiconductor and chip technology has improved, Moore's prediction has proven to be highly accurate over from the 1970s to the late 2000s. In more recent years, the trend has changed slightly, partly due to [physical limitations on the degree to which components can be miniaturised](https://en.wikipedia.org/wiki/Quantum_tunnelling). However, advancements in parallelisation, and potentially revolutionary changes in semiconductor technology and quantum computing may mean that Moore's Law could continue to hold true for decades to come.

См. также:

- [Закон Куми](#закон-куми)

### Закон Мерфи / Закон подлости

[Murphy's Law on Wikipedia](https://en.wikipedia.org/wiki/Murphy%27s_law)

> Anything that can go wrong will go wrong.

Related to [Edward A. Murphy, Jr](https://en.wikipedia.org/wiki/Edward_A._Murphy_Jr.) _Murphy's Law_ states that if a thing can go wrong, it will go wrong.

This is a common adage among developers. Sometimes the unexpected happens when developing, testing or even in production. This can also be related to the (more common in British English) _Sod's Law_:

> If something can go wrong, it will, at the worst possible time.

These 'laws' are generally used in a comic sense. However, phenomena such as [_Confirmation Bias_](#TODO) and [_Selection Bias_](#TODO) can lead people to perhaps over-emphasise these laws (the majority of times when things work, they go unnoticed, failures however are more noticeable and draw more discussion).

См. также:

- [Предвзятость подтверждения](#TODO)
- [Систематическая ошибка отбора](#TODO)

### Бритва Оккама

[Occam's Razor on Wikipedia](https://en.wikipedia.org/wiki/Occam's_razor)

> Entities should not be multiplied without necessity.
>
> William of Ockham

Occam's razor says that among several possible solutions, the most likely solution is the one with the least number of concepts and assumptions. This solution is the simplest and solves only the given problem, without introducing accidental complexity and possible negative consequences.

See also:

- [YAGNI](#yagni)
- [No Silver Bullet: Accidental Complexity and Essential Complexity](https://en.wikipedia.org/wiki/No_Silver_Bullet)

Example:

- [Lean Software Development: Eliminate Waste](https://en.wikipedia.org/wiki/Lean_software_development#Eliminate_waste)

### Закон Паркинсона

[Parkinson's Law on Wikipedia](https://en.wikipedia.org/wiki/Parkinson%27s_law)

> Work expands so as to fill the time available for its completion.

In its original context, this Law was based on studies of bureaucracies. It may be pessimistically applied to software development initiatives, the theory being that teams will be inefficient until deadlines near, then rush to complete work by the deadline, thus making the actual deadline somewhat arbitrary.


См. также:

- [Закон Хофштадтера](#закон-хофштадтера)

### Преждевременная оптимизация

[Premature Optimization on WikiWeb](http://wiki.c2.com/?PrematureOptimization)

> Premature optimization is the root of all evil.
>
> [(Donald Knuth)](https://twitter.com/realdonaldknuth?lang=en)


However, _Premature Optimization_ can be defined (in less loaded terms) as optimizing before we know that we need to.

### Закон Патта

[Putt's Law on Wikipedia](https://en.wikipedia.org/wiki/Putt%27s_Law_and_the_Successful_Technocrat)

> Technology is dominated by two types of people, those who understand what they do not manage and those who manage what they do not understand.

Putt's Law is often followed by Putt's Corollary:

> Every technical hierarchy, in time, develops a competence inversion.

These statements suggest that due to various selection criteria and trends in how groups organise, there will be a number of skilled people at working levels of a technical organisations, and a number of people in managerial roles who are not aware of the complexities and challenges of the work they are managing. This can be due to phenomena such as [The Peter Principle](#принцип-питера) or [The Dilbert Principle](#принцип-дилберта).

However, it should be stressed that Laws such as this are vast generalisations and may apply to _some_ types of organisations, and not apply to others.

См. также:

- [Принцип Питера](#принцип-питера)
- [Принцип Дилберта](#принцип-дилберта)

### Закон Рида

[Reed's Law on Wikipedia](https://en.wikipedia.org/wiki/Reed's_law)

> The utility of large networks, particularly social networks, scales exponentially with the size of the network.

This law is based on graph theory, where the utility scales as the number of possible sub-groups, which is faster than the number of participants or the number of possible pairwise connections. Odlyzko and others have argued that Reed's Law overstates the utility of the system by not accounting for the limits of human cognition on network effects; see [Dunbar's Number](#число-данбара).

См. также:

- [Закон Меткалфа](#закон-меткалфа)
- [Число Данбара](#число-данбара)

### Горький урок Ричарда Саттона

[The Bitter Lesson by Richard S. Sutton](http://www.incompleteideas.net/IncIdeas/BitterLesson.html)

> The biggest lesson that can be read from 70 years of AI research is that general methods that leverage computation are ultimately the most effective, and by a large margin.
>
> Richard S. Sutton (2019)

The "Bitter Lesson", stated by [Rich S. Sutton](https://en.wikipedia.org/wiki/Richard_S._Sutton), says that scale (in terms of both data and computational power) has driven the most significant advancements in AI research, rather than the intricacies of the research methods themselves.

He goes on to suggest that this indicates we should stop trying to build simplified (or even complex) models of the mind as history has shown that these have always in the long term been failures compared to (as an example) scaling the capacity of neural networks and applying existing methods such as convolution.

### Эффект Рингельмана

[The Ringelmann effect on Wikipedia](https://en.wikipedia.org/wiki/Ringelmann_effect)

The Ringelmann Effect is the tendency of an individual to become increasingly inefficient as more and more people are involved in a task. In other words, as more individuals are added to a team, the more the average individual performance decreases. Multiple causes are believed to be at work, including loss of motivation ("[social loafing](https://en.wikipedia.org/wiki/Social_loafing)") and challenges related to coordination.

См. также:

- [Закон Брукса](#закон-брукса)

### Закон сохранения сложности / Закон Теслера

[The Law of Conservation of Complexity on Wikipedia](https://en.wikipedia.org/wiki/Law_of_conservation_of_complexity)

This law states that there is a certain amount of complexity in a system which cannot be reduced.

Some complexity in a system is 'inadvertent'. It is a consequence of poor structure, mistakes, or just bad modeling of a problem to solve. Inadvertent complexity can be reduced (or eliminated). However, some complexity is 'intrinsic' as a consequence of the complexity inherent in the problem being solved. This complexity can be moved, but not eliminated.

One interesting element to this law is the suggestion that even by simplifying the entire system, the intrinsic complexity is not reduced, it is _moved to the user_, who must behave in a more complex way.

### Закон Деметры

[The Law of Demeter on Wikipedia](https://en.wikipedia.org/wiki/Law_of_Demeter)

> Don't talk to strangers.

The Law of Demeter, also known as "The Principle of Least Knowledge" is a principle for software design, particularly relevant in object orientated languages.

It states that a unit of software should talk only to its immediate collaborators. An object `A` with a reference to object `B` can call its methods, but if `B` has a reference to object `C`, `A` should not call `C`s methods. So, if `C` has a `doThing()` method, `A` should not invoke it directly; `B.getC().doThis()`.

Following this principal limits the scope of changes, making them easier and safer in future.

### Закон дырявых абстракций

[The Law of Leaky Abstractions on Joel on Software](https://www.joelonsoftware.com/2002/11/11/the-law-of-leaky-abstractions/)

> All non-trivial abstractions, to some degree, are leaky.
>
> ([Joel Spolsky](https://twitter.com/spolsky))

This law states that abstractions, which are generally used in computing to simplify working with complicated systems, will in certain situations 'leak' elements of the underlying system, this making the abstraction behave in an unexpected way.


The example above can become more complex when _more_ abstractions are introduced. The Linux operating system allows files to be accessed over a network but represented locally as 'normal' files. This abstraction will 'leak' if there are network failures. If a developer treats these files as 'normal' files, without considering the fact that they may be subject to network latency and failures, the solutions will be buggy.

The article describing the law suggests that an over-reliance on abstractions, combined with a poor understanding of the underlying processes, actually makes dealing with the problem at hand _more_ complex in some cases.

См. также:

- [Закон Хайрама / Закон неявных интерфейсов)](#закон-хайрама--закон-неявных-интерфейсов)

Real-world examples:

- [Photoshop Slow Startup](https://forums.adobe.com/thread/376152) - an issue I encountered in the past. Photoshop would be slow to startup, sometimes taking minutes. It seems the issue was that on startup it reads some information about the current default printer. However, if that printer is actually a network printer, this could take an extremely long time. The _abstraction_ of a network printer being presented to the system similar to a local printer caused an issue for users in poor connectivity situations.

### Закон инструмента / Закон молотка / Золотой молоток / Молоток Маслоу

[The Law of the Instrument](https://en.wikipedia.org/wiki/Law_of_the_instrument)

> I call it the law of the instrument, and it may be formulated as follows: Give a small boy a hammer, and he will find that everything he encounters needs pounding.
>
> _Abraham Kaplan_

> If all you have is a hammer, everything looks like a nail.
>
> _Abraham Maslow_

In the context of computer programming, this law suggests that people tend to use tools that are familiar with, rather than the best possible tool. This over-reliance on a familiar tool is an anti-pattern referred to as 'the golden hammer'.

See also:

- [Avoiding the law of the instrument](https://josemdev.com/avoiding-the-law-of-the-instrument/)
- [Anti-Pattern - The Golden Hammer](https://archive.org/details/antipatternsrefa0000unse/page/111/mode/2up)

### Закон тривиальности

[The Law of Triviality on Wikipedia](https://en.wikipedia.org/wiki/Law_of_triviality)

This law suggests that groups will give far more time and attention to trivial or cosmetic issues rather than serious and substantial ones.

The common fictional example used is that of a committee approving plans for nuclear power plant, who spend the majority of their time discussing the structure of the bike shed, rather than the far more important design for the power plant itself. It can be difficult to give valuable input on discussions about very large, complex topics without a high degree of subject matter expertise or preparation. However, people want to be seen to be contributing valuable input. Hence a tendency to focus too much time on small details, which can be reasoned about easily, but are not necessarily of particular importance.

The fictional example above led to the usage of the term 'Bike Shedding' as an expression for wasting time on trivial details. A related term is '[Yak Shaving](https://en.wiktionary.org/wiki/yak_shaving),' which connotes a seemingly irrelevant activity that is part of a long chain of prerequisites to the main task.

### Философия Unix

[The Unix Philosophy on Wikipedia](https://en.wikipedia.org/wiki/Unix_philosophy)

The Unix Philosophy is that software components should be small, and focused on doing one specific thing well. This can make it easier to build systems by composing together small, simple, well-defined units, rather than using large, complex, multi-purpose programs.

Modern practices like 'Microservice Architecture' can be thought of as an application of this law, where services are small, focused and do one specific thing, allowing complex behaviour to be composed of simple building blocks.

### Правило бойскаута

[The Scout Rule on O'Reilly](https://www.oreilly.com/library/view/97-things-every/9780596809515/ch08.html)

> Always leave the code better than you found it.
>
> (Robert C. Martin (Uncle Bob))

Based on the "Scout Rule", which is "always leave the campground cleaner than you found it", the Scout Rule in programming is simply "always leave the code cleaner than you found it".

This was introduced in the first chapter of the book [Clean Code](https://www.goodreads.com/book/show/3735293-clean-code) by Bob Martin. The rule suggests that developers should perform 'optimistic refactoring', which means to endeavour to improve the overall quality of the code when you work on it. If you see a mistake, attempt to fix it or clean it up. However, when making changes to code which seems incorrect, it may be worth remembering [Chesterton's Fence](#забор-честертона)!

См. также:

- [Литература: Чистый код. Создание, анализ и рефакторинг](#литература)
- [Забор Честертона](#забор-честертона)
- [Теория разбитых окон](#теория-разбитых-окон)

https://www.amazon.sg/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882

### Модель Spotify

[The Spotify Model on Spotify Labs](https://labs.spotify.com/2014/03/27/spotify-engineering-culture-part-1/)

The Spotify Model is an approach to team and organisation structure which has been popularised by 'Spotify'. In this model, teams are organised around features, rather than technologies.

The Spotify Model also popularises the concepts of Tribes, Guilds, Chapters, which are other components of their organisation structure.

Members of the organisation have described that the actual meaning of these groups changes, evolves and is an on-going experiment. The fact that the model is a _process in motion_, rather than a fixed model continues to lead to varying interpretations of the structure, which may be based on presentations given by employees at conferences. This means 'snapshots' may be 're-packaged' by third parties as a _fixed structure_, with the fact that the model is dynamic being lost.

### Правило двух пицц

> If you can't feed a team with two pizzas, it's too large.
>
> (Jeff Bezos)

This rule suggests that regardless of the size of the company, teams should be small enough to be fed by two pizzas. Attributed to Jeff Bezos and Amazon, this belief suggests that large teams are inherently inefficient. This is supported by the fact that as the team size increases linearly, the links between people increases quadratically; thus the cost of coordinating and communicating also grows quadratically. If this cost of coordination is essentially overhead, then smaller teams should be preferred.

The number of links between people can be expressed as `n(n-1)/2` where n = number of people.

<img width="200px" alt="Complete graph; Links between people" src="./images/complete_graph.png" />

### Закон Тваймана

[Twyman's Law on Wikipedia](https://en.wikipedia.org/wiki/Twyman%27s_law)

> The more unusual or interesting the data, the more likely they are to have been the result of an error of one kind or another.

This law suggests that when there are particularly unusual data points, it is more likely that they are the result of errors or manipulation. For example, if a dataset of long-jump results from a sporting event showed a maximum value of 20 meters (more than twice the world record), it is more likely to be due to an error (such as recording a value in feet rather than meters) than due to an unusually long jump. It is also more likely in this case that the results could have been manipulated.

См. также:

- [Стандарт Сагана](#TODO)

### Закон Уодлера

[Wadler's Law on wiki.haskell.org](https://wiki.haskell.org/Wadler's_Law)

> In any language design, the total time spent discussing a feature in this list is proportional to two raised to the power of its position.
>
> 0. Semantics
> 1. Syntax
> 2. Lexical syntax
> 3. Lexical syntax of comments
>
> (In short, for every hour spent on semantics, 8 hours will be spent on the syntax of comments).

Similar to [The Law of Triviality](#закон-тривиальности), Wadler's Law states what when designing a language, the amount of time spent on language structures is disproportionately high in comparison to the importance of those features.

См. также:

- [Закон тривиальности](#закон-тривиальности)

### Закон Уитона

[The Link](http://www.wheatonslaw.com/)

[The Official Day](https://dontbeadickday.com/)

> Don't be a dick.
>
> _Wil Wheaton_

Coined by Wil Wheaton (Star Trek: The Next Generation, The Big Bang Theory), this simple, concise, and powerful law aims for an increase in harmony and respect within a professional organization. It can be applied when speaking with coworkers, performing code reviews, countering other points of view, critiquing, and in general, most professional interactions humans have with each other.

## Принципы

Принципы, как правило, представляют собой рекомендации, касающиеся дизайна.

### Все модели неверны / Закон Джорджа Бокса

[All Models Are Wrong](https://en.wikipedia.org/wiki/All_models_are_wrong)

> All models are wrong, but some are useful.
>
> _George Box_

This principle suggests that all models of systems are flawed, but that as long as they are not _too_ flawed they may be useful. This principle has its roots in statistics but applies to scientific and computing models as well.

A fundamental requirement of most software is to model a system of some kind. Regardless of whether the system being modeled is a computer network, a library, a graph of social connections or any other kind of system, the designer will have to decide an appropriate level of detail to model. Excessive detail may lead to too much complexity, too little detail may prevent the model from being functional.

См. также:

- [Закон дырявых абстракций](#закон-дырявых-абстракций)

### Забор Честертона

[Chesterton's Fence on Wikipedia](https://en.wikipedia.org/wiki/Wikipedia:Chesterton%27s_fence)

> Reforms should not be made until the reasoning behind the existing state of affairs is understood.

This principle is relevant in software engineering when removing technical debt. Each line of a program was originally written by someone for some reason. Chesterton's Fence suggests that one should try to understand the context and meaning of the code fully, before changing or removing it, even if at first glance it seems redundant or incorrect.

The name of this principle comes from a story by [G.K. Chesterton](https://en.wikipedia.org/wiki/G._K._Chesterton). A man comes across a fence crossing the middle of the road. He complains to the mayor that this useless fence is getting in the way, and asks to remove it. The mayor asks why the fence is there in the first place. When the man says he doesn't know, the mayor says, "If you don't know its purpose, I certainly won't let you remove it. Go and find out the use of it, and then I may let you destroy it."

### Принцип Керкгоффса

[Kerckhoffs's principle on Wikipedia](https://en.wikipedia.org/wiki/Kerckhoffs%27s_principle)

> "...design your system assuming that your opponents know it in detail."
>
> _Steven M. Bellovin's formulation of Kerckhoff's Principle_

This principle of cryptography was an axiom created by cryptographer Auguste Kerckhoffs. He stated that a cryptosystem should be secure, even if everything about the system, except the key, is public knowledge. Not to be confused with [_"security through obscurity"_](#todo).

The gold standard for any secret-keeping system is that implementation details should be publicly distributed, without sacrificing or compromising security of said system.

The history of cryptography has shown that open discussion and analysis of cryptographic systems leads to better and more secure systems - as researchers are able to test for and expose potential vulnerabilities.

См. также:

- [Максима Шеннона / Принципом Керкгоффса](#todo)

### Эффект Мёртвого моря

[The Dead Sea Effect on Bruce F. Webster](http://brucefwebster.com/2008/04/11/the-wetware-crisis-the-dead-sea-effect/)

> "... [T]he more talented and effective IT engineers are the ones most likely to leave - to evaporate ... [those who tend to] remain behind [are] the 'residue' — the least talented and effective IT engineers."
>
> _Bruce F. Webster_

The "Dead Sea Effect" suggests that in any organisation, the skills/talent/efficacy of engineers is often inversely proportional to their time in the company.

Typically, highly skilled engineers find it easy to gain employment elsewhere and are the first to do so. Engineers who have obsolete or weak skills will tend to remain with the company, as finding employment elsewhere is difficult. This is particularly pronounced if they have gained incremental pay rises over their time in the company, as it can be challenging to get equivalent remuneration elsewhere.

### Принцип Дилберта

[The Dilbert Principle on Wikipedia](https://en.wikipedia.org/wiki/Dilbert_principle)

> Companies tend to systematically promote incompetent employees to management to get them out of the workflow.
>
> _Scott Adams_

A management concept developed by Scott Adams (creator of the Dilbert comic strip), the Dilbert Principle is inspired by [The Peter Principle](#принцип-питера). Under the Dilbert Principle, employees who were never competent are promoted to management in order to limit the damage they can do. Adams first explained the principle in a 1995 Wall Street Journal article, and expanded upon it in his 1996 business book, [The Dilbert Principle](#литература).

См. также:

- [Принцип Питера](#принцип-питера)
- [Закон Патта](#закон-патта)

### Закон Парето / Правило 80/20

[The Pareto Principle on Wikipedia](https://en.wikipedia.org/wiki/Pareto_principle)

> Most things in life are not distributed evenly.

The Pareto Principle suggests that in some cases, the majority of results come from a minority of inputs:

- 80% of a certain piece of software can be written in 20% of the total allocated time (conversely, the hardest 20% of the code takes 80% of the time)
- 20% of the effort produces 80% of the result
- 20% of the work creates 80% of the revenue
- 20% of the bugs cause 80% of the crashes
- 20% of the features cause 80% of the usage

In the 1940s American-Romanian engineer Dr. Joseph Juran, who is widely credited with being the father of quality control, [began to apply the Pareto principle to quality issues](https://en.wikipedia.org/wiki/Joseph_M._Juran).

This principle is also known as: The 80/20 Rule, The Law of the Vital Few, and The Principle of Factor Sparsity.

Real-world examples:

- In 2002 Microsoft reported that by fixing the top 20% of the most-reported bugs, 80% of the related errors and crashes in windows and office would become eliminated ([Reference](https://www.crn.com/news/security/18821726/microsofts-ceo-80-20-rule-applies-to-bugs-not-just-features.htm)).

### Принцип Ширки

[The Shirky Principle explained](https://kk.org/thetechnium/the-shirky-prin/)

> Institutions will try to preserve the problem to which they are the solution.
>
> _Clay Shirky_

The Shirky Principle suggests that complex solutions - a company, an industry, or a technology - can become so focused on the problem that they are solving, that they can inadvertently perpetuate the problem itself. This may be deliberate (a company striving to find new nuances to a problem which justify continued development of a solution), or inadvertent (being unable or unwilling to accept or build a solution which solves the problem completely or obviates it).

Related to:

- Upton Sinclair's famous line, _"It is difficult to get a man to understand something, when his salary depends upon his not understanding it!"_
- Clay Christensen's _The Innovator's Dilemma_

См. также:

- [Закон Парето / Правило 80/20](#закон-парето--правило-8020)

### Принцип Питера

[The Peter Principle on Wikipedia](https://en.wikipedia.org/wiki/Peter_principle)

> People in a hierarchy tend to rise to their "level of incompetence".
>
> _Laurence J. Peter_

A management concept developed by Laurence J. Peter, the Peter Principle observes that people who are good at their jobs are promoted, until they reach a level where they are no longer successful (their "level of incompetence"). At this point, as they are more senior, they are less likely to be removed from the organisation (unless they perform spectacularly badly) and will continue to reside in a role which they have few intrinsic skills at, as their original skills which made them successful are not necessarily the skills required for their new jobs.

This is of particular interest to engineers - who initially start out in deeply technical roles, but often have a career path which leads to _managing_ other engineers - which requires a fundamentally different skill set.

См. также:

- [Принцип Дилберта](#принцип-дилберта)
- [Закон Патта](#закон-патта)

### Принцип надежности / Закон Постела

[The Robustness Principle on Wikipedia](https://en.wikipedia.org/wiki/Robustness_principle)

> Be conservative in what you do, be liberal in what you accept from others.

Often applied in server application development, this principle states that what you send to others should be as minimal and conformant as possible, but you should aim to allow non-conformant input if it can be processed.

The goal of this principle is to build systems which are robust, as they can handle poorly formed input if the intent can still be understood. However, there are potentially security implications of accepting malformed input, particularly if the processing of such input is not well tested. These implications and other issues are described by Eric Allman in [The Robustness Principle Reconsidered](https://queue.acm.org/detail.cfm?id=1999945).

Allowing non-conformant input, in time, may undermine the ability of protocols to evolve as implementors will eventually rely on this liberality to build their features.

См. также:

- [Закон Хайрама / Закон неявных интерфейсов)](#закон-хайрама--закон-неявных-интерфейсов)

### SOLID

This is an acronym, which refers to:


These are key principles in [Object-Oriented Programming](#todo). Design principles such as these should be able to aid developers build more maintainable systems.

### Принцип единственной ответственности

[The Single Responsibility Principle on Wikipedia](https://en.wikipedia.org/wiki/Single_responsibility_principle)

> Every module or class should have a single responsibility only.

The first of the '[SOLID](#solid)' principles. This principle suggests that modules or classes should do one thing and one thing only. In more practical terms, this means that a single, small change to a feature of a program should require a change in one component only. For example, changing how a password is validated for complexity should require a change in only one part of the program.

Theoretically, this should make the code more robust, and easier to change. Knowing that a component being changed has a single responsibility only means that _testing_ that change should be easier. Using the earlier example, changing the password complexity component should only be able to affect the features which relate to password complexity. It can be much more difficult to reason about the impact of a change to a component which has many responsibilities.

См. также:

- [Объектно-ориентированное программирование](#todo)
- [SOLID](#solid)

### Принцип открытости/закрытости

[The Open/Closed Principle on Wikipedia](https://en.wikipedia.org/wiki/Open%E2%80%93closed_principle)

> Entities should be open for extension and closed for modification.

The second of the '[SOLID](#solid)' principles. This principle states that entities (which could be classes, modules, functions and so on) should be able to have their behaviour _extended_, but that their _existing_ behaviour should not be able to be modified.

As a hypothetical example, imagine a module which is able to turn a Markdown document into HTML. Now imagine there is a new syntax added to the Markdown specification, which adds support for mathematical equations. The module should be _open to extension_ to implement the new mathematics syntax. However, existing syntax implementations (like paragraphs, bullets, etc) should be _closed for modification_. They already work, we don't want people to change them.

This principle has particular relevance for object-oriented programming, where we may design objects to be easily extended, but would avoid designing objects which can have their existing behaviour changed in unexpected ways.

См. также:

- [Объектно-ориентированное программирование](#todo)
- [SOLID](#solid)

### Принцип подстановки Лисков

[The Liskov Substitution Principle on Wikipedia](https://en.wikipedia.org/wiki/Liskov_substitution_principle)

> It should be possible to replace a type with a subtype, without breaking the system.

The third of the '[SOLID](#solid)' principles. This principle states that if a component relies on a type, then it should be able to use subtypes of that type, without the system failing or having to know the details of what that subtype is.

As an example, imagine we have a method which reads an XML document from a structure which represents a file. If the method uses a base type 'file', then anything which derives from 'file' should be usable in the function. If 'file' supports seeking in reverse, and the XML parser uses that function, but the derived type 'network file' fails when reverse seeking is attempted, then the 'network file' would be violating the principle.

This principle has particular relevance for object-oriented programming, where type hierarchies must be modeled carefully to avoid confusing users of a system.

См. также:

- [Объектно-ориентированное программирование](#todo)
- [SOLID](#solid)

### Принцип разделения интерфейса

[The Interface Segregation Principle on Wikipedia](https://en.wikipedia.org/wiki/Interface_segregation_principle)

> No client should be forced to depend on methods it does not use.

The fourth of the '[SOLID](#solid)' principles. This principle states that consumers of a component should not depend on functions of that component which it doesn't actually use.

As an example, imagine we have a method which reads an XML document from a structure which represents a file. It only needs to read bytes, move forwards or move backwards in the file. If this method needs to be updated because an unrelated feature of the file structure changes (such as an update to the permissions model used to represent file security), then the principle has been invalidated. It would be better for the file to implement a 'seekable-stream' interface, and for the XML reader to use that.

This principle has particular relevance for object-oriented programming, where interfaces, hierarchies and abstract types are used to [minimise the coupling](#todo) between different components. [Duck typing](#todo) is a methodology which enforces this principle by eliminating explicit interfaces.

См. также:

- [Объектно-ориентированное программирование](#todo)
- [SOLID](#solid)
- [Утиная типизация](#todo)
- [Развязка](#todo)

### Принцип инверсии зависимостей

[The Dependency Inversion Principle on Wikipedia](https://en.wikipedia.org/wiki/Dependency_inversion_principle)

> High-level modules should not be dependent on low-level implementations.

The fifth of the '[SOLID](#solid)' principles. This principle states that higher-level orchestrating components should not have to know the details of their dependencies.

As an example, imagine we have a program which read metadata from a website. We would assume that the main component would have to know about a component to download the webpage content, then a component which can read the metadata. If we were to take dependency inversion into account, the main component would depend only on an abstract component which can fetch byte data, and then an abstract component which would be able to read metadata from a byte stream. The main component would not know about TCP/IP, HTTP, HTML, etc.

This principle is complex, as it can seem to 'invert' the expected dependencies of a system (hence the name). In practice, it also means that a separate orchestrating component must ensure the correct implementations of abstract types are used (e.g. in the previous example, _something_ must still provide the metadata reader component a HTTP file downloader and HTML meta tag reader). This then touches on patterns such as [Inversion of Control](#todo) and [Dependency Injection](#todo).

См. также:

- [Объектно-ориентированное программирование](#todo)
- [SOLID](#solid)
- [Инверсия управления](#todo)
- [Внедрение зависимости](#todo)

### DRY / Принцип «не повторяйся»

[The DRY Principle on Wikipedia](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)

> Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.

DRY is an acronym for _Don't Repeat Yourself_. This principle aims to help developers reducing the repetition of code and keep the information in a single place and was cited in 1999 by Andrew Hunt and Dave Thomas in the book [The Pragmatic Programmer](https://en.wikipedia.org/wiki/The_Pragmatic_Programmer)

> The opposite of DRY would be _WET_ (Write Everything Twice or We Enjoy Typing).

In practice, if you have the same piece of information in two (or more) different places, you can use DRY to merge them into a single one and reuse it wherever you want/need.

See also:

- [The Pragmatic Programmer](https://en.wikipedia.org/wiki/The_Pragmatic_Programmer)

### Принцип KISS

[KISS on Wikipedia](https://en.wikipedia.org/wiki/KISS_principle)

> Keep it simple, stupid

The KISS principle states that most systems work best if they are kept simple rather than made complicated; therefore, simplicity should be a key goal in design, and unnecessary complexity should be avoided.  Originating in the U.S. Navy in 1960, the phrase has been associated with aircraft engineer Kelly Johnson.

The principle is best exemplified by the story of Johnson handing a team of design engineers a handful of tools, with the challenge that the jet aircraft they were designing must be repairable by an average mechanic in the field under combat conditions with only these tools. Hence, the "stupid" refers to the relationship between the way things break and the sophistication of the tools available to repair them, not the capabilities of the engineers themselves.

См. также:

- [Закон Галла](#закон-галла)

### YAGNI

[YAGNI on Wikipedia](https://en.wikipedia.org/wiki/You_ain%27t_gonna_need_it)


> Always implement things when you actually need them, never when you just foresee that you need them.
>
> ([Ron Jeffries](https://twitter.com/RonJeffries)) (XP co-founder and author of the book "Extreme Programming Installed")

This _Extreme Programming_ (XP) principle suggests developers should only implement functionality that is needed for the immediate requirements, and avoid attempts to predict the future by implementing functionality that might be needed later.

Adhering to this principle should reduce the amount of unused code in the codebase, and avoid time and effort being wasted on functionality that brings no value.

См. также:

- [Литература: Extreme Programming Installed](#литература)

### Заблуждения о распределённых вычислениях

[The Fallacies of Distributed Computing on Wikipedia](https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing)

Also known as _Fallacies of Networked Computing_, the Fallacies are a list of conjectures (or beliefs) about distributed computing, which can lead to failures in software development. The assumptions are:

- The network is reliable
- Latency is zero
- Bandwidth is infinite
- The network is secure
- Topology doesn't change
- There is one administrator
- Transport cost is zero
- The network is homogeneous

The first four items were listed by [Bill Joy](https://en.wikipedia.org/wiki/Bill_Joy) and [Tom Lyon](https://twitter.com/aka_pugs) around 1991 and first classified by [James Gosling](https://en.wikipedia.org/wiki/James_Gosling) as the "Fallacies of Networked Computing". [L. Peter Deutsch](https://en.wikipedia.org/wiki/L._Peter_Deutsch) added the 5th, 6th and 7th fallacies. In the late 90's Gosling added the 8th fallacy.

The group was inspired by what was happening at the time inside [Sun Microsystems](https://en.wikipedia.org/wiki/Sun_Microsystems).

These fallacies should be considered carefully when designing code which is resilient; assuming any of these fallacies can lead to flawed logic which fails to deal with the realities and complexities of distributed systems.

See also:

- [Foraging for the Fallacies of Distributed Computing (Part 1) - Vaidehi Joshi
 on Medium](https://medium.com/baseds/foraging-for-the-fallacies-of-distributed-computing-part-1-1b35c3b85b53)

### Принцип наименьшего удивления

[The Principle of Least Astonishment on Wikipedia](https://en.wikipedia.org/wiki/Principle_of_least_astonishment)

> People are part of the system. The design should match the user's experience, expectations, and mental models.
>
> Frans Kaashoek

This principle proposes that systems and interfaces should be designed in a way that features and functionality is easily discovered and matches users expectations. Features that 'surprise' users should be discouraged in favour of features that can be intuitively reasoned about based on existing patterns and practices.

Many examples are present in user interfaces, such as a 'pull down' gesture on a mobile appliation to refresh content. Another example would be command line tools, where many standards exist for how parameters are named, common parameters that should be available and so on.

См. также:

- [Соглашения по конфигурации](#todo)

## Литература

Если эти концепции показались вам интересными, вам могут понравиться следующие книги.

- [Чистый код. Создание, анализ и рефакторинг - Роберт Мартин](https://www.piter.com/product/chistyy-kod-sozdanie-analiz-i-refaktoring-biblioteka-programmista-45ccca) - Одна из самых уважаемых книг о том, как писать чистый и удобный для поддержки код.
- [Extreme Programming Installed - Ron Jeffries, Ann Anderson, Chet Hendrikson (en)](https://www.goodreads.com/en/book/show/67834) - Охватывает основные принципы экстремального программирования.
- [Гёдель, Эшер, Бах: эта бесконечная гирлянда - Дуглас Хофштадтер](https://www.livelib.ru/book/1000005849-gedel-esher-bah-eta-beskonechnaya-girlyanda-daglas-hofshtadter) - Эту книгу трудно классифицировать. [Закон Хофштадтера](#закон-хофштадтера) из этой книги.
- [Структура и Интерпретация Компьютерных Программ - Харольд Абельсон, Джеральд Джей Сассман, Джули Сассман](https://www.livelib.ru/book/1000799728-struktura-i-interpretatsiya-kompyuternyh-programm-dzhuli-sassman) - Если вы были студентом факультета компьютерных наук или электротехники в Массачусетском технологическом институте или Кембридже, это было вашим введением в программирование. Широко известно, что это был поворотный момент в жизни многих людей.
- [Собор и Базар - Эрик Стивен Реймонд](https://www.livelib.ru/work/1000216789-sobor-i-bazar-erik-s-rejmond) - Сборник эссе об открытом исходном коде. [Закон Линуса](#закон-линуса) из этой книги.
- [The Dilbert Principle - Scott Adams (en)](https://www.goodreads.com/book/show/85574.The_Dilbert_Principle) - Юмористический взгляд на корпоративную Америку от автора [принципа Дилберта](#принцип-дилберта).
- [Мифический человеко-месяц, или Как создаются программные системы - Фредерик Брукс мл.](https://www.piter.com/product/mificheskiy-cheloveko-mesyats-ili-kak-sozdayutsya-programmnye-sistemy) - Классический труд по программной инженерии. [Закон Брукса](#закон-брукса) является центральной темой книги.
- [Принцип Питера, или Почему дела всегда идут вкривь и вкось - Лоуренс Джонстон Питер, Реймонд Халл](https://azbooka.ru/books/printsip-pitera-ili-pochemy-dela-vsegda-idyt-vkriv-i-vkos) - Еще один юмористический взгляд на проблемы крупных организаций и управления людьми, источник принципа [Принцип Питера](#принцип-питера).

## Онлайн ресурсы

Некоторые полезные ресурсы и материалы для чтения.

- [CB Insights: 8 Laws Driving Success In Tech: Amazon's 2-Pizza Rule, The 80/20 Principle, & More (en)](https://www.cbinsights.com/research/report/tech-laws-success-failure) - интересное описание некоторых законов, оказавших большое влияние на технологии.

## PDF версия

Проект доступен в виде электронной книги в формате PDF. [Загрузите последнюю версию электронной книги в формате PDF по этой ссылке](https://github.com/dwmkerr/hacker-laws/releases/latest/download/hacker-laws.pdf) или проверьте страницу [релиза](https://github.com/dwmkerr/hacker-laws/releases) для более ранних версий.

Новая версия электронной книги создается автоматически при добавлении тега новой версии.

## Подкаст

Hacker Laws был представлен в подкасте [The Changelog](https://changelog.com/podcast/403).
Вы можете ознакомиться с эпизодом по ссылке ниже:

<a href="https://changelog.com/podcast/403" target="_blank"><img src="./images/changelog-podcast.png" width="800px" alt="Changelog Podcast Image" /></a>

