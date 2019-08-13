<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <!-- <Son1 :message="message" @changeMore="change"/> 写法1-->
    <!-- <Son1 :message="message" @changeMore="value=>this.message=value"/> 写法2-->
    <!-- <Son1 :message="message" @update:message="value=>this.message=value"/> 写法3-->
    <!-- <Son1 :message.sync="message"/> 写法4 是写法3的简化形式 -->
    <!-- <Son1 :message="message" @input="value=>this.message = value"/> -->
    <Son1 v-model="message"/>
    <!-- v-model 是 value 和 input事件的简写形式，且只能是value和input，而sync就自由灵活的多 -->
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
    // change(value){ 写法1
    //   this.message = value;
    // }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
