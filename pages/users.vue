<template>
  <div>
    <input type="text" v-model="userId" />
    <button class="button--green" v-on:click="onLoadUser">nono</button>
    <nuxt-child />
  </div>
</template>
<script>
export default {
  // ? 왜 이렇게 함수로 작성되는지
  data() {
    return {
      userId: ''
    }
  },
  methods: {
    onLoadUser() {
      this.$router.push(`/users/${this.userId}`)
    }
  },
  layout: 'users'
}
</script>