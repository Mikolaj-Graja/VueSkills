<template>
  <div id="app">
    <div>
      <h1>Page made with vue.js</h1>
      <h2>Skills</h2>
      <InputBox :skills="skills" @addNewSkill="addSkill($event)" />
      <div>New Skill is {{skill.skillName}}</div>
      <SkillsList v-bind:skills="skills" />
    </div>
  </div>
</template>

<script>
import InputBox from "./components/InputBox.vue";
import SkillsList from "./components/SkillsList.vue";

export default {
  name: "App",
  components: {
    InputBox,
    SkillsList
  },
  data() {
    return {
      skills: [
        { skillName: "Vue.js", id: 1 },
        { skillName: "React", id: 2 }
      ],
      skill: ""
    };
  },
  methods: {
    addSkill($event) {
      this.skill = {
        skillName: $event,
        id: this.skills.length + 1
      };
      this.skills.push(this.skill);
      console.log(this.skill);
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
h2 {
  font-weight: 500;
  text-transform: uppercase;
}
</style>
