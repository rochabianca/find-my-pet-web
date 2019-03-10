<template>
  <div class="home">
    <Navbar />
    <PetCarrousel />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import PetCarrousel from "@/components/PetCarrousel";

export default {
  name: "home",
  components: {
    Navbar,
    PetCarrousel
  }
};
</script>
