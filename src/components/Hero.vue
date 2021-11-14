<template>
  <div class="hero" id="home">

  <div class="pop" ref="pop">
    <div class="pop__content">
      <div class="pop__f">
        <input type="text" placeholder="email">
        <button class="btnp" @click="getAlert">SEND</button>
        <h1 class="px" @click="closePop">X</h1>
      </div>
    </div>
  </div>



    <div class="nav">
      <div class="nav__logo">
        <img src="../assets/hero/4.png" alt="">
      </div>
      <nav>
        <ul>
          <a href="/#home"><li>Home</li></a>
          <a href="/#servicesId"><li>Service</li></a>
          <a href="/#contactId"><li>Contacts</li></a>
        </ul>
      </nav>      
    </div>

    <div class="main-content">
      <div class="main-content__row">
        <div class="main-content__col">
          <div class="main-content__left-content">
            <h1>we help with business!</h1>
            <p>we help with electronic financial management,<br/> help to manage and analyze information</p>
            <a href="/#contactId"><button class="btn">BUY NOW</button></a>
          </div>
        </div>
        <div class="main-content__col">
          <img src="../assets/hero/2.jpg" alt="">
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
.hero{
  width: 100%;
  height: 600px;
  background-image: url("../assets/hero/3.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  color: white;
}
.nav{
  position: fixed;
  left: 50%;
  color: white;
  text-shadow: black 0 0 2px;
  transform: translate(-50%);
  nav{
    letter-spacing: 1px;
    ul{
      display: flex;
      justify-content: center;
      padding-top: 40px;
      li:not(:last-child){
        margin-right: 20px;
        cursor: pointer;
      }
    }
  }
}
.main-content__row{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  padding-top: 90px;
}
.main-content__col{
  img{
    width: 450px;
    height: 350px;
    object-fit: cover;
  }
}
.main-content__col:not(:last-child){
  margin-right: 80px;
}
.main-content__left-content{
  text-align: left;
  h1{
    text-transform: uppercase;
    font-weight: bold;
    font-size: 2em;
    margin-bottom: 20px;
  }
  p{
    font-size: 0.7em;
    opacity: 0.8;
    margin-bottom: 40px;
  }
}
.main-content__left-content:not(:last-child){
  margin-bottom: 20px;
}
.btn{
  background-color: #061e37;
  border: none;
  color: white;
  padding: 15px 40px;
  cursor: pointer;
}
.nav__logo{
  position: absolute;
  color: black;
  top: 40px;
  left: -533px;
}
@media (max-width: 1313px) {
  .nav__logo{
    left: -433px;
  }
}
@media (max-width: 1097px) {
  .nav__logo{
    left: -233px;
  }
}
@media (max-width: 708px) {
  .nav__logo{
    display: none;
  }
}
@media (max-width: 700px) {
  .nav__logo{
    left: -0px;
    top: 85px;
  }
}
@media (max-width: 923px) {
  .main-content__left-content{
    margin-top: 90px;
    margin-bottom: 30px;
  }
  .main-content__col{
  img{
    width: 550px;
    height: 150px;
    object-fit: cover;
  }
}
}
@media (max-width: 585px) {
  .main-content__col{
  img{
    width: 350px;
    height: 150px;
    object-fit: cover;
  }
}
.main-content__col:not(:last-child){
  margin-right: 0px;
}
.main-content__left-content{
  text-align: center;
}
}
@media (max-width: 392px) {
  .main-content__col{
  img{
    width: 250px;
    height: 130px;
    object-fit: cover;
  }
}
}
.main-content__col{
  img{
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0,0,0,0.8);
  }
}


.pop{
    width: 100%;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.87);
    position: fixed;
    z-index: 99;
    display: none;
    justify-content: center;
    align-content: center;
  }
  .pop__f{
    width: 250px;
    height: 180px;
    border-radius: 5px;
    background-color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    align-content: center;
  }
  .pop__content{
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: center;
  }
  .btnp{
    border: none;
    padding: 10px 40px;
    cursor: pointer;
    background-color: #1de9b6;
    margin-top: 20px;
  }
  .px{
    color: black;
    cursor: pointer;
  }
  a{
    color: white;
    text-shadow: black 0 0 2px;
    text-decoration: none;
  }
  a:not(:last-child){
    margin-right: 20px;
  }
</style>