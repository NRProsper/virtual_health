<script setup>
const props = defineProps({
  img: String,
  title: String,
  description: String
})
</script>

<template>
  <div class="card">
    <div class="card-top">
      <img :src="props.img" :alt="props.title + ' image '">
    </div>
    <div class="card-bottom">
      <h3>{{props.title}}</h3>
      <p>{{props.description}}</p>
    </div>
  </div>
</template>

<style scoped>
.card {
  border-radius: 20px;
  background: #ffffff;
  padding: 24px;
  //box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  border: 1px solid var(--vh-nav-text);
}

.card img{
  width: 46px;
  height: 46px;
  margin-bottom: 10px;
}

.card-bottom h3 {
  margin-bottom: 10px;
}

</style>