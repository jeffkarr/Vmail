<template>

    <button>Inbox View</button>
    <button>Archived View</button>
    <div class="row">
        <span><img alt="Vue logo" class="logo" src="./assets/logo.svg" width="40" height="40" /></span><h1>VMail Inbox</h1>
    </div>
    <h1>VMail</h1>

</template>

<script>
    import axios from 'axios';

    export default {
        async setup() {
            let res = await axios.get('http://localhost:3000/emails');
            let emails = res.data;

            return {
                emails
            }
        },
        components: {

        },
        methods: {

        },
        computed: {

        }
    }


</script>

<style scoped>

</style>