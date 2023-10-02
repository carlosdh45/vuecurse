import counter from '@/components/counter.vue';
<template>
  <h2>{{title || customTitle }} </h2>
  <p>{{ counter }} <sub>2</sub> = {{ squareCounter }}</p>

  <div>
    <button v-on:click="increase(this.counter)">+1</button>

    <button v-on:click="decrease(this.counter)">-1</button>
  </div>
</template>

<script>
export default {

  props: ['title', 'start'],
  data() {
    return {
      counter: 5,
    };
  },
  methods: {
    getSquare() {
      return this.counter * this.counter;
    },

    increase() {
      this.counter++

    },

    decrease() {
      this.counter--
    }
  },
  computed: {
    squareCounter() {
      return this.counter * this.counter;
    },

    customTitle() {
      if(this.title !== undefined) {
        return this.title
      }else{
        return this.title || 'counter'
      }
      
    }
    
  },
};
</script>

<style>
button{
  background: green;
  border-radius: 5px;
  color: white;
  margin: 0 5px;
  transition: 0.3s ease-in-out;
  padding: 1%;
}
  button:hover {
    background-color: red;
    transition: 0.3s ease-in-out
  }

</style>
