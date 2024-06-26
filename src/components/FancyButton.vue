<script setup>
defineProps({
  url: String
})
</script>

<template>
  <a :href="url" class="btn flex justify-between">
    <slot>
      Learn more
    </slot>
  </a>
</template>

<style scoped>
a {
  display: inline-block;
  cursor: pointer;
  transition: background-color 0.3s ease-in-out;
}

.btn {
  padding: 6px 16px;
  border-radius: 18px;
}

.btn-outline {
  border: 1px solid var(--vh-primary-blue);
  color: var(--vh-primary-blue);
  background: transparent;
}

.btn-primary {
  background: var(--vh-primary-blue);
  color: #ffffff;
}

.btn-primary:hover {
  background-color: rgb(37, 103, 194);
}

.btn-outline:hover {
  background-color: var(--vh-primary-blue);
  color: #ffffff;
}
</style>