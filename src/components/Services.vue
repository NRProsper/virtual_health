<script setup>
import ServiceCard from "@/components/ServiceCard.vue";

const services = [
  {
    img: "/src/assets/img/search.svg",
    title: "Search doctor",
    description: "Choose your doctor from thousands of specialist, general, and trusted hospitals"
  },
  {
    img: "/src/assets/img/pharmacy.svg",
    title: "Online pharmacy",
    description: "Buy  your medicines with our mobile application with a simple delivery system"
  },
  {
    img: "/src/assets/img/consultation.svg",
    title: "Consultation",
    description: "Free consultation with our trusted doctors and get the best recommendations"
  },
  {
    img: "/src/assets/img/detailed-info.svg",
    title: "Details info",
    description: "Free consultation with our trusted doctors and get the best recommendations"
  },
  {
    img: "/src/assets/img/emergency.svg",
    title: "Emergency care",
    description: "You can get 24/7 urgent care for yourself or your children and your" +
        "lovely family"
  },
  {
    img: "/src/assets/img/tracking.svg",
    title: "Tracking",
    description: "Track and save your medical history and health data "
  }
];
</script>

<template>
<section id="services">
  <div class="container">
    <div class="services">
      <div class="top">
        <h2>Services</h2>
        <p>We provide to you the best choices for you. Adjust it to your health needs and make sure your undergo treatment with our highly qualified doctors you can consult with us which type of service is suitable for your health</p>
      </div>
      <div class="bottom">
        <ServiceCard
            v-for="(service, index) in services"
            :key="index"
            :img="service.img"
            :title="service.title"
            :description="service.description"
        />
      </div>
      <div class="serv_cta">
        <a href="" class="btn btn-outline">Learn more</a>
      </div>
    </div>
  </div>
</section>
</template>

<style scoped>
#services {
  background-image: url("../assets/img/vector-1.svg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: top;
}

.bottom {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.services {
  margin-top: 40px;
}

.services .top {
  text-align: center;
  margin-bottom: 40px;
}

.bottom {
  margin-bottom: 40px;
}

.top h2 {
  color: var(--vh-headers);
  position: relative;
  padding: 8px 0;
  margin-bottom: 20px;

  display: flex;
  align-items: center;
  justify-content: center;
}

.top h2::after {
  content: "";
  position: absolute;
  bottom: 0;
  width: 40px;
  height: 3px;
  background: var(--vh-headers);
}

.serv_cta {
  text-align: center;
  margin-top: 10px;
}

@media only screen and (max-width: 768px) {
  .bottom {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media only screen and (max-width: 576px) {
  .bottom {
    grid-template-columns: repeat(1, 1fr);
  }
}

</style>