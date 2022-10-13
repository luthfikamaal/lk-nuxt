<template>
  <div>
    <Head>
      <Title>{{ post.title }}</Title>
    </Head>
    <div class="text-2xl">{{ post.title }}</div>
    <div v-html="post.text"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "Hello",
    };
  },
  head() {
    return {
      title: this.post.title,
    };
  },
  async asyncData({ params }) {
    console.log(params.slug);
    const data = await fetch(
      `https://blog-rest-api.000webhostapp.com/api/post/${params.slug}`
    ).then((response) => response.json());
    const post = data.data;
    // this.title = post.title;
    console.log(post);
    return { post };
  },
};
</script>

<style lang="scss" scoped></style>
