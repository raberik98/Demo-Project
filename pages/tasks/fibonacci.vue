<template>
  <div>
    <div class="d-flex m-5">
        <div class="mb-3">
            <label class="form-label">Give a number</label>
            <input type="text" class="form-control" v-model="input">
        </div>
    </div>

    <button class="btn-primary m-5" @click="fibonacciSetVariables()">Start analisis</button>

    <h3 v-if="result == true" >Yes this number is part of the Fibonacci sequence!</h3>
    <h3 v-if="result == false" >No this number isn't part of the Fibonacci sequence!</h3>
    

  </div>
</template>

<script>
export default {
    data(){
        return{
            input:"",
            result: null
        }
    },
    methods:{
        isPerfectSquare(input){
            let inputSqrt = parseInt(Math.sqrt(input))
            if (inputSqrt*inputSqrt == input) {
                return true
            }
            else{
                return false
            }
        },
        isFibonacci(input){
            if (this.isPerfectSquare(5*input*input+4) == true
             || this.isPerfectSquare(5*input*input-4) == true) {
                return true
            }
            else{
                return false
            }
        },
        fibonacciSetVariables(){
            this.result = this.isFibonacci(this.input)
        }
    }
}
</script>

<style>

</style>