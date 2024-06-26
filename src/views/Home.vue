<script setup>

import FancyButton from "@/components/FancyButton.vue";
</script>

<template>
  <section id="main-content">
    <div class="container">
      <div class="hero flex">
        <div class="left">
          <h1>Virtual healthcare  for you</h1>
          <p>Trafalgar provides progressive, and affordable
            <br/>healthcare, accessible on mobile and online
            for everyone</p>
          <div class="cta">
            <FancyButton class="btn-primary">
              Consult today
            </FancyButton>
          </div>
        </div>
        <div class="right">
          <img src="../assets/img/main-illustration.png" alt="">
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
#main-content {
  background-image: url("../assets/img/main-dots.svg");
  background-repeat: no-repeat;
  //height: calc(100vh - 80px);
}

#main-content .container {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero {
  gap: 50px;
  margin: 40px 0;
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
    opacity: 0.2;
    z-index: -3;
  }

  #main-content {
    background: none;
  }
}

</style>