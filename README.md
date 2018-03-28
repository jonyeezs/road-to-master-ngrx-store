# Road To Master Ngrx/Store
A curated guided hyperlinks to learn all there is to know of Ngrx/Store

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- **Content**
	- [What does state mean?](#what-does-state-mean)
	- [Why the need for a UI state management?](#why-the-need-for-a-ui-state-management)
	- [Ngrx/Store](#ngrxstore)
	- [Why choose Ngrx/Store as your _"flux capacitor"_](#why-choose-ngrxstore-as-your-flux-capacitor)
	- [Building blocks of Ngrx/Store](#building-blocks-of-ngrxstore)
		- [Reducer and its application state](#reducer-and-its-application-state)
			- [meta-programming on reducers](#meta-programming-on-reducers)
		- [Ways to manage the application's state](#ways-to-manage-the-applications-state)
		- [Handling side-effects caused by change of state](#handling-side-effects-caused-by-change-of-state)
		- [Actions](#actions)
		- [Gluing and registering actions to reducers](#gluing-and-registering-actions-to-reducers)
		- [Selectors](#selectors)
	- [Dev Tools](#dev-tools)
	- [Recommended tutorials](#recommended-tutorials)
	- [Supporting resources](#supporting-resources)

<!-- /TOC -->

---

All information is currently base on [Ngrx/Store v4](https://github.com/ngrx/platform)

The links that are tagged would lead you to the exact snippet of the linked article that is relevant to the topic. Some post may not have anchors but the whole article should help you in your journey as well. Feel free to skip to the relevant topic or read all of it. The time indicators will be for the prescribed texts only.

Here we go!

## What does state mean?
* [Understanding UI state][state-management] <sup>(5mins)</sup>
* [What is usually in a state][defining-state] <sup>(23sec)</sup>

## Why the need for a UI state management?
* [The motivation][redux-motivation] <sup>(1min)</sup>
* [A video on the history of how the solution was born - Flux][flux] <sup>(44:35mins)</sup>
* [What is the most frequent problem that it][problem-it-solves]  <sup>(2mins)
* [How does it relate to state in Angular SPA?][persisting-state-in-angular] <sup>(2mins)</sup>

## Ngrx/Store
* [Principles borrowed from Redux][principles] <sup>(3mins)</sup>
* [Contains building blocks to implement Flux][readme] <sup>(26secs)</sup>
* [Prerequisite: must know reactive programming RxJS][rxjs] <sup>(25mins)</sup>

## Why choose Ngrx/Store as your _"flux capacitor"_
* [Advantages][advantages] <sup>(2mins)</sup>
* [A video on some thoughts why this suits angular][why-ngrx-for-angular] <sup>(65secs)</sup>
* [Well opinionated comparison on redux vs ngrx/store][redux-vs-ngrx] <sup>(3mins)</sup>

## Building blocks of Ngrx/Store

### Reducer and its application state
* [What is a reducer][reducer] <sup>(4mins)</sup>
* [Designing reducer (_although from Redux, it has the exact same pattern_)][reducer-by-redux] <sup>(15mins)</sup>

#### meta-programming on reducers
* [middle-ware on reducers][meta-reducers] <sup>(2mins)</sup>

### Ways to manage the application's state
* [Partition state table by featureModule][fractal-state] <sup>(32secs)</sup>
* [Using scan Rxjs operator to automatically maintain state updates][scan-on-dispatch] <sup>(2mins)</sup>
* [Using ngrx/entity to reduce boilerplate in creating entity-type application state][ngrx-entity] <sup>(3mins)</sup>

### Handling side-effects caused by change of state
* [SO answers the need for ngrx/effects][so-effects] <sup>(9mins)</sup>
* [Pro-tips on when and how to use effects][pro-effects] <sup>(6mins)</sup>
* [Controlling lifecycle of effect][on-run] <sup>(40secs)<sup>

### Actions
* [Creating actions][type-actions] <sup>(10mins)</sup>
* [Three categories of action][cat-actions] <sup>(1min)</sup>
* [Use several actions to convey an interaction][action-story] <sup>(2mins)</sup>

### Gluing and registering actions to reducers
* [Using ActionReducerMap][action-reducer-map] <sup>(24secs)</sup>

### Selectors
* [All you need to know about selectors][selectors]

## Dev Tools

* [store devtools browser extension][store-devtools] - allows you to monitor events and chart the state. To have it working with ng-cli, see [here][dev-cli]

## Helper Libraries

* ~~NGRX-Actions - Using decorators and class symbols to reduce the boiler-plate~~ (_The author is diverting his resources to a new state management library.)
* [Angular-ngrx-data](https://github.com/johnpapa/angular-ngrx-data) - Manages entity in a clever black-box
* [Nrwl Extensions](https://nrwl.io/nx) - Developer toolkit to assist in Ng development, which comes with [Ngrx CLI generators](https://nrwl.io/nx/guide-setting-up-ngrx)

[ngrxaction]: https://medium.com/@amcdnl/reducing-the-boilerplate-with-ngrx-actions-8de42a190aac

## Recommended tutorials

* [Paid step-by-step tutorial by Todd Motto](https://ultimateangular.com/ngrx-store-effects)
* [Tour of Heroes tutorial with Ngrx/store](https://github.com/LMFinney/toh-ngrx4)

<!--link references-->
[state-management]: https://medium.com/front-end-developers/domain-state-vs-ui-state-768c1271a41d
[defining-state]: https://angular-2-training-book.rangle.io/handout/state-management/ngrx/defining_your_main_application_state.html
[redux-motivation]: https://redux.js.org/docs/introduction/Motivation.html
[flux]: https://youtu.be/nYkdrAPrdcw
[problem-it-solves]: https://blog.angular-university.io/angular-2-redux-ngrx-rxjs#whatisthemostfrequentproblemthatreduxsolves
[persisting-state-in-angular]: https://malcoded.com/posts/angular-ngrx-guide#state-in-angular
[readme]: https://github.com/ngrx/platform/blob/master/docs/store/README.md
[rxjs]: https://gist.github.com/staltz/868e7e9bc2a7b8c1f754
[principles]: https://redux.js.org/docs/introduction/ThreePrinciples.html
[why-ngrx-for-angular]: https://www.youtube.com/embed/BxHkI0NUGNQ?start=95&end=161
[advantages]: https://gist.github.com/btroncone/a6e4347326749f938510#advantages-of-store
[redux-vs-ngrx]: https://medium.com/@charliegreenman/redux-vs-rxjs-ngrx-store-db6066058719
[reducer]: https://gist.github.com/btroncone/a6e4347326749f938510#whats-a-reducer
[reducer-by-redux]: https://redux.js.org/docs/basics/Reducers.html
[meta-reducers]: https://netbasal.com/implementing-a-meta-reducer-in-ngrx-store-4379d7e1020a
[fractal-state]: https://github.com/ngrx/platform/blob/master/docs/store/api.md#feature-module-state-composition
[scan-on-dispatch]: https://gist.github.com/btroncone/a6e4347326749f938510#aggregating-state-with-scan
[ngrx-entity]: https://medium.com/ngrx/introducing-ngrx-entity-598176456e15
[so-effects]: https://stackoverflow.com/questions/39552067/what-is-the-purpose-of-ngrx-effects-library
[pro-effects]: https://medium.com/@m3po22/stop-using-ngrx-effects-for-that-a6ccfe186399
[on-run]: https://github.com/ngrx/platform/blob/master/docs/effects/api.md#controlling-effects
[type-actions]: https://toddmotto.com/ngrx-store-actions-versus-action-creators
[cat-actions]: https://blog.nrwl.io/ngrx-patterns-and-techniques-f46126e2b1e5#8d68
[action-story]: https://blog.nrwl.io/ngrx-patterns-and-techniques-f46126e2b1e5#96a8
[action-reducer-map]: https://www.concretepage.com/angular-2/ngrx/ngrx-store-4-angular-5-tutorial#ActionReducerMap#ActionReducerMap
[selectors]: https://github.com/ngrx/platform/blob/master/docs/store/selectors.md
[store-devtools]: http://extension.remotedev.io/
[dev-cli]: https://blog.schwarty.com/using-ngrx-store-devtools-with-the-angular-cli-a3b5f88f12e9

---

## Supporting resources

* [Style guide](https://github.com/orizens/ngrx-styleguide)
* [Introduction video by ngrx team](https://youtu.be/cyaAhXHhxgk)
* [Core concepts inspired by Redux](https://redux.js.org/docs/introduction/CoreConcepts.html)
* [Video by Mike Ryan(lead contributor of Ngrx) describing benefits of ngrx ](https://www.youtube.com/watch?v=BxHkI0NUGNQ)
* [Comprehensive Introduction to @ngrx/store by @btroncone](https://gist.github.com/btroncone/a6e4347326749f938510)
* [Example of a minimal setup](https://github.com/ngrx/platform/blob/master/docs/store/setup.md)
* [Splitting state by features](http://ngxsolutions.azurewebsites.net/understanding-features-in-ngrx-4/)
* [A developers learnings on ngrx](https://hackernoon.com/what-i-have-learned-using-ngrx-redux-with-angular-2-20a748149661?gi=fbb7e4910efa)
* [What's feature module](https://blog.realworldfullstack.io/real-world-angular-part-7-lazy-coding-load-splitting-4552f5f54ef7#e15e)
