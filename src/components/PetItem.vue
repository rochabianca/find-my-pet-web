<template>
  <div class="d-flex justify-content-center align-items-start pet">
    <img
      class="pet__image align-self-start"
      :src="pet.image"
      :alt="'Foto de ' + pet.name"
    />
    <div class="ml-md-5">
      <p class="pet__description">"{{ pet.description }}"</p>
      <div class="mt-3 mb-5 pet-tutor d-flex align-items-center">
        <img
          class="pet__tutor__image"
          :src="pet.tutor.image"
          :alt="'Foto de ' + pet.tutor.name"
        />
        <div class="ml-3 mb">
          <span class="pet__tutor__name">{{ pet.tutor.name }}</span>
          <div class="pet__sendBy">via {{ pet.sendBy }}</div>
        </div>
      </div>
      <button class="button button__primary">Adote {{ pet.name }}</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    pet: Object
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/variables.scss";

.pet {
  .pet__image {
    max-width: 500px;
  }
  .pet__description {
    font-size: 36px;
  }
  .pet__tutor__image {
    width: 60px;
  }
  .pet__tutor__name {
    font-size: 18px;
  }
  .pet__sendBy {
    font-size: 12px;
    color: $light-gray;
  }
}
</style>
