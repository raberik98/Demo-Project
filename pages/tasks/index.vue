<template>
  <div>
    <h1>
        Here we will solve some tasks!
    </h1>
    <ul>
      <li v-for="item in Tasks" :key="item">
          <TaskListItem :taskName="item.name" :taskDescription="item.text" :url="item.url"/>
      </li>
    </ul>
  </div>
</template>

<script>
import TaskListItem from '../../components/TaskListItem.vue'
export default {
  components: { TaskListItem },
  data(){
    return{
        Tasks:[
          {name:"anagrams", text:"We will check if the two inputs are anagrams", url:"anagram", id: 1},
          {name:"fibonacci", text:"We will check if the two inputs are fibonacci numbers", url:"fibonacci", id: 2},
          {name:"first and last index", text:"We will check if the target numbers first and last apperance in a sequence", url:"firstAndLastIndex", id: 3}
        ]
    }
  }
}
</script>

<style>

</style>