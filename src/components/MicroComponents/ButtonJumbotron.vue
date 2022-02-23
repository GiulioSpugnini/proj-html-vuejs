<template>
  <button class="px-3 m-5 bg-transparent text-white"><h6 class="m-0">{{textButton}}</h6></button>
</template>

<script>
export default {
name: 'ButtonJumbotron',
props:['textButton'],
}
</script>

<style scoped>
button{
  border: 2px solid white;
}
button:hover{
 background-color: white !important;
 color: #4c4a9b !important;
}
</style>