<template>
  <div>
    <p>{{operator}}</p>
    <button @click="$emit('clear')">Back</button>
  </div>
</template>

<script>
export default {
  props: ['operator']
}
</script>