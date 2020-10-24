<template>
  <div>
    <article>
          <h1>{{ article.title }}</h1>
{{ article.date | formatDate }}
<nuxt-content :document="article"></nuxt-content>
    </article>
  </div>
</template>


<script>
export default {
  layout: "master",
  async asyncData({ $content, params }) {
    const article = await $content("blog", params.slug).fetch();
    return {
      article
      };
  },
};
</script>


