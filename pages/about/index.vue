<template>
  <main>
    <section v-if="about" class="w-full max-w-2xl mx-auto">
      <template>
        <div>
          <img v-if="about.thumbnail" class="w-1/4 m-0 m-auto mt-10" :src="about.thumbnail" />
          <template>
            <span class="flex-1">
              <div class="mt-3 text-base text-2xl text-center font-black">{{ about.title }}</div>
              <div class="text-sm font-ligth text-center">{{ about.subtitle }}</div>
              <p class="mt-4 text-center">{{ about.description }}</p>
            </span>
          </template>
        </div>
      </template>
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, error }) {
    let about
    try {
      about = await $content('about').fetch()
    } catch (e) {
      error({ message: 'About data not found' })
    }
    return { about: about[0] }
  },
}
</script>
