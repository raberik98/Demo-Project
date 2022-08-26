<template>
  <div class="navbar-background">
    <ul class="navbar-links">
        <li class="navbar-item" v-for="item in Links" :key="item">
            <nuxt-link class="navbar-item" :to='item.to'>{{item.text}}</nuxt-link>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    name:"Navbar",
    data(){
        return {
            Links: [
                {text:"Home",to:"/"},
                {text:"About",to:"/about"},
                {text:"Tasks",to:"/tasks"}
            ]
        }
    }
}
</script>

<style>
    .navbar-background {
        display: flex;
        background-color: gray;
        padding: 0.5rem;
        align-items: center;
        justify-content: space-between;
    }
    .navbar-links{
        display: flex;
        list-style: none;
    }
    .navbar-item{
        font-size: 1.5rem;
        padding: 0.4rem;
        color: white;
    }
    .navbar-item :hover, .navbar-links:hover{
        text-decoration: none;
        color: rgb(255, 145, 0);
    }
</style>