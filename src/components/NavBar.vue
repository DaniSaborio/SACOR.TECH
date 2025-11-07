<script setup>
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
  width: 90%;
  background: #983790;
  border-radius: 10px;
}
</style>