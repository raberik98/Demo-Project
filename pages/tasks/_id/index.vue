<template>
  <div>
    <h2>{{$route.params.id}}</h2>
  </div>
</template>

<script>
export default {
    head() {
        return {
            title: 'Do the task',
            meta: [
                {
                hid: 'Do the task',
                name: 'Do the task',
                content: 'Nuxt.js do one task'
                }
            ]
        }
    }
}
</script>

<style>

</style>