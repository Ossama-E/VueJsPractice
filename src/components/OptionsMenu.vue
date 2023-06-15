<template>
  <div class="container">
    <button
      @click="storedClicked"
      :class="{ selected: this.clickedButton == 'Stored' }"
    >
      Stored Resources
    </button>
    <button
      @click="addClicked"
      :class="{ selected: this.clickedButton == 'Add' }"
    >
      Add a Resource
    </button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      clickedButton: '',
    };
  },
  methods: {
    addClicked() {
      this.clickedButton = 'Add';
      this.$emit('add-click', 'AddResources');
    },
    storedClicked() {
      this.clickedButton = 'Stored';
      this.$emit('store-click', 'StoredMenu');
    },
  },
};
</script>
<style>
button {
  background: gray;
  color: white;
  border-radius: 10px;
  padding: 10px;
  margin-right: 15px;
  font-size: 1rem;
}
.container {
  margin-top: 2%;
  border-radius: 10px;
  padding: 20px;
  background-color: white;
  box-shadow: 2px 2px 2px 3px rgba(0, 0, 0, 0.5);
}

.selected {
  background: purple;
}
</style>
