<template>
  <h3>hihihi</h3>
  <form @submit.prevent="onSubmit">
    <input v-model="title" type="text" placeholder="title" required />
    <input
      v-model="description"
      type="text"
      placeholder="description"
      required
    />
    <input v-model="url" type="text" placeholder="url" required />
    <button type="submit">Submit</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      title: '',
      description: '',
      url: '',
    };
  },
  methods: {
    onSubmit() {
      this.$emit('submitted', this.title, this.description, this.url);
      this.title = '';
      this.description = '';
      this.url = '';
    },
  },
};
</script>
<style></style>
