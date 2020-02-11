<template>
    <div class="row">
        <form action="">
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <label for="slogan">Slogan</label>
                <textarea class="form-control" rows="3" v-model="slogan"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <button class="btn btn-primay" @click.prevent="addSlogan">Add Slogan</button>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
                slogan: ''
            };
        },
        methods: {
            addSlogan() {
                this.$emit('sloganAdded', this.slogan);
                this.slogan = '';
            }
        }
    }
</script>

<style>
    
</style>