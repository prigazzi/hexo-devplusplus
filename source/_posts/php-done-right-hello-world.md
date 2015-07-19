title: Hello World
subtitle: "The general facts about our everyday work"
date: 2014-10-14 18:21:31
tags:
categories:
	- codecademy
---
### Getting started with PHP

This is a comprehensive list of topics that you must know before starting fiddling with PHP within Coolblue. PHP is very well known by the multiplicity of its configurations and ways of doing things, and we know not all of them are wrong.

This are simply ours.

### PHP versions we´re using

We´re trying the best we can to use the last stable PHP version in our production and development set ups. So long, we´re running latests versions of PHP 5.5 in all our environments. 

### Our development setup

We´re creating our development environment virtualizing with [Vagrant](http://vagrantup.com) and [VirtualBox](http://virtualbox.org). These images are automatically set up through [Puppet Manifests](http://puppetlabs.com) that leave you with a properly set dev machine. You only need to include is some *awesome* "**codes**". 

### Coding Standards

For all our new proyects, we´re using **PSR-4** as our current coding standard, and we´re enforcing it properly within our IDE by default, [PHPStorm](https://www.jetbrains.com/phpstorm/).

But for every rule you may know that there are always exceptions. And in Coolblue we also have some of those, as are the cases for **Skunksworks** and **Flirt**.  For these two proyects, we´re using some specific coding standards as defined in the Wiki. 

### Coding Style

Disregarding the standards we´re using for coding, every single proyect within Coolblue tries to aim at a certain level es quality and design. At first it´s going to be like you walk in sand, but you´ll get up to speed, don´t worry. 

#### Object Orientation

Every proyect in Coolblue will be coded in an Object Oriented fashion. There´s absolutely no exceptions to this. Even if you´re working in our oldest codebase, like **Flirt**, you´ll find a clear object orientation pattern there. 

#### Design Patterns

If you have a trained eye, you´ll discover certain design patterns over there. Explaining these patterns are subject to a complete different course in Coolcademy, but for the time being, you´ll notice some common cases like Singletons over here and there that we´re hardly trying to remove (Why?, you may say. Ask your new colleague and he will definitely tell you why we hate Singletons), some factories, and certain implementations of MVC. 

### Debugging

If you configured already your development platform, you´ll notice that we´re running the latest version of PHP along with xDebug enabled. The de-facto IDE we use here, PHPStorm, supports debugging PHP code and you´ll find it pretty easy to do it if you´ve never done it before. 
