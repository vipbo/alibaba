<template>
    <div class="son1">
        <p>Son1</p>
        <p>Son1-{{message}}</p> 
        <p @click="change" class="change-more">点击变多</p>
    </div>
</template>
<script>
export default {
    props:{
        message:{
            type:Number,
            default:10
        }
    },
    methods:{
        change(){
            this.$emit('changeMore',200)
        }
    }
}
</script>
<style scoped>
.change-more{
    cursor: pointer;
}
</style>


