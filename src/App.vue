<template>
  <div>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Libre+Franklin:wght@200;400;600&display=swap"
      rel="stylesheet"
    />
    <TheHeader />
    <!-- <OptionsMenu /> -->
    <options-menu
      @add-click="setSelected('AddResource')"
      @store-click="setSelected('StoredMenu')"
    ></options-menu>
    <component
      @submitted="submitAction"
      :is="selectedComp"
      :resources="resources"
    ></component>
  </div>
</template>

<script>
// import ResourcesMenu from './components/ResourcesMenu.vue';
import StoredMenu from './components/StoredMenu.vue';
import TheHeader from './components/TheHeader.vue';
import OptionsMenu from './components/OptionsMenu.vue';
import AddResource from './components/AddResource.vue';

export default {
  components: {
    TheHeader,
    OptionsMenu,
    StoredMenu,
    AddResource,
  },
  data() {
    return {
      selectedComp: '',
      resources: [
        {
          title: 'google',
          description: 'a resource',
          attach: 'google.com',
        },
        {
          title: 'google',
          description: 'a resource',
          attach: 'google.com',
        },
      ],
    };
  },``
  methods: {
    submitAction(title, description, url) {
      this.resources.push({ title, description, url });
    },
    setSelected(comp) {
      this.selectedComp = comp;
    },
  },
};
</script>

<style>
* {
  font-family: 'Libre Franklin', sans-serif;
}
</style>
