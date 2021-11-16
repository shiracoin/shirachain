<template>
  <h1>Block Details</h1>
  <p>Block Height : {{ id }}</p>
</template>

<script>
export default {
    props: ['id'],
    data() {
        return {
            id: this.$route.params.id
        }
    }
}
</script>

<style>
</style>