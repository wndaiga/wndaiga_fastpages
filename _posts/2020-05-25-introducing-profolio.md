---
toc: true
layout: post
description: An approach to managing your professional online portfolio
categories: [portfolio,professional]
title: Introducing Profolio
hide: false
---

## Introduction

Primary aim is to help job-seeking technology workers effectively manage
their professional portfolios on Github. Secondary aims are:

<ul>
    <li>
        <span>To serve as base content for Webiterate's first experiment</span>
    </li>
    <li>
        <span>To help introduce readers to Github's various platform tools</span>
    </li>
    <li>
        <span>To develop engaged community of like-minded and similarly situated individuals</span>
    </li>
    <li>
        <span>To increase my professional visibility</span>
    </li>
</ul>

## Background
<small>We automate much of our work, can we do the same for our <span>body</span> of work?</small>

We are in dramatically tenuous times. It is difficult to process and
manage the demands of job-seeking while also navigating personal
stressors exacerbated by the pandemic. Recruitment has by-and-large,
ground to a near halt, networking platforms like LinkedIn are uniquely
geared towards itemizing our work. Collaborative software development
platforms like Github are conversely tooled to store our work. Currently
siloed, this blog post serves to both question and hopefully bridge
these sibling worlds for the benefit of job-seeking technology workers.

In this section we'll review the underpinning technologies that will
be used to build Profolio. It should be noted that while the tools
explored in this post detail Github-specific offerings, the same can be
achieved with alternative platforms (e.g.
[NetlifyCMS]("https://www.netlifycms.org/"), [CircleCI]("https://circleci.com/") 
and [Scripting]("https://nodejs.org/en/about/"). This article
is largely focussed on solution speed and sacrificed exploration for
exploitation to minimise lead-time.

### Github Pages

[Github Pages]("https://pages.github.com/") is a static
site hosting service that allows for the building and publishing of
[HTML]("https://developer.mozilla.org/en-US/docs/Web/HTML"),
[CSS]("https://developer.mozilla.org/en-US/docs/Glossary/CSS")
and [JavaScript]("https://developer.mozilla.org/en-US/docs/Glossary/JavaScript")
files from a [Github]("https://www.howtogeek.com/180167/htg-explains-what-is-github-and-what-do-geeks-use-it-for/")
repository. It offers quick, reliable and consistent website publishing
and lowers the barrier to entry for development of the same. For an
in-depth and digestible overview of the same please take this quick
[GitHub Pages course]("https://lab.github.com/githubtraining/github-pages")
on Github's Learning Lab.


### Github Webhooks


[Github Webhooks]("https://developer.github.com/webhooks/")
are a HTTP-based, event subscription mechanism offered by Github to
developers who might want to integrate with Github's platform.
Developer integration tasks might include performing
[OAuth]("https://developer.okta.com/blog/2017/06/21/what-the-heck-is-oauth")
or alerting an application to the state of a repository. Ever signed in
or registered to an online service through your social media platform of
choice? Those are webhooks in action.


### Github Actions


[Github Actions]("https://github.com/features/actions")
are an approach to creating
[Continuous Integration / Continuous Delivery]("https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment")
pipelines on Github. These pipelines/workflows allow developers to
quickly integrate and deploy their developed code to end-users.


### Github Templates


[Github Templates]("https://github.blog/2019-06-06-generate-new-repositories-with-repository-templates/")
are a quick and robust way of sharing repetitive code across
repositories. It allows users to share entire files and folders between
different projects that rely on the same content and structure,
circumventing time overheads involved in setting up projects.


## Design
<small>Can we git our jobs?</small>


While Networking platforms require you to manually update your profiles
with content, dynamical platforms like Github conversely track and
follow you throughout your professional career (at least if you work
with software, but this too is shifting). We will aim to use the latter
to track, manage and showcase professional online portfolios. To develop
our proof of concept, we envision utilising the following tools and
processes:

<ul>
<li>
<span>
Use Github pages to create and host static portfolio pages
</span>
</li>
<li>
<span>
Use Github webhooks and actions that will build updated portfolio
versions
</span>
</li>
<li>
<span>
Use Github repository templates to share proof of concept with wider
community
</span>
</li>
</ul>

<iframe
width="100%"
height="450"
title="Profolio-design"
src="https://whimsical.com/embed/FHLAa1Xru9b97qVR75MBqY#2Ux7TurymMrx1skZe73J"
/>

## Implementation


A number of Github Action Workflows were developed to prototype
Profolio and will be reviewed below.


### Github Resume Workflow

