<template>
    <nuxt-link :to="'/tasks/'+url">
        <div class="ListItem">
            <div class="ListItemHeader">
                <h4>
                    {{taskName}}
                </h4>
            </div>
            <div class="ListItemBody">
                <p>
                    {{taskDescription}}
                </p>
            </div>
        </div>
    </nuxt-link>
</template>

<script>
export default {
    name: "TaskListItem",
    props: ['taskName', 'taskDescription', 'url']
}
</script>

<style>
.ListItemHeader{
    background-color: rgb(58, 58, 105);
    color: white;
    margin: 0;
    padding: 5px;
}
.ListItemBody{
   background-color: rgb(118, 118, 138);
    color: white;
    font-size: 15px;
    margin: 0;
    padding: 5px;
}
.ListItem{
    margin-bottom: 1rem;
}
</style>