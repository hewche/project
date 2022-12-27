<template>
  <div class="hello">
    <p>Введите число 1  <input @input = "getFourthNumber" v-model="firstNumber"/></p>
    <p>Введите число 2  <input @input = "getFourthNumber" v-model="secondNumber"/></p>
    <p>{{ fourthNumber }}</p>
    <p> Введите число 3  <input  @input = "getFitfthNumber" v-model="thirdNumber"/></p>
    <p>{{ fifthNumber }}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return{
      firstNumber:null,
      secondNumber:null,
      thirdNumber:null,
      fourthNumber:null,
      fifthNumber:null
    }
  },
  methods:{
    getFourthNumber(){
      this.fourthNumber = (this.firstNumber / this.secondNumber).toFixed(2)
    },
    getFitfthNumber(){
      this.fifthNumber = (this.fourthNumber * this.thirdNumber).toFixed(2)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
