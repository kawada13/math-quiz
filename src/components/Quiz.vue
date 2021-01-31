<template>
  <div>
    <div v-if="isQuizStart">
      <h4>{{left}} {{operator}} {{right}}</h4>
      <hr>
      <button v-for="(answer, i) in answers" :key="i">{{answer}}</button>
    </div>
    <hr>
    <div v-if="!isQuizStart">
      <button @click="start">start</button>
    </div>
    <button @click="$emit('clear')">Back</button>
  </div>
</template>

<script>
export default {
  props: ['operator'],
  data() {
    return {
      isQuizStart: false,
      left: null,
      right: null,
      answers: []
    }
  },
  methods: {
    start() {
      this.isQuizStart = true
      this.left = parseInt(Math.random() * 13)
      this.right = parseInt(Math.random() * 13)
      for(let i = 0; i < 5; i++) {
        const answer =
        this.left * parseInt(Math.random() * 3) +
        this.right * parseInt(Math.random() * 3) 

        this.answers.push(answer)
      }
    }
  },
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