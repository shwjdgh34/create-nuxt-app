<template>
  <h1>{{ $route.params.id}}</h1>
</template>

<script>
export default {
  validate({ params }) {
    // must be a number
    return /^\d+$/.test(params.id)
  }
}
</script>