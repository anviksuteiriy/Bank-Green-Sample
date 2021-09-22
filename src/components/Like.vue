<template>
  <button class="like focus:outline-none" @click.prevent="like">
    <transition
      enter-active-class="transition ease-out duration-300"
      enter-class="transform opacity-0 scale-300"
      enter-to-class="transform opacity-100 scale-100"
      leave-active-class="transition ease-in duration-300"
      leave-class="transform opacity-100 scale-100"
      leave-to-class="transform opacity-0 scale-300"
      mode="out-in"
    >
      <div v-if="!isLiked" key="like">
        <i class="far fa-heart text-white"></i>
      </div>
      <div v-else key="unlike">
        <i class="fas fa-heart text-white"></i>
      </div>
    </transition>
  </button>
</template>

<script>
export default {
  data() {
    return {
      isLiked: false
    }
  },
  methods: {
    like() {
      this.isLiked = !this.isLiked 
    }
  }
}
</script>

<style lang="css" scoped></style>
