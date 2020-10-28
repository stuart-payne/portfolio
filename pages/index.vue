<template>
  <div class="mainContainer">
    <h1>Stuart Payne</h1>
    <h2>Software Developer</h2>
    <p>
      I'm software developer from the UK focused on web development. Experienced
      in both front and back end languages/frameworks. Have also dabbled in game
      development with the Unity game engine.
    </p>
    <div class="techContainer">
      <TechDisplay
        v-for="tech in techs"
        :key="tech.experience"
        :experience="tech.experience"
        :techs="tech.techs"
      />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      techs: [
        {
          experience: 'Experienced',
          techs: ['JavaScript', 'Node', 'HTML', 'CSS', 'C#'],
        },
        {
          experience: 'Intermediate',
          techs: ['Laravel', 'PHP', 'Vue', 'React', 'TypeScript'],
        },
        {
          experience: 'Basic',
          techs: ['Unity', 'ASP.net', 'MySQL', 'MongoDB'],
        },
      ],
    }
  },
})
</script>

<style scoped>
.mainContainer {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.techContainer {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: center;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
