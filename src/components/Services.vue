<template>
  <div class="services" id="servicesId">
    <div class="services__content">
      <div class="services__info">
        <h1>Services</h1>
        <p>we use the analytical information department <br/> for the best results and with the best specialists</p>
      </div>
      <div class="services__row">
        <div class="services__col" ref="s1">
          <div class="services__inner-col">
            <img class="s1" src="../assets/services/1.png" alt="">            
            <h3>Statistics</h3>
            <img  class="ss1" src="../assets/services/6.png" alt="" @click="openCloseS1">
          </div>
          <div class="services__inner-col2 services__inner-col2v" ref="ss1">
            <img src="../assets/services/i1.jpg" alt="">
            <p>we use the analytical information department <br/> for the best results and with the best specialists</p>
          </div>
        </div>

        <div class="services__col" ref="s2">
          <div class="services__inner-col">
            <img  class="s1" src="../assets/services/2.png" alt="">
            <h3>Inbox</h3>
            <img  class="ss1" src="../assets/services/6.png" alt=""  @click="openCloseS2">
          </div>
          <div class="services__inner-col2" ref="ss2">
            <img src="../assets/services/i2.jpg" alt="">
            <p>constantly developing communication between partners <br/> for the best results and with the best specialists</p>
          </div>
        </div>

        <div class="services__col" ref="s3">
          <div class="services__inner-col">
            
            <img  class="s1" src="../assets/services/3.png" alt="">
            <h3>Team</h3>
            <img  class="ss1" src="../assets/services/6.png" alt=""  @click="openCloseS3">
          </div>
          <div class="services__inner-col2" ref="ss3">
            <img src="../assets/services/i3.jpg" alt="">
            <p>one of the best teams on the market, constantly developing</p>
          </div>
        </div>

        <div class="services__col" ref="s4">
          <div class="services__inner-col">
            <img class="s1" src="../assets/services/4.png" alt="">
            <h3>Settings</h3>
            <img  class="ss1" src="../assets/services/6.png" alt=""  @click="openCloseS4">
          </div>
          <div class="services__inner-col2" ref="ss4">
            <img src="../assets/services/i4.jpg" alt="">
            <p>customize everything for yourself as you like</p>
          </div>
        </div>

        <div class="services__col" ref="s5">
          <div class="services__inner-col">
            <img  class="s1" src="../assets/services/5.png" alt="">
            <h3>Feed</h3>
            <img  class="ss1" src="../assets/services/6.png" alt=""  @click="openCloseS5">
          </div>
          <div class="services__inner-col2" ref="ss5">
            <img src="../assets/services/i5.png" alt="">
            <p>constantly in touch and give access to all important analytics</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data(){
      return{
        ss1: false,
        ss2: false,
        ss3: false,
        ss4: false,
        ss5: false

      }
    },
    methods:{
      openCloseS1(){
        if(this.ss1){
          this.$refs.ss1.style.display = "none";
          this.ss1 = false;
        }else{
          this.$refs.ss1.style.display = "flex";
          this.ss1 = true;
        }        
      },
      openCloseS2(){
        if(this.ss2){
          this.$refs.ss2.style.display = "none";
          this.ss2 = false;
        }else{
          this.$refs.ss2.style.display = "flex";
          this.ss2 = true;
        }        
      },
      openCloseS3(){
        if(this.ss3){
          this.$refs.ss3.style.display = "none";
          this.ss3 = false;
        }else{
          this.$refs.ss3.style.display = "flex";
          this.ss3 = true;
        }        
      },
      openCloseS4(){
        if(this.ss4){
          this.$refs.ss4.style.display = "none";
          this.ss4 = false;
        }else{
          this.$refs.ss4.style.display = "flex";
          this.ss4 = true;
        }        
      },
      openCloseS5(){
        if(this.ss5){
          this.$refs.ss5.style.display = "none";
          this.ss5 = false;
        }else{
          this.$refs.ss5.style.display = "flex";
          this.ss5 = true;
        }        
      }
    }
  }
</script>

<style lang="scss" scoped>
.services{
  width: 100%;
  margin-bottom: 90px;
}
.services__info{
  p{
    opacity: 0.4;
    margin-top: 20px;
    margin-bottom: 140px;
  }
}
.services__row{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  justify-self: center;
  justify-content: center;
}
.services__col{
   box-shadow: 0 0 10px rgba(0,0,0,0.2);
   border-radius: 5px;
   padding: 5px 30px;
}
.services__inner-col{
  display: flex;
  justify-content: space-between;  
  align-content: center;
  align-items: center;
  margin-bottom: 40px;
}
.services__inner-col{
  img{
    width: 15px;
    height: 10px;
  }
}
.services__col{
  width: 650px;
  transition: 1s;
}
.services__inner-col2{
  display: flex;
  align-items: center;
  align-content: center;
  transition: 1s;
  display: none;
  p{
    opacity: 0.4;
    margin-left: 20px;
  }
  margin-bottom: 20px;
  img{
    width: 250px;
    height: 150px;
    border-radius: 5px;
    object-fit: cover;
  }
}
.services__col:not(:last-child){
  margin-bottom: 5px;
}
.services__inner-col{
  h3{
    color: #061e37;
  }
}
.services__inner-col2v{
  display: flex;
}
@media (max-width: 982px){
  .services{
  margin-top: 600px;

  }
}
@media (max-width: 694px){
  .services__col{
    width: 450px;
  }
}
@media (max-width: 484px){
  .services__col{
    width: 250px;
  }
  .services__inner-col2{
    flex-direction: column;
  }
}
.services{
  padding-left: 30px;
  padding-right: 30px;

}
@media (max-width: 650px){
  .services{
    margin-top: 650px;

  }
}
@media (max-width: 413px){
  .services{
    margin-top: 720px;

  }
}
@media (max-width: 411px){
  .services{
    margin-top: 820px;

  }
}
</style>