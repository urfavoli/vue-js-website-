<template>
  <span ref="root" class="inline-block" style="clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);">
    <slot></slot>
  </span>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import SplitType from 'split-type';
import gsap from 'gsap';

const root = ref();

onMounted(() => {
  const text = new SplitType(root.value, { types: 'chars' });
  gsap.from(text.chars, {
    duration: 0.7,
    ease: 'power3.out',
    y: '110%',
    stagger: 0.02,
    delay: 0.1
  });
});
</script>
