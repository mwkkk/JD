<template>
    <section class="swiper">
        <swiper :options="options" :not-next-tick="options.notNextTick">
            <swiper-slider v-for:"item in items" :key="item.href">
                <router-link to="{name:item.href}">
                    <img :src="item.src"/>
                </router-link>
            </swiper-slider>
            <div class="swiper-pagination" v-if="options.pagination"/>
        </swiper>
    </section>
</template>
<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
 
export default {
  components: {
    swiper,
    swiperSlide
  },
  props:{
      options:{
         type:Object,
         default(){
            return {
              autoplay:true,
              loop:true,
              pagination:{
                  el:'.swiper-pagination',
              },
              notNextTick:false
         }
      },
      items:{
          type:Array,
          default(){
              return []
          }
      }         
    }
  }
}
</script>
<style>
@import '~swiper/dist/css/swiper.css'

</style>