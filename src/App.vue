<template>
    <FiltroBusca/>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';
    import FiltroBusca from './components/FiltroBusca.vue'

    export default defineComponent({
        name: 'App',
        components: {
            FiltroBusca
        },
        data() {
            return {
                camadasOption: [
                    { name: 'Pizza', value: '1' },
                    { name: 'Apple', value: '2' },
                    { name: 'Cake', value: '3' },
                    { name: 'Fish', value: '4' },
                    { name: 'Rice', value: '5' }
                ],
                atributosOption: [
                    { name: 'Cheese', value: '1' },
                    { name: 'Banana', value: '2' },
                    { name: 'Shrimp', value: '3' },
                    { name: 'Crab', value: '4' },
                    { name: 'Grape', value: '5' }
                ]
            }
        },
        provide() {
            return {
                camadasOption: this.camadasOption,
                atributosOption: this.atributosOption
            }
        }
    })
</script>

<style>
</style>
