<template>
    <div>
        <p v-if="$fetchState.pending">
            <b-spinner variant="primary"></b-spinner>
        </p>
        <p v-else-if="$fetchState.error">Error while fetching users</p>
        <div v-else>
            <h1>List of Users</h1>
            <nuxt-link v-for="user in users" :key="user.id" :to="'users/' +user.id" class="single">
                {{user.name}}
            </nuxt-link>
        </div>
    </div>
</template>

<script>
export default ({
    data() {
        return {
            users: []
        }
    },

    async fetch() {
        this.users = await this.$http.$get('https://jsonplaceholder.typicode.com/users')
    },

    head() {
        return {
            title: "Users app",
            meta: [{
                hid: 'description',
                name: 'description',
                content: 'user pages'
            }]
        }
    },
})
</script>

<style>

.single {
    padding: 2px 16px;
    background: #fff;
    margin: 20px 10px;
    display: block;
}

.single:hover {
    border-left: 8px solid purple
}

</style>