<template>
    <button>Inbox View</button>
    <button>Archived View</button>

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