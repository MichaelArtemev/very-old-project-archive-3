<template>
  <div class="team">
    <div class="team__content">
      <div class="team__info">
        <h1>Our Team</h1>
        <p>meet those who will help your business</p>
      </div>
      <div class="team__slider" >
         <swiper ref="mySwiper" :options="swiperOptions">
          <swiper-slide>
            <div class="team__content2">
              <div class="team__img">
                <img src="../assets/team/s1.jpg" alt="">

              </div>
              <div class="team__i">
                <h1>Jack Torn</h1>
                <p>Data Scientist and Lead Analyst</p>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="team__content2">
              <div class="team__img">
                <img src="../assets/team/s2.jpg" alt="">

              </div>
              <div class="team__i">
                <h1>Jakob Uorhost</h1>
                <p>account Manager</p>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="team__content2">
              <div class="team__img">
                <img src="../assets/team/s4.jpg" alt="">

              </div>
              <div class="team__i">
                <h1>Nikole Trotsky</h1>
                <p>recruiting specialist</p>
              </div>
            </div>
          </swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
      </div>
      <div class="team__nav">
        <div><h1 @click="slidePrev">previous</h1></div>
        <div><h1 @click="slideNext">next</h1></div>
      </div>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper';
import 'swiper/swiper-bundle.css';

  export default {
    components: {
      Swiper,
      SwiperSlide
    },
    directives: {
      swiper: directive
    },
  data(){
    return{
      swiperOptions: {
        loop: true,
          // Some Swiper option/callback...
      }
    }
  },
  methods:{
    slideNext(){
      this.swiper.slideNext();
    },
    slidePrev(){
      this.swiper.slidePrev();
    }
  },
  computed: {
    swiper() {
      return this.$refs.mySwiper.$swiper;
    }
  },
  mounted() {
      console.log('Current Swiper instance object', this.swiper)
  }
}
</script>

<style lang="scss" scoped>


.team{
  width: 100%;
  color: #061e37;
  padding-top: 50px;
}
.team__info{
  p{
    font-size: 0.8em;
    opacity: 0.8;
    margin-bottom: 100px;
  }
}
.team__content2{
  display: flex;
  justify-content: center;
  flex-direction: column;
  text-align: center;
  margin-bottom: 30px;
  img{
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    box-shadow: 0 0 10px rgba(0,0,0,0.5);
  }
}
.team__img{
  display: flex;
  justify-content: center;
  margin-bottom: 50px;
}
.team__nav{
  display: flex;
  justify-content: center;
  justify-content: space-around;
  margin-top: 20px;
  margin-bottom: 50px;
  cursor: pointer;
  h1{
  border-bottom: 2px solid #061e37;

  }
}
</style>