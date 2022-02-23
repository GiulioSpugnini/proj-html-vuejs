<template>
  <div class="col-12">
            <h1 class="purple">{{title}}</h1>
            <p class="text-secondary">{{text}}</p>
            <img class="py-4" src="../../assets/img/header_divider.png" alt="" />
          </div>
</template>

<script>
export default {
name: 'TitleWithDivisor',
props:['title','text'],
}
</script>

<style>

</style>