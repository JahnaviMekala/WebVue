<template>
  <div class="container">
    
    <HeaderTop ConcertName="Musical Concert" performerName="live music" />
  
      <ConcertBox :concert="concert" />
  </div>

 
     

</template>
<script>




import HeaderTop from './components/HeaderTop.vue'
import ConcertBox from './components/ConcertBox.vue'



export default {
  name: 'App',
  components: {
    
    HeaderTop,
    ConcertBox
  },

  data(){
    return {
      concert: []
    }
  },
  methods: {
    // promises

      
        async fetchConcert(){
        const res= await fetch('https://webprojectf.herokuapp.com/api')
        const data= await res.json()
        console.log(data)
        return data
      }

  },

  async created(){
    this.concert = await this.fetchConcert()
    
  }
}
</script>


<style scoped>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}


div{
  margin-bottom: 0.5em;
}



</style >



