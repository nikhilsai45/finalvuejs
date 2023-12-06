<template>

    <div :class="flight.booking_status ? 'green' :'red' ">

        <h2>{{flight.flight_name}}</h2>
        <h2>{{flight.date}}</h2>
        <h2>{{flight.price}}</h2>
        <h2> {{flight.passenger_details.name}}</h2>
        <h2>{{flight.booking_status}}</h2>

    </div>

</template>

<script>

 

export default {

    name: 'SingleFlight',

    props:{

        flight: Array

    }

    

}

</script>

 

<style scoped>

.green{

  background-color: green;

}

.red{

  background-color: red;

}

h2{

    font-size:2em;
    color: white;
    text-align: center;

}

h4{

  margin: 2px

}

div{

  background-color: #FFB89e;

  color: black;

  padding: 1em;

  text-align: center;

  margin: 1em;

}

 



</style>