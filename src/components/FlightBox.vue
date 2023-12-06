<template>

    <div>

        

        <div v-for="flight of flights" :key="flight.flight_number" >

            <SingleFlight :flight=flight />

        </div>

 

    </div>

    

    

    

    

    

</template>

 

 

<script>

import SingleFlight from './SingleFlight.vue'

export default{

 

    name:'FlightBox',

    props:{

        flights: Array

    },

    components:{

        SingleFlight

    }

 

}

 

</script>

<style scoped>

div{

    text-align: center;

}

</style>