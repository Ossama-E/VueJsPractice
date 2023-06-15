<template>
  <div class="form-container">
    <h3>Add Resource</h3>
    <form @submit.prevent="onSubmit">
      <div class="form-group">
        <label for="title">Title</label>
        <input
          v-model="title"
          type="text"
          id="title"
          placeholder="Enter title"
          required
        />
      </div>
      <div class="form-group">
        <label for="description">Description</label>
        <input
          v-model="description"
          type="text"
          id="description"
          placeholder="Enter description"
          required
        />
      </div>
      <div class="form-group">
        <label for="url">URL</label>
        <input
          v-model="url"
          type="text"
          id="url"
          placeholder="Enter URL"
          required
        />
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
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

<style scoped>
.form-container {
  width: 100%;
  max-width: 500px;
  margin: 0 auto;
  padding: 20px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}

.form-group {
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
}

label {
  font-weight: bold;
  margin-bottom: 5px;
}

input[type='text'] {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: purple;
  color: white;
  cursor: pointer;
  font-size: 16px;
}

button:hover {
  background-color: darkmagenta;
}
</style>
