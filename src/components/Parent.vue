<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <Son1 :message="message" @changeMore="change"/>
  </div>
</template>

<script>
import Son1 from './Son1'
export default {
  name: 'parent',
  components:{
    Son1
  },
  props: {
    msg: String
  },

  data(){
    return {
      message:100
    }
  },
  methods:{
    change(value){
      this.message = value;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
