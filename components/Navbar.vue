<template>
  <b-navbar centered spaced>
    <template #brand>
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        <strong>Justin Cheung</strong>
      </b-navbar-item>
      <b-navbar-item href="https://github.com/j43cheun">
        <b-icon icon="github" />
      </b-navbar-item>
      <b-navbar-item href="https://www.linkedin.com/in/ulongmax/">
        <b-icon icon="linkedin" />
      </b-navbar-item>
      <b-navbar-item href="mailto: me@j43cheun.dev">
        <b-icon icon="email" />
      </b-navbar-item>
    </template>
    <template #end>
      <b-navbar-item tag="router-link" :to="{ path: '/about' }">
        About
      </b-navbar-item>
      <b-navbar-item tag="router-link" :to="{ path: '/projects' }">
        Projects
      </b-navbar-item>
      <b-navbar-item tag="router-link" :to="{ path: '/blog' }">
        Blog
      </b-navbar-item>
      <b-navbar-item tag="router-link" :to="{ path: '/gallery' }">
        Gallery
      </b-navbar-item>
    </template>
  </b-navbar>
</template>
