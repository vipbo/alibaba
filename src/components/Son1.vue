<template>
    <div class="son1">
        <p>Son1</p>
        <p>message-{{message}}</p> 
        <p>value-{{value}}</p> 
        <p @click="change" class="change-more">点击变多</p>
    </div>
</template>
<script>
export default {
    props:{
        value:{
            type:Number,
            default:8
        },
        message:{
            type:Number,
            default:10
        }
    },
    methods:{
        change(){
            // this.$emit('changeMore',200) // 写法1 写法2
            // this.$emit('update:message',300) // 写法3 写法4
            this.$emit('input',300) // 写法3 写法4
        }
    }
}
</script>
<style scoped>
.change-more{
    cursor: pointer;
}
</style>


