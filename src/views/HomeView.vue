<script setup>

</script>

<template>
  <div id="main-content">
    <div class="container">
      <div class="hero flex">
        <div class="left">
          <h1>Virtual healthcare <br /> for you</h1>
          <p>Trafalgar provides progressive, and affordable
            <br/>healthcare, accessible on mobile and online
            for everyone</p>
          <div class="cta">
            <a href="#" class="btn btn-primary">Consult today</a>
          </div>
        </div>
        <div class="right">
          <img src="../assets/img/main-illustration.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero {
  gap: 50px;
  margin-top: 40px;
}

.left {
  flex:1;
}

.right {
  flex: 1;
}

.left h1{
  color: var(--vh-headers);
  font-size: 48px;
  line-height: 56px;
  margin: 12px 0;
}

.left p {
  margin-bottom: 30px;
}

</style>