<template>
  <b-navbar spaced>
    <template #brand>
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        <strong>Justin Cheung</strong>
      </b-navbar-item>
    </template>
    <template #start>
      <b-navbar-item href="https://github.com/j43cheun">
        <b-icon icon="github" />
      </b-navbar-item>
      <b-navbar-item href="https://www.linkedin.com/in/ulongmax/">
        <b-icon icon="linkedin" />
      </b-navbar-item>
    </template>
  </b-navbar>
</template>
