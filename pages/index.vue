<template>
  <div class="mainContainer">
    <h1 class="title">Stuart Payne</h1>
    <h2 class="subtitle">Software Developer</h2>
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
    <p>
      For examples of my code and projects which I have worked on click
      <nuxt-link class="pLink" to="/portfolio"><b>here</b></nuxt-link>
    </p>
    <p>To get in contact, send me an email at <b>paynestu@gmail.com</b></p>
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
          techs: ['TypeScript', 'Laravel', 'PHP', 'Vue', 'React'],
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

<style>
html {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  color: white;
}

.mainContainer {
  padding-top: 20px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.pLink {
  color: #97476f;
}

.mainContainer > * {
  margin: 30px 0px;
  padding: 10px;
}

.title {
  display: block;
  font-weight: 300;
  font-size: 100px;
  letter-spacing: 1px;
  margin-bottom: 10px;
}

.techContainer {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: flex-start;
  justify-content: center;
}

.subtitle {
  margin-top: 0px;
  font-weight: 300;
  font-size: 42px;
  word-spacing: 5px;
}

.links {
  padding-top: 15px;
}
</style>
