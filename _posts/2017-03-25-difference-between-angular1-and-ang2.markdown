---
layout: post
title:  "Difference between AngularJS and Angular 2"
date:   2017-03-28 06:44:01 +0530
categories: jekyll update
---

[Angular][angular] the framework as this is what the Angular team would like to call, has evolved(and evolving) from being the most popular MV* framework to a framework that has brought in best of from other good front end frameworks around and has transformed itself to survive and be a leader for years to come.

In this post, we would be seeing how different is Angular 2 and what are the new additions it is bringing to the world of Single Page App development. Before we start with that, lets first understand what triggered the development of Angular 2 which is essentially a rewrite of the AngularJS framework. Lets discuss about the pain points in AngularJS that made the Angular dev Team rewrite the framework from scratch.

## _Pain Points in AngularJS_

# 1. Scope pollution
To connect the view with data, we know we have to use the $scope object and we could just keep modifying depending on the context. But what this has lead too is $scope objects getting cluttered all through our controller code which makes maintaining and debugging the application hard. In addition to the current scope, we could also access parent or root scope freely which again creates havoc when we update data at different controllers.

# 2. Digest Cycle - Boon becoming a bane
Two-way data binding was one killer feature that made developers go 'wow' and one of main reasons to increase Angular JS adoption. But this also brought in the ugly digest loop. As we have more watchers in our views, the digest loop is going to take more time which is going to impact our page responsiveness.

# 3. Communication among different UI View/Screens - Deep Mesh(s)
$broadcast, $emit, $on are used to communicate among sections of your App but these are slow as it has to traverse through sometimes the entire scope.

To address these issues, Angular team decided that a rewrite is required as all these core to AngularJS. Having said this, Angular team still continues to work on AngularJS, making it better for people using it.

OK. Lets now look at whats new in Angular 2 and how it is addressing the above mentioned issues.

# 1. Think in Terms of Components
Angular team realized that the MV* way of building SPA was not fitting into the realm of modern web app development. In came [Web Components][web-components] approach popularized by [ReactJS][react-js]. This is one of the core change in Angular 2, thinking of UI design in terms of components and how they interact and communicate. There is no more concept of global scope as each component has its own scope.

# 2. Better Change detection Strategy - Bye Bye Digest Cycle
With the component based approach, the change detection strategy could be well optimized thus eliminating the digest cycle. Dirty checking is still employed to detect the changes, but this checking happens only once for a component and its children. Use of immutable objects and observables aids in highly performant apps. For more info on the change detection strategy, please refer to Vicktor Savkin's [blog][victor-blog].

# 3. Leaning towards uni-directional flow of data

# 4. Platform agonistic - Angular can run on Server now

# 5. Embracing TypeScript - Stronger Type Checking

[angular]: https://angular.io/
[web-components]: https://developer.mozilla.org/en-US/docs/Web/Web_Components
[react-js]: https://facebook.github.io/react/
[victor-blog]: https://vsavkin.com/change-detection-in-angular-2-4f216b855d4c