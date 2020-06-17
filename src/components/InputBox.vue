<template>
  <div>
    <input type="text" placeholder="Skill" v-model="skill" />
    <div>{{skill}}</div>
  </div>
</template>

<script>
export default {
  name: "InputBox",
  data() {
    return {
      skill: ""
    };
  }
};
</script>

<style>
</style>