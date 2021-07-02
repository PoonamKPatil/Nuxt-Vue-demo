<template>
    <div>
        <header class="header">
           <nav-bar/>
        </header>
    </div>
</template>

<script>
import NavBar from './NavBar.vue'
export default {
    name: 'AppHeader',
    components:{
        NavBar
    }
}
</script>
