<script setup>
import FancyButton from "@/components/FancyButton.vue";
import ArrowDown from "vue-material-design-icons/ArrowDownThin.vue";
</script>

<template>
<section id="download">
  <div class="container">
    <div class="download-container flex">
      <div class="left">
        <h2>Download our <br />
          mobile apps</h2>
        <p>Our dedicated patient engagement app and
          web portal allow you to access information instantaneously (no tedious form, long calls,
          or administrative hassle) and securely</p>
        <div>
          <FancyButton class="btn-outline">
             Download
<!--            <ArrowDown />-->
          </FancyButton>
        </div>
      </div>
      <div class="right">
        <img src="../assets/img/illustration-3.png" alt="Lean More Image">
      </div>
    </div>
  </div>
</section>
</template>

<style scoped>
#download {
  margin: 60px 0;
}

.left h2 {
  font-size: 2rem;
  position: relative;
  padding: 8px 0;
  margin-bottom: 20px;
}

.left h2::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 40px;
  height: 3px;
  background-color: var(--vh-headers);
}

.left div:last-of-type {
  margin-top: 20px;
}

@media only screen and (max-width: 768px) {
  .download-container {
    position: relative;
    flex-flow: column;
    text-align: center;
  }

  .download-container .right {
    position: absolute;
    opacity: 0.2;
    z-index: -3;
  }

  .left h2::after {
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
  }

}
</style>