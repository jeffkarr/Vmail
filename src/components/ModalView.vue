<template>
    <div class="modal">
        <div class="overlay" @click="closeModalEmitter"></div>
        <div class="modal-card">
            <slot />
        </div>
    </div>
</template>

<script>
    export default {
        methods: {
            closeModalEmitter() {
                this.$emit('closeModal');
            }
        }
        // props: {
        //     email: {
        //         type: Object,
        //         required: true
        //     }
        // }
    }
</script>

<style scoped>
</style>