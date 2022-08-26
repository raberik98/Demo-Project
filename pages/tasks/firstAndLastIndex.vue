<template>
  <div>
    <div class="d-flex m-5">
        <div class="mb-3">
            <label class="form-label">Numbers</label>
            <input type="text" class="form-control" v-model="numbers">
        </div>
        <div class="mb-3">
            <label class="form-label">Target</label>
            <input type="text" class="form-control" v-model="target">
        </div>
    </div>

    <button class="btn-primary m-5" @click="checkNumberSequence()">Start analisis</button>

    <h3 v-if="this.firstIndex == 0">The target number isn't part of the sequence!</h3>
    <h3 v-else>The target numbers first index is: <span style="color:red">{{this.firstIndex}}</span>
     and the last index is: <span style="color:red">{{this.lastIndex}}</span>
    </h3>

    

  </div>
</template>

<script>
export default {
    data(){
        return{
            numbers:null,
            target:null,
            firstIndex:0,
            lastIndex:0
        }
    },
    methods:{
        checkNumberSequence(){
            for (let index = 0; index < this.numbers.length; index++) {
                if (index == this.target) {
                    if (this.firstIndex == 0) {
                        this.firstIndex == index
                        this.lastIndex == index
                    }
                    else{
                        this.lastIndex == index
                    }
                }
            }
        }
    }
}
</script>

<style>

</style>