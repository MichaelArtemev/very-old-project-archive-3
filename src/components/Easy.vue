<template>
  <div class="easy">


    


    <div class="easy__content">
      <div class="easy__info">
        <h1>Easy & Useful</h1>
        <h4>Project Management Tool</h4>
        <p>tools tested by people and time</p>
      </div>
      <div class="easy__row">
        <div class="easy__col">
          <img src="../assets/easy/1.png" alt="">
          <h2>Timings</h2>
          <p>Follow all convenient information</p>
        </div>
        <div class="easy__col">
          <img src="../assets/easy/2.png" alt="">
          <h2>Support</h2>
          <p>24/7 support and high quality</p>          
        </div>
        <div class="easy__col">
          <img src="../assets/easy/3.png" alt="">
          <h2>Prof team</h2> 
          <p>A team of top-level specialists</p>              
        </div>
      </div>
      <a href="/#contactId"><button class="btn">JOIN NOW</button></a>
      <div class="easy__row2">
        <div class="easy__col2 easy__col2-1">
          <div class="easy__col2-img">
            <img src="../assets/easy/4.png" alt="">
          </div>
          <div class="easy__col2-info">
            <h2>12000+</h2>
            <h2>Bussines</h2>
          </div>
        </div>
        <div class="easy__col2 easy__col2-2">
          <div class="easy__col2-img">
            <img src="../assets/easy/5.png" alt="">
          </div>
          <div class="easy__col2-info">
            <h2>60000+</h2>
            <h2>Downloads</h2>
          </div>
        </div>
        <div class="easy__col2 easy__col2-3">
          <div class="easy__col2-img">
            <img src="../assets/easy/6.png" alt="">
          </div>
          <div class="easy__col2-info">
            <h2>30000+</h2>
            <h2>Free installs</h2>
          </div>
        </div>
        <div class="easy__col2 easy__col2-4">
          <div class="easy__col2-img">
            <img src="../assets/easy/7.png" alt="">
          </div>
          <div class="easy__col2-info">
            <h2>40000+</h2>
            <h2>Pro users</h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    methods:{
      getPop(){
        this.$refs.pop.style.display = "flex";
      },
      closePop(){
        this.$refs.pop.style.display = "none";
      },
       getAlert(){
        alert("Thank you");
        this.closePop();
      }
    }
  }
</script>

<style lang="scss" scoped>
.easy{
  width: 100%;
  height: 955px;
  color: black;
  font-family: "Lato" sans-serif;
}
.easy__content{
}
.easy__info{
  margin-top: 50px;
  margin-bottom: 50px;
  h4{
    opacity: 0.4;
  }
  p{
    opacity: 0.4;
  }
}
.easy__row{
  display: flex;
  justify-content: center;
  margin-bottom: 60px;
  margin-top: 150px;
  justify-content: space-evenly;
  flex-wrap: wrap;  
}
.easy__col{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  align-items: center;
  h2{
    margin-bottom: 10px;
  }
  p{
    opacity: 0.4;
  }
  img{
    width: 60px;
    height: 70px;
    margin-bottom: 20px;
  }
}
.btn{
  background-color: #1de9b6;
  border: none;
  padding: 20px 40px;
  color: white;
  font-weight: bold;
  cursor: pointer;
  margin-bottom: 180px;
}
.easy__row2{
  display: flex;
  justify-content: center;
  justify-content: space-evenly;
}
.easy__col2-4{
  background-color: #ea80fc;
}
.easy__col2-3{
  background-color: #b388ff;
}
.easy__col2-2{
  background-color: #82b1ff;
}
.easy__col2-1{
  background-color: #80d8ff;
}
.easy__col2{
  width: 25%;
  display: flex;
  justify-content: center;
  padding-top: 50px;
  padding-bottom: 50px;
}
.easy__col2-info{
  color: white;
  margin-left: 40px;
}
@media (max-width: 981px) {
  .easy__row2{
    flex-direction: column;
  }
  .easy__col2{
    width: 100%;
  }
}
@media (max-width: 383px){
  .easy__col{
    margin-bottom: 20px;
  }
}



</style>