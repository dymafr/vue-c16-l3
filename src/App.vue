<template>
  <div class="p-20">
    <div class="mb-20 d-flex w100 justify-content-center align-items-center">
      <button class="btn btn-primary mr-20" @click="selectedComponent = 'A'">
        Composant A
      </button>
      <button class="btn btn-primary" @click="selectedComponent = 'B'">
        Composant B
      </button>
      <Transition>
        <Component :is="components[selectedComponent]" />
      </Transition>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import type { Component as C } from 'vue';
import A from './A.vue';
import B from './B.vue';

const show = ref(true);
</script>

<style lang="scss">
@import './assets/scss/base.scss';
</style>
