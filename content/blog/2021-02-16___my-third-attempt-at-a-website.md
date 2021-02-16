---
title: "My third attempt at a website"
slug: "2021-02-16___my-third-attempt-at-a-website"
date: "2021-02-16T00:00:00-08:00"
tags: [ "Meta" ]
---

## Attempt No. 1

Back in 2015, I was looking at portfolio websites from some folks I knew from
university and decided that I wanted a "modern" looking one for myself. At the
time, I only had limited exposure to web development from my co-op work term at
Nav Canada in 2012 (where I used
[ICEFaces](http://www.icesoft.org/java/projects/ICEfaces/overview.jsf)) and a
hospital database management system group assignment for my Databases course
(which used [JSP](https://projects.eclipse.org/projects/ee4j.jsp) for its
backend and [Bootstrap](https://getbootstrap.com) for its frontend). Armed with
my lack of familiarity with HTML, CSS, and JavaScript, I ended up hacking
together a hardcoded static portfolio website using [Semantic
UI](https://semantic-ui.com) (because it looked "modern") and hosting it on
[GitHub Pages](https://pages.github.com) (because it's free as in 🍺).

<div class="columns mt-5">
  <div class="column">
    <img src="/blog/2021-02-16___my-third-attempt-at-a-website/img/website-1.png">
  </div>
</div>

## Attempt No. 2

In 2019, while looking for ways to improve my portfolio website, I came across
[Jekyll](https://jekyllrb.com). Using Jekyll, it's possible to generate a static
website/blog using [Markdown](https://daringfireball.net/projects/markdown),
HTML, and CSS. Refactoring my project posts into Markdown and adding a blog
sounded intriguing, so I tried to redo my portfolio website using Jekyll and the
[Clean Blog Jekyll](https://startbootstrap.com/theme/clean-blog-jekyll) theme by
[Start Bootstrap](https://startbootstrap.com). Problem was, I couldn't quite
figure out how to customize the website to add a separate "blog" for projects
due to my lack of familiarity with HTML, CSS, JavaScript, and now Ruby (which
Jekyll is written in). Being lazy, my second website ended up persistently
"under construction" and I ended up taking it down later on.

<div class="columns mt-5">
  <div class="column">
    <img src="/blog/2021-02-16___my-third-attempt-at-a-website/img/clean-blog-jekyll-theme.png">
  </div>
</div>

## Attempt No. 3
Due to the COVID-19 pandemic in 2020, I suddenly found myself stuck at home with
a lot of time on my hands. I ended up spending some of that time learning web
development with [Node.js](https://nodejs.org).

At some point in 2020, I decided that I wanted to try again at building a
portfolio website/blog. Now that I was familiar with HTML, CSS, JavaScript, and
Node.js, I considered building a dynamic website to host my project portfolio/
blog. However, managing a database sounded like a lot of work and I didn't want
to pay for hosting, so I quickly dropped that option. As a result, I decided to
have a look at some other static site generators. I almost considered using
[VuePress Blog](https://vuepress.vuejs.org/plugin/official/plugin-blog.html),
but I found it very difficult to customize. Also, I thought the [default blog
theme](https://vuepress.vuejs.org/theme/blog-theme.html) for VuePress Blog was
meh.

<div class="columns mt-5">
  <div class="column">
    <img src="/blog/2021-02-16___my-third-attempt-at-a-website/img/vuepress-default-blog-theme.png">
  </div>
</div>

Ultimately, I decided to build my portfolio website/blog using
[NuxtJS](https://nuxtjs.org) (which is built on top of
[Vue.js](https://vuejs.org)) and the
[`@nuxt/content`](https://content.nuxtjs.org) module. I decided to use the
[Buefy](https://buefy.org) and [Bulma](https://bulma.io) CSS frameworks for the
frontend, since I felt it was more intuitive than [Bootstrap
Vue](https://bootstrap-vue.org). I also decided to go for a simpler UI this time
around. As a result, I now have a statically generated portfolio website/blog
hosted on GitHub Pages with a responsive UI which scales to both desktop and
mobile screen sizes 😃.

<div class="columns mt-5">
  <div class="column is-2">
    <img src="/blog/2021-02-16___my-third-attempt-at-a-website/img/website-3-mobile.PNG">
  </div>
  <div class="column">
    <img src="/blog/2021-02-16___my-third-attempt-at-a-website/img/website-3-desktop.png">
  </div>
</div>