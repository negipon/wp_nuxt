<template>
  <div>
    <h3>
      Recent Posts
    </h3>
    <ul>
      <li v-for="(item, key, index) in posts" :key="index">
        <nuxt-link :to="slugToUrl(item.slug)">{{ item.title }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  props: ['posts'],
  methods: {
    slugToUrl(slug) {
      return `/${slug}`
    }
  }
}
</script>

<style scoped>

h3 {
  font-size:22px;
}
a {
  color:#444;
}
a.nuxt-link-active {
  color:#ccc;
}
</style>
