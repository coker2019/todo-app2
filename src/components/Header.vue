<template>
    <div>
        <h3 class="header">My VueJs ToDo App</h3>
        <p>{{name}}</p>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                name: 'WELCOME'
            }
        }
    }
</script>


<style>
 .header {
     color: black;
 }
</style>
