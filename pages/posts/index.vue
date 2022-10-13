<template>
  <div>
    <h1>Posts</h1>
    <div
      v-for="post in posts"
      class="px-3 mb-3 py-2 rounded-md border border-solid border-slate-200"
    >
      <nuxt-link v-bind:to="'/posts/' + post.slug">
        {{ post.title }}
      </nuxt-link>
    </div>
  </div>
</template>

<script>
import { urlAPI, companyName } from "~/config";
export default {
  head() {
    return {
      title: `Posts - ${companyName}`,
    };
  },
  async asyncData() {
    const data = await fetch(urlAPI).then((res) => res.json());
    const posts = data.data;
    return { posts };
  },
};
</script>

<style lang="scss" scoped></style>
