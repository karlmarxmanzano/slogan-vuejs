<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="card card-default">
            <div class="card-body qoute">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>

</script>

<style>
    .card-body {
        font-family: 'Arizonia', cursive;
        font-size: 24px;
        color: #6e6e6e;
    }

    .qoute {
        cursor: pointer;
    }

    .qoute:hover {
        background-color: #ffe2e2;
    }
</style>