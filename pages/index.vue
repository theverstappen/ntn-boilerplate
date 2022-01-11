<template>
  <main>
    <section class="mt-8">
      <h3 class="text-primary-600 dark:text-primary-400 max-w-2xl mx-auto">Latest blog post</h3>
      <posts post-type="blog" :amount="1" />
    </section>
  </main>
</template>