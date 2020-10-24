<template>
  <v-bottom-navigation :value="value" color="teal" grow>
    <v-btn to="/">
      <span>Home</span>

      <v-icon>mdi-home</v-icon>
    </v-btn>

    <v-btn to="/writings">
      <span>Writings</span>

      <v-icon>mdi-note</v-icon>
    </v-btn>
    <v-btn to="/projects">
      <span>Projects</span>

      <v-icon>mdi-briefcase</v-icon>
    </v-btn>

    <v-btn to="/projects">
      <span>Project</span>

      <v-icon>mdi-account</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>
<script>
export default {

  data: () => ({ value: 1 }),
};
</script>