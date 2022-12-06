<template>
<div>
    <h1> {{ConcertName}} </h1>
    <h4> {{performerName}} </h4>
</div>
</template>

<script>

export default{
    name: 'HeaderTop',
    props:{
        ConcertName: String,
        performerName:String
    }
}

</script>

<style scoped>

div{
    text-align: center;
    color:rgb(6,2,16);
    margin: 4px black;
    backgroundcolor:blue;
}
h1{
    margin: 3px;
    backgroundcolor:gray;
}

</style>