<template>
  <header>
    <div style="display: flex">
      <svg
        width="50px"
        height="50px"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 261.76 226.69"
      >
        <path
          d="M161.096.001l-30.225 52.351L100.647.001H-.005l130.877 226.688L261.749.001z"
          fill="#41b883"
        />
        <path
          d="M161.096.001l-30.225 52.351L100.647.001H52.346l78.526 136.01L209.398.001z"
          fill="#34495e"
        />
      </svg>
      <h1>{{ title }}</h1>
    </div>
    <Button
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'CLOSE' : 'ADD TASK'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./Button";

export default {
  name: "Header",
  props: {
    title: String,
    showAddTask: Boolean,
  },
  components: {
    Button,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
