<template>
  <div>
    <h1>Description</h1>
    <p>This is a demo project where I build a simple website using
        many feautres of Nuxt.js
    </p>
  </div>
</template>

<script>
export default {
    head() {
        return {
            title: 'About page',
            meta: [
                {
                hid: 'description',
                name: 'description',
                content: 'Nuxt.js demo project'
                }
            ]
        }
    }
}
</script>

<style>

</style>