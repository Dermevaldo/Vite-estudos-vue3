<script LANG="ts">
export default {
  data() {
    return {
      color: 'red',
      count: 10,
    };
  },
};
</script>

<template>
  <div style="" @click="count += 10">
    {{ count }}
  </div>
</template>

<style scoped>
div {
  background-color: blue;
  width: 50px;
  height: v-bind('count');
  color: white;
  top: ;
}
</style>
