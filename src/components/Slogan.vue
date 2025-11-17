

<script setup>
import { ref } from 'vue'
const name_company = ref ("Sacor.Tech")
const slogan = ref ("Alma en cada byte")
const introduction = ref ("Buscamos ofrecerte desde desarrollo web, mantenimiento de equipos de computo hasta soluciones IOT para tu causa ")
</script>

<template> 
    <div class="block">
        <h1>{{name_company}}</h1>
        <h2>{{ slogan }}</h2>
        <p>{{ introduction }}</p>
    </div>
</template>

<style>
.block{
    text-align: center;
    position: absolute ;
    top: 100px;
  
}
</style>

