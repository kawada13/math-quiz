<template>
  <div>
    <button @click="$emit('changeOperator', '+')">Addition <br> +</button>
    <button @click="$emit('changeOperator', '-')">Substraction <br> -</button>
    <button @click="$emit('changeOperator', '/')">Division <br> /</button>
    <button @click="$emit('changeOperator', '*')">Multiplication <br> *</button>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
button {
  padding: 10px;
  height: 80px;
  margin-right: 10px;
  background-color: #10aeb2;
  color: white;
  font-size: 24px;
  cursor: pointer;
  vertical-align: top;
}
</style>