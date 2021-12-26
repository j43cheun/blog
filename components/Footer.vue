<template>
  <footer class="footer">
    <div class="content has-text-centered is-size-7">
      &copy; Justin Cheung {{ new Date().getFullYear() }} ⋅ Number of days in quarantine: {{ Math.trunc((new Date() - new Date("03/06/2020")) / (1000 * 3600 * 24)) }}
    </div>
  </footer>
</template>
