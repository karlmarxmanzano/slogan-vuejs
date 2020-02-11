<template>
    <div class="row">
        <app-slogan 
            v-for="(slogan, index) in slogans"
            @click.native="deleteSlogan(index)">{{ slogan }}</app-slogan>
    </div>
</template>

<script>
    import Slogan from './Slogan.vue';

    export default {
        props: ['slogans'],
        methods: {
            deleteSlogan(index) {
                this.$emit('sloganDeleted', index);
            }
        },
        components: {
            'app-slogan': Slogan
        }
    }
</script>

<style>
    
</style>