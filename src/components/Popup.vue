<template>
  <div class="pop" ref="pop">
    <div class="pop__content">
      <div class="pop__f">
        <input type="text" placeholder="email">
        <button class="btn" @click="getAlert">SEND</button>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    methods:{
      getAlert(){
        alert("Thank you");
        this.$refs.pop.style.display = "none";
      }
    }
  }
</script>

<style lang="scss" scoped>
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
    height: 150px;
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
  .btn{
    border: none;
    padding: 10px 40px;
    cursor: pointer;
    background-color: #1de9b6;
    margin-top: 20px;
  }
</style>