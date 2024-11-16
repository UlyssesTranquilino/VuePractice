<template>
  <div class="home">
    HOME
    <p ref="paragraph">My nbame is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">CLIcK me</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const paragraph = ref<HTMLElement | null>(null);

const name: string = "ulysses";
const age: number = 19;

const handleClick = (): void => {
  console.log("You clicked me! ", paragraph, paragraph.value);
  paragraph.value.classList.add("test");
  paragraph.value.textContent = "Hello ";
};
</script>
