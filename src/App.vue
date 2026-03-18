<template>
  <ul>
    <learning-resource></learning-resource>
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
