<template>
  <div class="resource-container">
    <h2>{{ title }}</h2>
    <h3>{{ description }}</h3>
    <a :href="attach" class="link" target="_blank">{{ attach }}</a>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: ['title', 'description', 'attach'],
  methods: {},
};
</script>

<style scoped>
.resource-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  background-color: #f5f5f5;
  margin: 1rem;
  padding: 1rem;
  border-radius: 5px;
  box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.1);
}

h2,
h3 {
  margin: 0;
}

h2 {
  color: #333;
}

h3 {
  color: #666;
}

.link {
  margin-top: 1rem;
  color: #007bff;
  text-decoration: none;
}
</style>
