---
layout: post
title:  "Learn Angular 2+ by building an App - WIP"
date:   2017-05-11
categories: jekyll update
comments: true
---

In this post, we would be learning Angular core concepts by building yet another version of Todo App :). If you are just starting with Angular (version 2+) and want to know what are differences between AngularJS and Angular, please checkout my earlier post [here][angularjsVsAngular].
We would be using [angular cli][angular-cli] for building our App.Just have it installed in your dev box.
Let's get started...

## Here comes the wireframe
This is the place it starts from. [Here][todo-app-link] is the link to the working version  of how our todo App should look like. It has 2 views - Home where we add our todos and Archive where we can manage our completed todos. **Note:** About page is still not added, but this will just have some static content 

## Step 1 - Seeing the page as components
I usually start with identifying the components in a given view. A component as per definition from techtarget: 
> A component is an identifiable part of a larger program or construction.

I usually apply Single Responsibility principle to help determine the components in the view. Each component should be responsible for one and only one logical functionality. By applying this principle, we can decompose the home page into the following components
  * Todo List
  * Todo item


## Summary




[angularjsVsAngular]: http://sundarcodes.in/2017/03/28/difference-between-angular1-and-ang2.html
[angular-cli]: https://cli.angular.io/
[todo-app-link]: https://sundarcodes.github.io/Angular-Training