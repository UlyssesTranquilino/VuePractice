<template>
  <div class="home">
    HOME
    <p ref="paragraph">My nbame is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">CLIcK me</button>
    <button @click="age++">Add 1 to age</button>
    <input type="text" v-model="name" />
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const paragraph = ref<HTMLElement | null>(null);

const name = ref<string>("ulysses");
const age = ref<number>(19);

const handleClick = (): void => {
  name.value = "yulsz";
  age.value = 20;
};
</script>
