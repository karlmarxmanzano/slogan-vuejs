<template>
    <div class="container">
        <app-header :sloganCount="this.slogans.length" :maxSlogan="maxSlogan"></app-header>
        <app-new-slogan @sloganAdded="newSlogan"></app-new-slogan>
        <app-slogan-grid 
            :slogans="slogans"
            @sloganDeleted="deleteSlogan"></app-slogan-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">Info: Click on a Slogan to detele.</div>
            </div>
        </div>
    </div>
</template>

<script>
    import Header from './components/Header.vue';
    import SloganGrid from './components/SloganGrid.vue';
    import NewSlogan from './components/NewSlogan.vue';

    export default {
        data: function() {
            return {
                slogans: [
                    'Default Slogan.'
                ],
                maxSlogan: 10
            };
        },
        methods: {
            newSlogan(slogan) {
                if(this.slogans.length >= 10) {
                    return alert('Slogan is full. Please delete first by clicking on a slogan.');
                }
                this.slogans.push(slogan);
            },
            deleteSlogan(index) {
                this.slogans.splice(index, 1);
            }
        },
        components: {
            'app-header': Header,
            'app-slogan-grid': SloganGrid,
            'app-new-slogan': NewSlogan
        }
    }
</script>