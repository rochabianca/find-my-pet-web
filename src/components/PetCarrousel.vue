<template>
  <div class="container pet-carrolsel mt-5">
    <carousel :perPage="1" paginationActiveColor="#06173b">
      <slide v-for="pet in pets" :key="pet.id">
        <PetItem :pet="pet" />
      </slide>
    </carousel>
  </div>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";
import PetItem from "@/components/PetItem";
import Mariana from "@/assets/images/Examples/mariana-negresco.png";
import Tobias from "@/assets/images/Examples/4.jpg";
import Gaster from "@/assets/images/Examples/8.jpg";

export default {
  components: {
    Carousel,
    Slide,
    PetItem
  },
  data() {
    return {
      pets: [
        {
          id: "1",
          name: "Tobias",
          image: Tobias,
          description:
            "Este é Tobias, um filhotinho muito brincalhão, só falta ele para ser adotado",
          sendBy: "FindMyPet App",
          tutor: {
            name: "Mariana Negresco",
            image: Mariana
          }
        },
        {
          id: "2",
          name: "Gaster",
          image: Gaster,
          description:
            "Me ajudem a encontrar um novo lar para o Gaster! Ele é um gatinho super dengoso e ama um carinhozin",
          sendBy: "FindMyPet Web",
          tutor: {
            name: "Janaina Monalisa",
            image: Mariana
          }
        }
      ]
    };
  }
};
</script>
