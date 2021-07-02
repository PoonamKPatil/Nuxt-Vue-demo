<template>
    <div>
       <h1>About</h1>
    </div>
</template>

<script>

export default ({
    data() {
        return {
            users: []
        }
    },
    created() {
        
    },
    head() {
        return {
            title: "About app",
            meta: [{
                hid: 'description',
                name: 'description',
                content: 'about pages'
            }]
        }
    }
    
})
</script>
