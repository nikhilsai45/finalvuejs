<template>
    
    <div>
        <h1>{{flightName}}</h1>
        <h2>{{authorName}}</h2>
    </div>
</template>

<script>
export default {
  name:'MyHeader',
  props:{
    flightName:String,
    authorName:String
  }
}
</script>

<style scoped>
div{
    text-align: center;
}
</style>