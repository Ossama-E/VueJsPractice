<template>
  <div>
    <h2>{{ title }}</h2>
    <h3>{{ description }}</h3>
    <p>attach</p>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  // props: { title: String, description: String, attach: String },
  props: ['title', 'description', 'attach'],
  methods: {},
};
</script>
<style></style>
