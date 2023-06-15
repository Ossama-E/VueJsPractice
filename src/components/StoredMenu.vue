<template>
  <div>
    <ul>
      <li v-for="resource in resources" :key="resource.attach">
        <base-resource
          :title="resource.title"
          :attach="resource.attach"
          :description="resource.description"
        ></base-resource>
      </li>
    </ul>
  </div>
</template>
<script>
import BaseResource from './BaseResource.vue';
export default {
  components: {
    BaseResource,
  },
  data() {
    return {};
  },
  props: ['resources'],
  methods: {},
};
</script>
<style></style>

<!-- object has .attach, .title, .description -->
