<script setup>

</script>

<template>
  <div id="main-content">
    <section id="hero">
      <div class="container">
        <div class="hero flex">
          <div class="left">
            <h1>Virtual healthcare  for you</h1>
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
    </section>
  </div>
</template>

<style scoped>
#main-content {
  background-image: url("../assets/img/main-dots.svg");
  background-repeat: no-repeat;
}
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
  font-size: 14px;
}

@media only screen and (max-width: 992px) {
  .left h1{
    font-size: 38px;
    line-height: 46px;
  }
}

@media only screen and (max-width: 768px) {
  .hero {
    position: relative;
    flex-flow: column;
    text-align: center;
    gap: 0;
  }
  .hero .right {
    position: absolute;
    opacity: 0.1;
    z-index: -3;
  }

  #main-content {
    background: none;
  }
}

</style>