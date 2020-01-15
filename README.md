Welcome to Vue 3.0
========

A small talk of summary latest Vue 3.0 news

Live: [【思否编程公开课】迎接Vue 3.0](https://segmentfault.com/ls/1650000021531837)

Thoughts from Evan You
--------

### [Twitter 1](https://twitter.com/youyuxi/status/1209870207398957057)

API design is in some way like designing a mental tax system: you can use a flat tax rate, or you can have brackets. Which system is fairer depends on the distribution of income level (in the case of API, use case complexity level) of the tax payers.

制定税收法律时，可以使用线性税率，也可以使用递进式税率。评价那种税收制度更公正，要看收入水平不同的人，谁缴的税更多。设计 API 也类似，要看哪些开发人员需要面对更复杂的问题。

The incentive of the system designer is a bit different though, as API designers, we want to minimize the total amount of tax collected, instead of maximizing it.

作为 API 设计人员，我们的目标和税收系统的谋划者不同：我们希望尽可能少征税，而不是多征税。

So if 90% of our users can stay in a low bracket, while only 10% falls into the higher bracket, to me that's better than a higher flat effective tax rate for everyone.

所以，如果 90% 的用户能够留在低税率阶段，只有 10% 的用户需要多缴税，在我看来，比大家平摊税负要好得多。

This is why Vue's API is in some way "layered": templates and Options API solve the majority of use cases pretty well with a very low tax rate. Composition API and render functions are a bit more taxing, but only for those who intend to make more out of the system.

正因为如此，Vue 的 API 是“分层”的：模版和对象式 API 可以满足大部分使用场景，工作得很好，只需要用户投入很少的学习时间。Composition API 和渲染函数需要“缴纳更多的税赋”，但是只有少数开发者需要负担，而他们也将从系统中获取更多收益。

1. The fundamental question though is are you designing for a more homogenous or a more diverse audience. For Vue, it's obviously the latter.
1. 简言之，（框架设计的）基本的问题是，你的目标用户群体，是同质化的，还是差异化的。 对于 Vue 来说，显然是后者。
2. Note I use the term "layered" instead of "forked", because render functions and Composition API are just exposing the same underlying concepts in a lower level API (which templates and the Options API are built on top of).
2. 同时请注意，我使用的术语是“分层的”，而不是“分叉的”。因为渲染函数和 Composition API 暴露出的 API 与模版和对象式 API 是基于同样的基础概念打造，只是前者更加底层而已。

### [Twitter 2](https://twitter.com/youyuxi/status/1192105980126998528)

The keyword is balance. Balance between scalability vs. approachability, power vs. size, framework coherence vs. low-level flexibility.

平衡是关键。在扩展性与易用性之间寻求平衡，在功能与体积之间寻求平衡，在架构一致性与底层灵活性之间寻求平衡。

References
--------

1. [State of Components (DotJS 2019)](https://docs.google.com/presentation/d/1jN_WUXYux-H8nuwSsO_-o4E7LWdX15S4nLH_9f3Xk6o/edit#slide=id.g6c09ba32c9_0_141)
2. [Design Principles of Vue 3.0](https://vuetoronto.com/videos/design-principles-of-vue-3-evan-you/)
3. [Vue Roadmap](https://github.com/vuejs/vue/projects/6)
4. [Vue Composition API](https://composition-api.vuejs.org/)
