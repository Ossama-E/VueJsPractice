<template>
  <div class="center-container">
    <div class="title">{{ title }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Resource Page',
    };
  },
};
</script>

<style scoped>
.center-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 15vh;
  background: purple;
  color: white;
  font-size: 1.5rem;
  border-radius: 10px;
  text-align: center;
  font-weight: 600;
}

.title {
  padding: 10px 0;
}
</style>
