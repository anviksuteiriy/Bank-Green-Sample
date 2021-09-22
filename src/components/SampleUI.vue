<template>
  <div class="font-sans flex flex-col max-w-md m-auto shadow-lg rounded-bl-2xl rounded-br-2xl">
    <div class="relative">
      <VueSlickCarousel v-bind="settings" class="slider__container awards__container1-cert">
        <div class="single__slide" v-for="(image, index) in images" :key="index">
          <div class="image__container rounded-tl-2xl rounded-tr-2xl">
            <img :src="require('@/assets/' + image.image)" class="max-w-md m-auto" />
          </div>
        </div>
      </VueSlickCarousel>
      <Like class="absolute top-4 right-6 text-3xl" />
    </div>
    <div class="flex flex-col p-3 bg-white text-left pb-6 pt-4 border-b">
      <div class="flex items-center font-bold text-base" style="color: #606f7b">
        <span>DETACHED HOUSE</span>
        <span><i class="fas fa-circle mx-2" style="font-size: 4px"></i></span>
        <span>5Y OLD</span>
      </div>
      <div style="color: #2f3947" class="text-4xl">$750,000</div>
      <div style="color: #8795a1" class="text-base">742 Evergreen Terrace</div>
    </div>
    <div class="flex p-3 bg-white">
      <div class="flex items-center">
        <i class="fal fa-bed text-2xl mr-3" style="color: #8795a1"></i>
        <span style="color: #2f3947" class="text-lg font-medium mr-2">3</span>
        <div style="color: #8795a1" class="text-lg">Bedrooms</div>
      </div>
      <div class="flex items-center ml-12">
        <i class="fal fa-bath text-2xl mr-3" style="color: #8795a1"></i>
        <span style="color: #2f3947" class="text-lg font-medium mr-2">3</span>
        <div style="color: #8795a1" class="text-lg">Bathrooms</div>
      </div>
    </div>
    <div class="flex flex-col p-3 bg-gray-100 text-left rounded-bl-2xl rounded-br-2xl">
      <div class="font-bold text-sm" style="color: #606f7b">REALTOR</div>
      <div class="flex items-center mt-3">
        <img class="rounded-full h-14 object-cover w-14 mr-4" src="https://hairstylesweekly.com/images/2013/11/065848qpT.jpg" alt="">
        <div>
          <div style="color: #2f3947" class="text-base font-bold mr-2">Tiffany Heffner</div>
          <div style="color: #8795a1" class="text-base">(555) 555-4321</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
import Like from './Like.vue'
export default {
  name: 'SampleUI',
  components: {
    VueSlickCarousel,
    Like
  },
  data() {
    return {
      settings: {
        arrows: false,
        dots: true,
        infinite: true,
        autoplay: false,
        speed: 2500,
        slidesToShow: 1,
        slidesToScroll: 1,
        initialSlide: 0,
      },
      images: [
        {
          image: "images/image1.jpeg"
        },
        {
          image: "images/image2.jpeg"
        },
        {
          image: "images/image3.jpeg"
        },
        {
          image: "images/image4.jpg"
        },
        {
          image: "images/image5.jpg"
        },
        {
          image: "images/image6.jpg"
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
