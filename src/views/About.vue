<template>
  <div class="about">
    <h1>This is an about page</h1>
    <hr>
    <input v-model="msg">
    <input v-model="hh">
    <input v-model="tt">
     <p>{{vvv}}</p>
    <p>{{hh}}</p>
    <p>{{tt}}</p>
    <p>{{$route.name}}</p>
  </div>
</template>

<script>

import moment from 'moment'


export default {

  
  data() {
    return {
      vvv: 'good',
      hh: 'hi',
      tt: 'hello'
    }
  },
  computed: {
    msg: {
      get() {
        return this.vvv
      },
      set(v) {
        console.log(v)
        this.hh = '変わったぜ'
        this.tt = 'それば'
        this.vvv = v
      }
    }
  },
  created() {
    console.log(moment('2017/04/07 23:10').fromNow())
  },
}
</script>