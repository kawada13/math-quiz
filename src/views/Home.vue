<template>
  <div class="home">
    <h1>Math Quiz</h1>
    <Quiz v-if="operator" :operator='operator' @clear="clear" />
    <Operator v-if="!operator" @changeOperator="changeOperator" />
  </div>
</template>




<script>

import Operator from '@/components/Operator.vue';
import Quiz from '@/components/Quiz.vue';

export default {
  data() {
    return {
      operator: null
    }
  },
  methods: {
    changeOperator(ope) {
      this.operator = ope
    },
    clear() {
      this.operator = null
    }
  },
  
  components: {Operator, Quiz}
}
</script>



<style scoped>
.home {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size: 24px;
}


</style>
