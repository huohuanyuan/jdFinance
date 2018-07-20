<template>
    <section :class="cname">
        <swiper :options="options">
            <swiper-slide v-for="item in items" :key="item.href">
                
            </swiper-slide>
        </swiper>
    </section>
</template>
<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  components: {
    swiper,
    swiperSlide
  },
  props: {
    options: {
      type: Object,
      default() {
        return {
            autoplay:true,
            loop:true,
            pagination:{
                el:".swiper-pagination"
            }
        };
      }
    },
    items:{
        type:Array,
        default(){
            return []
        }
    }
  },
  data() {
    return {
      cname: "swiper"
    };
  }
};
</script>
<style lang="scss" scoped>
@import "~swiper/dist/css/swiper.css";
</style>