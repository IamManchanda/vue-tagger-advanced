<template>
  <div id="app">
    <h2>Vue Tagger Advanced</h2>
    <div class="my-component">
      <vue-tagger-advanced 
        :tags="tags" 
        @change="logTags" 
        :placeholder="'Enter a tag...'" 
        :delimiter="','"></vue-tagger-advanced>
    </div>
  </div>
</template>

<script>
import VueTaggerAdvanced from './components/VueTaggerAdvanced.vue';

export default {
  name: 'app',
  components: {
    VueTaggerAdvanced,
  },
  data() {
    return {
      tags: [
        { name: 'JavaScript', selected: true },
        { name: 'Ruby', selected: false },
        { name: 'PHP', selected: true },
        { name: 'Crystal', selected: true },
        { name: 'Python', selected: false },
      ],
    };
  },
  methods: {
    logTags(tags) {
      console.log(tags);
    },
  },
};
</script>

<style lang="scss">
</style>
