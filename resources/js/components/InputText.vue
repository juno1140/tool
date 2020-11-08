<template>
    <div class="blade_text">
            &lt;div class="form-group"&gt;
                &lt;div class="col-md-6"&gt;
                    &lt;label for="name"&gt;name&lt;/label&gt;
                    &lt;input type="text" class="form-control" name="{{ msg }}" id="name"/&gt;
                &lt;/div&gt;
            &lt;/div&gt;
    </div>
</template>

<script>
export default {
    data() {
        return {
            msg: 'fff',
        };
    },
    mounted() {
        console.log('Component mounted.')
    },
}
</script>

<style>
.blade_text {
    white-space: pre-wrap;
}
</style>