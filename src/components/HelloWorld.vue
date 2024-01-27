<script setup>
import { ref } from "vue";

const number1 = ref(0);
const number2 = ref(0);

</script>
<template>
  <div
    class="grid grid-rows-4 grid-flow-col gap-4 justify-center mx-5 mb-5 mt-5"
  >
    <div>
      <span class="badge">Input number here here</span>
      <input
        placeholder="Type here"
        class="input input-bordered w-full max-w-xs"
        v-model="number1"
        type="text"
      />
    </div>
    <div>
      <input
        placeholder="Type here"
        class="input input-bordered w-full max-w-xs"
        v-model="number2"
        type="text"
      />
    </div>
    <p>Result text is: {{ (+number1) + (+number2) }}</p>
  </div>
</template>
