<template lang="html">
    <div :class="$style.home">
        <h1>Home</h1>
<<<<<<< HEAD
        <input type="text" name="" value="" @keydown="get">
=======
        <input type="text" name="" value="" v-modefont-familyl="msg" @keydown="get">
>>>>>>> e6b7cd2cbf5abb6db633bf7b017443d14265cdf0
        {{msg}}
    </div>
</template>

<script>
export default {
  data(){
    return {
      msg:''
    }
  },
  watch:{
    msg(){
      alert('watch')
    }
  },
  methods:{
    get(){
      alert('method')
    }
  }
}
</script>

<style lang="scss" module>
  @import '../../css/reset.scss';
  .home{
    color: red;
    font-size: 80px;
  }
</style>
