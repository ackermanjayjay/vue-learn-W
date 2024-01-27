<script setup>
import { ref } from "vue";

const number1 = ref(0);
const number2 = ref(0);
const result = ref(0);
const addition = () => {
  result.value = +number1.value + +number2.value;
};
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
    <button
      class="btn btn-accent"
      type="submit"
      @click="addition"
      :disabled="!number1 || !number2"
    >
      Tambah
    </button>
    <p>
      Result:
      {{ result }}
    </p>
  </div>
</template>
