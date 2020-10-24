<template>
  <div class="prys_writings">
    <div v-for="article in articles" :key="article.id">
      <nuxt-link :to="`/writings/${article.slug}`">
      <v-card class="mx-auto elevation-0" max-width="344">
        <v-card-title>
          {{ article.title }}
        </v-card-title>
        <v-card-subtitle>
          {{ article.date | formatDate }}
        </v-card-subtitle>
      </v-card>
      </nuxt-link>
      <v-divider></v-divider>
    </div>
  </div>
</template>


<script>
export default {
  layout: "master",
  async asyncData(context) {
    const { $content } = context;
    const articles = await $content("blog").sortBy("createdAt", "desc").fetch();
    return {
      articles,
    };
  },
};
</script>

<style scoped>
.prys_writings a {
  text-decoration: none !important;
}
</style>