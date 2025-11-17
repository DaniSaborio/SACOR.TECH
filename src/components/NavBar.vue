<script setup>
import Game_Projects from './Game_Projects.vue';
import General_Buttons from './General_Buttons.vue';

defineProps({
    msg:{
        type: String,
        required: true,
    },
})
</script>

<template>
<div>
    <h1 class="jacquard-12-regular">
        {{ msg }}
    </h1>
</div>
<General_Buttons class="services_btn" name_btn="Services"/>
<Game_Projects class="projects_btn"/>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Jacquard+12&display=swap');

.jacquard-12-regular {
  font-family: "Jacquard 12", system-ui;
  font-weight: 400;
  font-style: normal;
}
header {
  position: absolute;
  top: 50px;
  left: 20px;
  width: 98%;
  height: 60px;
  background: #983790;
  border-radius: 10px;
  text-align: left;
}

.services_btn {
  position: absolute;
  margin-top: -30px;
  right: 98px;
}

.projects_btn{
  position: absolute;
  margin-top: -75px;
  right: 10px;
}
</style>