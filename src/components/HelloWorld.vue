<script setup>
import { ref } from "vue";

const isactive = ref(false);
function go() {
  isactive.value = !isactive.value;
  console.log(isactive.value);
}

// return { isactive };
</script>

<template>
  <div class="main" :class="{ active: isactive }">
    <el-button type="info" @click="go" style="float: right">go</el-button>
  </div>
</template>

<style scoped>
.active {
  transform: translateX(-90%);
}
.main {
  width: 300px;
  height: 300px;
  position: fixed;
  top: 300px;
  left: 0;
  background-color: antiquewhite;
  transition: all 0.3s ease;
}
</style>
