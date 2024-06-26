<script setup>

import FancyButton from "@/components/FancyButton.vue";
</script>

<template>
<section id="learn-more">
  <div class="container">
    <div class="learn-more-container flex">
      <div class="left">
        <img src="../assets/img/illustration-2.png" alt="Lean More Image">
      </div>
      <div class="right">
        <h2>Leading healthcare <br /> providers</h2>
        <p>Trafalgar provides progressive, and affordable healthcare, accessible on mobile and online for everyone. To us, it’s not just work. We take pride
          in the solutions we deliver</p>
        <div>
          <FancyButton class="btn-outline">
            Learn More
          </FancyButton>
        </div>
      </div>
    </div>
  </div>
</section>
</template>

<style scoped>
#learn-more {
  margin: 60px 0;
}

.learn-more-container {
  gap: 50px;
}

.right h2 {
  font-size: 2rem;
  position: relative;
  padding: 8px 0;
  margin-bottom: 20px;
}

.right h2::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 40px;
  height: 3px;
  background-color: var(--vh-headers);
}

.right div {
  margin-top: 20px;
}

@media only screen and (max-width: 768px) {
  .learn-more-container {
    position: relative;
    flex-flow: column;
    text-align: center;
  }

  .right h2::after {
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
  }

  .learn-more-container .left {
    position: absolute;
    z-index: -3;
    opacity: 0.2;
  }

}
</style>