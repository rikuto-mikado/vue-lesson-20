<template>
  <ul>
    <!-- v-for: loops over storedResources array, each item is available as "res" -->
    <!-- : (colon) = v-bind shorthand. evaluates the value as JS and passes res properties as props -->
    <learning-resource
      v-for="res in storedResources"
      :key="res.id"
      :title="res.title"
      :description="res.description"
      :link="res.link"
    ></learning-resource>
  </ul>
</template>

<script>
import LearningResource from './components/learning-resources/LearningResource.vue';

export default {
    components: {
        // You can also use shorthand: LearningResource
        LearningResource : LearningResource
    },
    data() {
        return {
            storedResources: [
                { 
                    id: 'official-guide', 
                    title: 'Official Guide', 
                    description: 'The Official Vue documentation.',
                    link: 'https://vuejs.org'
                },
                { 
                    id: 'google', 
                    title: 'Google', 
                    description: 'Learn to google...',
                    link: 'https://google.org'
                }
            ]
        };
    },

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>