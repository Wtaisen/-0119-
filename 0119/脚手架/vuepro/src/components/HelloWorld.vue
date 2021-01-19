<template>
  <div class="hello">
    <input type="text" v-model="msg" @keydown.enter="enter">
    <br>
    <span>{{toUpper}}</span>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'hello world'
    }
  },
  computed:{
    toUpper(){
      return this.msg.toUpperCase();
    }
  },
  methods: {
    enter(){
      alert(this.msg);
    }
  }
}
</script>

<style scoped>
span{
  color: red;
}
</style>
