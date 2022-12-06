<template>
    <div v-for="concert in concert" :key="concert.id">
        <ul><h4>Event Id: {{ concert.id }}</h4></ul>
        <ul><h4>Event Name: {{ concert.concert_name }}</h4></ul>
        <ul><h4> Event Date: {{ concert.concert_date }} </h4></ul>
        <ul><h4>Event Time:  {{ concert.concert_time }}</h4></ul>
        <ul><h4>Cost: {{ concert.concert_price }}</h4></ul>
         <ul><h4>Availability: {{ concert.tickets_available }}</h4></ul>
        
        
        
        
    </div>
</template>


<script>

export default{
    name: 'ConcertApp',
    props:{
        concert: Array,
    },
   
};
</script>

<style scoped>



h4{
    margin: 2px;
}

div{
    width: 90%;
    height: 90%;
    color: white;
    padding: 1em;
    border-radius: 5px;
    border: 0.3em solid  white;
    margin-bottom: 25px auto;
    overflow: auto;
    background: black;
  }
div:hover {
 border: 0.3em solid yellow;
 color: yellow;
}

.red{
background-color: orangered !important;

}
.green{
background-color: rgb(115, 159, 61) ;
}


</style>