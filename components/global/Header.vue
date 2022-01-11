<template>
  <nav class="scrim-bg w-full fixed z-40 top-0 inset-x-0px-3" aria-label="Main Menu">
    <ul class="flex">
      <li class="py-3 ml-5">
        <nuxt-link class="btn font-sans" to="/">Home</nuxt-link>
      </li>
      <li class="py-3 ml-5">
        <nuxt-link class="btn" to="/blog">Blog</nuxt-link>
      </li>
      <!-- <li class="py-3 ml-5">
        <nuxt-link class="btn" to="/projects">Projects</nuxt-link>
      </li> -->
      <li class="py-3 ml-5">
        <nuxt-link class="btn" to="/about">About</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="postcss" scoped>
.scrim-bg {
  border-bottom: 1px solid var(--color-primary-100);
  background-color: var(--bg);
}
.nuxt-link-exact-active {
  @apply text-primary-300 font-bold;
}

.light {
  & .scrim-bg {
    &::after {
      animation-name: fadeIn2;
    }
  }
  & .nuxt-link-exact-active {
    @apply text-primary-300;
  }
}

/* Need two because of smoother switching between color modes */
@keyframes fadeIn1 {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@keyframes fadeIn2 {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
