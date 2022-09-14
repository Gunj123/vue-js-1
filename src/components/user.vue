<template>
    <div class="user">
        <h2>{{data.name}}</h2>
        <h2>{{data.email}}</h2>
        <button v-on:click="getdata(data.name)">show name</button>
    </div>

</template>
<script>
export default {
    name:'user-',
    props:{
        data:Object,
        getdata:Function
    },
}
</script>
<style>
  .user {
    background-color: skyblue;
    padding: 10px;
    border: 1px solid black;
    margin-bottom: 20px;
} 
</style>
