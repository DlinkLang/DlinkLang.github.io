<template>
  <div>
    <h1 class="text-center">{{error.message}}</h1>
    <a href="/"><button class="ml-auto mr-auto d-block">Go to the homepage</button></a>
  </div>
</template>

<script>
export default {
  props: ['error']
};
</script>
