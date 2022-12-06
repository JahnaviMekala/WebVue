<template>
    
    
         
        <div class="ConcertBox">
                
                <ConcertApp :concert="concert"/>
        </div>

        

    

</template>

<script>

import ConcertApp from "./ConcertApp.vue"
export default{

    name: 'ConcertBox',
    components: {
        ConcertApp
    },
    props: {
        concert: Array
    }

}

</script>


<style scoped>

.ConcertBox{

    
    padding: 1em;
    color: gray;
    font-size: 2vmin;
    margin: 5% 5% 5% 5%;
    display:grid;
    grid-template-columns:1fr 1fr 1fr;
    
    
}
</style>