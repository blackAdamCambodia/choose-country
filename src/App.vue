<script setup>
import countries from "./data/country-by-capital-city.json"
const myStyle = {
  listStyle: "none",
  border: "1px solid",
  padding: "10px",
  backgroundColor: "#fcba03",
  color: "black",
  fontWeight: "bold",
  fontSize: "20px",
  textAlign: "left",
}
function myFilterCountry() {
  return countries.filter(x => {
    return  x.country.startsWith("B")
  })
}
const colorName = "color:Green"
  
 
</script>

<template>
      <div>
        <h1>Countries Starts With Letter "B"</h1>
        <p>This is a list of all the countries Name Start With "B".</p>
        <ul>
          <li :style="myStyle" v-for="(country , index) in myFilterCountry()" :key="index"><span :style="colorName">{{index+1}}</span> .{{ country.country }}</li>
        </ul>
      </div>
      
    
</template>

<style scoped>

</style>
