<template>
  <div class="contact" id="contactId">    
    <div class="contact__content">
      <div class="contact__i">
        <h1>Contact Us</h1>
        <p>We will contact you shortly</p>
      </div>
      <div class="contact__form">
        <div class="contact__input-row">
          <input type="text" placeholder="First Name" class="i1">
          <input type="text" placeholder="Last Name">
        </div>
        <div class="contact__input-row">
          <input type="text" placeholder="Email" class="i1">
          <input type="text" placeholder="Phone">
        </div>
      </div>
      <div class="contact__msg">
        <textarea placeholder="Message" name="area" id="m" cols="30" rows="10"></textarea>
      </div>
      <div class="contacnt__check">
        <input type="checkbox"> <p>*subscribe to the newseller</p>
        <button class="btn" @click="getAlert">SEND</button>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    methods:{
      getAlert(){
        alert("Thank you")
      }
    }
  }
</script>

<style lang="scss" scoped>
.contact{
  width: 100%;
  padding-top: 100px;
  background-color: #fafafa;
  color: #061e37;
}
.contact__i{
  margin-bottom: 50px;
}
.contact__input-row{
  display: flex;
  justify-content: center;
  padding: 15px;
}
.i1{
  margin-right: 5px;
}
input{
  border: 1px solid black;
  padding: 10px 15px;
  border-radius: 5px;
}
#m{
  width: 55%;
  padding: 50px;
}
.btn{
  border: none;
  padding: 10px 40px;
  background-color: #1de9b6;
  color: white;
  box-shadow: 0 0 10px rgba(0,0,0,0.5);
  margin-bottom: 50px;
}
.contacnt__check{
  p{
    margin-bottom: 20px;
  }
}
@media (max-width: 460px){
  .contact__input-row{
    flex-direction: column;
  }
  .i1{
    margin-right: 0px;
    margin-bottom: 20px;
  }
}

</style>