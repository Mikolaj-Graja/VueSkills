<template>
  <div>
    <ul>
      <li v-for="skill of skills" :key="skill.id">{{skill.skillName}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "SkillsList",
  props: ["skills"]
};
</script>

<style scooped>
ul {
  list-style-type: none;
}
</style>