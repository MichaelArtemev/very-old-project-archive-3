<template>
  <div class="about">
    <div class="about__content">
      <div class="about__row">
        <div class="about__col about__col-inf">
          <h1>What our customershave <br> to say about us.</h1>
          <p>we always listen and understand</p>
          <a href="/#contactId"><button class="btn">GET STARTED</button></a>
        </div>
        <div class="about__col about__colaf">
          <div class="about__inner-col">
            <img src="../assets/about/2.png" alt="">
            <div class="about__inner-info">
              <h1>Watslav Nerko</h1>
              <p>the help was not appreciated, <br> I was able to increase my profits</p>
            </div>
          </div>
          <div class="about__inner-col">
            <img src="../assets/about/3.png" alt="">
            <div class="about__inner-info">
              <h1>Nadezhda Petrovna</h1>
              <p>raised an unprofitable business <br> and was able to improve its position in the market</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
.about{
  width: 100%;
  background-image: url("../assets/about/1.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  color: white;
  padding-top: 50px;
  padding-bottom: 50px;
  padding-left: 30px;
  padding-right: 30px;

}
.about__row{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
.about__col-inf{
  text-align: left;
  h1{
    margin-bottom: 20px;
  }
  p{
    margin-bottom: 50px;
    font-size: 0.8em;
    opacity: 0.8;
  }
}
.about__col:not(:last-child){
  margin-right: 120px;
}
.btn{
  border: none;
  padding: 20px 40px;
  color: white;
  background-color: #061e37;
  cursor: pointer;
}
.about__inner-col{
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 25px;
}
.about__inner-info{
  margin-left: 40px;
  background-color: white;
  color: #061e37;
  padding: 20px 50px;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
  p{
    font-size: 0.8em;
    opacity: 0.8;
  }
}
@media (max-width: 941px){
  .about__col-inf{
    text-align: center;
  }
  .about__col:not(:last-child){
  margin-right: 0px;
}
.about__col{
  margin-bottom: 50px;
}
}
@media(max-width: 400px){
  .about__inner-col{
    flex-direction: column;
    align-content: center;
    align-items: center;
  }
  .about__inner-info{
    margin-left: 0px;
  }
}
</style>