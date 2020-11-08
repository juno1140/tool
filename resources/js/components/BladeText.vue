<template>
    <div class="blade_text">
        @extends('layouts.app')

        @section('content')
            &lt;div class="container"&gt;

            &lt;/div&gt;
        @endsection
    </div>
</template>

<script>
import InputText from './InputText.vue';

export default {
    components: { InputText },
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
    /*line-height: 0.6;*/
}
</style>