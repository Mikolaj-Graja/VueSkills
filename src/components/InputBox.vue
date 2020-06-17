<template>
  <form action="sumbit" @submit.prevent="addSkill">
    <input type="text" placeholder="Skill" v-model="skill" />
    <button>Submit</button>
  </form>
</template>

<script>
export default {
  name: "InputBox",
  data() {
    return {
      skill: ""
    };
  },
  methods: {
    addSkill() {
      this.$emit("addNewSkill", this.skill);
      this.skill = "";
    }
  }
};
</script>

<style>
</style>