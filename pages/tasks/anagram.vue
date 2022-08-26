<template>
  <div>
    <div class="d-flex m-5">
        <div class="mb-3">
            <label class="form-label">Input 1</label>
            <input type="text" class="form-control" v-model="input1">
        </div>
        <div class="mb-3">
            <label class="form-label">Input 2</label>
            <input type="text" class="form-control" v-model="input2">
        </div>
    </div>

    <button class="btn-primary m-5" @click="anagramSetVariables()">Start analisis</button>

    <h3 v-if="result == true" >Yes these are each others anagrams!</h3>
    <h3 v-if="result == false" >No they aren't each others anagrams!</h3>
    

  </div>
</template>

<script>
export default {
    data(){
        return{
            input1:"",
            input2:"",
            result: null
        }
    },
    methods:{
        anagramCheck(i1,i2){
            if(i1.length != i2.length){
                console.log(false)
                return false
            }

            const hashList = {}

            for (let i = 0; i < i1.length; i++) {
                if (!hashList[i1[i]]) {
                    hashList[i1[i]] = 0
                }
                hashList[i1[i]]++
            }

            for (let j = 0; j < i2.length; j++) {
                if (!hashList[i2[j]]) {
                    console.log(false)
                    return false
                }
                hashList[i2[j]]--
            }
            console.log(true)
            return true
        },
        anagramSetVariables(){
            this.result = this.anagramCheck(this.input1,this.input2)
        }
    }
}
</script>

<style>

</style>