<template>
    <div>
        <p v-if="$fetchState.pending">
            <b-spinner variant="primary"></b-spinner>
        </p>
        <p v-else-if="$fetchState.error">Error while fetching users </p>
        <div v-else>
            <b-card title=" Details of User" tag="article" style="max-width: 20rem;" class="mb-2">
                <b-card-text> Name: {{user.name}}</b-card-text>
                <b-card-text> Email: {{user.email}}</b-card-text>
                <b-card-text> Website: {{user.website}}</b-card-text>
                <b-card-text> City: {{user.address.city}}</b-card-text>
            </b-card>
            <!-- <b-button v-b-toggle.collapse-a.collapse-b>Toggle Collapse A and B</b-button> -->

        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            user: null
        }
    },
    async fetch() {
        this.user = await this.$http.$get(`https://jsonplaceholder.typicode.com/users/${this.$route.params.id}`)
    },
}
</script>
