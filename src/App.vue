<template>

   <!-- Step , you must use the component -->
   <MyHeader flightName="Flight Information details" authorName="Nikhil Sai Kamma" />
   
   <FlightBox :flights=flights />

  

  

</template>

 

<script>

 

// step 1 import the child component

import MyHeader from './components/MyHeader.vue'

import FlightBox from './components/FlightBox.vue'

 

// 

 

export default{

  name: 'App',

  // step 2: register the component 

  components:{

    MyHeader,

    FlightBox

  },

  data(){

    return {

      flights: []

    }

  },

  methods:{

    //promises

    async fetchflights(){

      const res = await fetch("https://nikhilsai-kamma-flightdetails.onrender.com/api");

      const data = await res.json()

      console.log(data)

      return data

    }

  },

  async created(){

    this.flights = await this.fetchflights();

  }

  

 

}

 

 

</script>

 

<style>

 

</style>