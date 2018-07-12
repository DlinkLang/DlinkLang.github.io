<template>
  <div class="content ml-auto mr-auto" :key="$route.params.page">
    <h1 class="text-center"> {{$route.params.page}} </h1>
    <div v-html="content"></div>
  </div>
</template>

<script>
export default {
  async asyncData ({params}) {
    params.page = params.page || 'index';
    const fileContent = await import(`~/_posts/standards/${params.page}.md`)
    return {
      content: fileContent
    }
  }
}
</script>

<style>
</style>