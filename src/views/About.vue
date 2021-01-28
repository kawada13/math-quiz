<template>
  <div class="about">
    <h1>This is an about page</h1>
    <hr>
    <input v-model="msg">
    <p>・変数valueの中身： {{msg}}</p>
  </div>
</template>

<script>


export default {
  data() {
    return {
      msg: 'Default message'
    }
  },
}
</script>