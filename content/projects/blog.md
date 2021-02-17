---
title: "blog"
description: "My personal website and blog."
date: "2021-02-16T00:00:00-08:00"
slug: "blog"
github: "https://github.com/j43cheun/blog.git"
tags: [ "Nuxt.js", "Vue.js", "Buefy", "Bulma", "Markdown", "HTML", "JavaScript", "CSS" ]
---

This website here, aptly named **blog**, is my personal website. I built it in
order to host content about my personal and professional projects, as well as my
blog. I also built it as an excuse to practice some of the web development
skills I learned during the COVID-19 pandemic in 2020.

For the implementation, I went with a statically generated website built using
the [Nuxt.js](https://nuxtjs.org) framework for the frontend and the
[`@nuxt/content`](https://content.nuxtjs.org) (content) module CMS. Going with
this implementation had several advantages. First, posts are formatted and
stored in [Markdown](https://daringfireball.net/projects/markdown). This allows
post content to be decoupled from the layout of the website. Second, there is no
database to manage and in turn, no database security concerns to contend with.
Third, since Nuxt.js is built on top of [Vue.js](https://vuejs.org), it is easy
to reuse code by defining custom reusable components using HTML, JavaScript, and
CSS. Fourth, using Nuxt.js and Vue.js does not require me to learn a new
programming language (e.g., Ruby, Go, etc.). Finally, the website is static, so
it can be hosted free of charge on [GitHub Pages](https://pages.github.com).

As for the layout, I went with a plain and simple responsive UI built using the
[Buefy](https://buefy.org) and [Bulma](https://bulma.io) CSS frameworks. Buefy
was chosen for its integration with Nuxt.js while Bulma was chosen for its ease
of use (Bulma is a CSS-only framework) and customizability. Other CSS frameworks
were also considered. In particular, I felt [Vuetify](https://vuetifyjs.com/)
was too rigid and I felt [Bootstrap-Vue](https://bootstrap-vue.org) was not
intuitive to use.

<div class="columns mt-5">
  <div class="column is-2">
    <img src="/projects/blog/img/blog-mobile.png">
  </div>
  <div class="column">
    <img src="/projects/blog/img/blog-desktop.png">
  </div>
</div>
