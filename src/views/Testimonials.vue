<script setup>

</script>

<template>
<section id="testimonials">
  <div class="container">
    <div class="testimonial-container">
      <div class="top">
        <h2 class="flex">What our customers are saying</h2>
      </div>
      <div class="bottom flex justify-between">
        <div class="customer flex">
          <img src="../assets/img/grinch.jpeg" alt="Customer">
          <div class="customer-details">
            <h3>Edward Newgate</h3>
            <p>Founder Circle</p>
          </div>
        </div>
        <div class="testimony">
          <p><span>“</span>Our dedicated patient engagement app and<br />
            web portal allow you to access information <br /> instantaneously (no tedeous form, long calls, <br />
            or administrative hassle) and securely </p>
        </div>
      </div>
    </div>
  </div>
</section>
</template>

<style scoped>
#testimonials {
  margin: 90px 0;
}

.testimonial-container {
  border-radius: 24px;
  background: rgba(90, 152, 242, 1);
  padding: 50px 100px;
  position: relative;
  background-image: url("../assets/img/dots-2.svg");
  background-repeat: no-repeat;
}


.top h2 {
  position: relative;
  text-align: center;
  font-size: 2rem;
  color: rgba(255, 255, 255, 0.9);
  padding: 8px 0;
  margin-bottom: 60px;
}

.top h2::after {
  position: absolute;
  content: '';
  height: 3px;
  width: 40px;
  background: #ffffff;
  bottom: 0;
}

.testimony {
  color: rgba(255, 255, 255, 0.9);
  text-transform: none;
}

.customer img{
  height: 100px;
  width: 100px;
  border-radius: 50%;
  border: 2px solid #ffffff;
  margin-right: 20px;
}

.customer .customer-details h3 {
  color: #ffffff;
  font-size: 15px;
  margin-bottom: 10px;
}

.customer .customer-details p {
  font-size: 12px;
  color: rgba(255, 255, 255, 0.9);
}

.testimony {
  position: relative;
}

.testimony span {
  content: "";
  z-index: 0;
  opacity: 0.2;
  position: absolute;
  font-size: 320px;
  top: -120px;
  left: -50px;
}

@media only screen and (max-width: 992px) {
  .testimonial-container {
    padding-left: 50px;
    padding-right: 50px;
  }
}

@media only screen and (max-width: 768px) {
  .testimonial-container {
    padding: 20px 10px;
  }
  .bottom {
    gap: 30px;
    flex-flow: column;
  }

  .top h2 {
    padding-bottom: 20px;
  }
}

</style>