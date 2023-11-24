<template>
    <div class="modal">
        <div class="overlay" @click="emit('closeModal')"></div>
        <div class="modal-card">
            <slot />
        </div>
    </div>
</template>

<script>
    import useKeydown from '../composables/use-keydown';

    export default {
        setup(props, {emit} ) {
            
            useKeydown([
                { key: 'Escape', fn: () => { emit('closeModal') }},
                { key: 'e', fn: () => { emit('toggleArchive') }},
                { key: 'r', fn: () => { emit('toggleRead') }},
                { key: 'k', fn: () => { emit('goNewer') }},
                { key: 'j', fn: () => { emit('goOlder') }},
                { key: '[', fn: () => { emit('goNewerAndArchive') }},
                { key: ']', fn: () => { emit('goOlderAndArchive') }}
            ]) 

            return {
                emit
            }
        }
    }
</script>

<style scoped>
</style>