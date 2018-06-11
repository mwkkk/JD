<template lang="html">
    <div :class="$style.home">
        <h1>Home</h1>
        <input type="text" name="" value="" v-modefont-familyl="msg" @keydown="get">
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
