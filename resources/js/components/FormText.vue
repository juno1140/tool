<template>
    <div class="blade_text">
        &lt;form method="POST" action=""&gt;
            @csrf
            <InputText />
        &lt;/form&gt;
    </div>
</template>

<script>
import InputText from './InputText';

export default {
    components: { InputText },
}
</script>

<style>
.blade_text {
    white-space: pre-wrap;
}
</style>