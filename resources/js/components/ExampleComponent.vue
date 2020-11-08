<template>
    <div class="container-fluid">
        <div class="row justify-content-center">
            <div class="col-md-4 p-2">
                <div class="card">
                    <div class="card-body">
                        <div class="form-group">
                            <div class="col-md-8 my-3">
                                <label for="type" class="m-0">input type</label>
                                <select class="form-control" id="type" v-model="selectedType" @change="changeType">
                                    <option v-for="input in inputs" :value="input.id">
                                        {{ input.type }}
                                    </option>
                                </select>
                            </div>
                            <div class="col-md-8 my-3">
                                <label for="name" class="m-0">input name</label>
                                <input type="text" class="form-control" id="name" v-model="msg"/>
                            </div>
                            <div class="col-md-8 my-3">
                                <label for="label" class="m-0">label表示</label>
                                <input class="form-control" id="label" v-model="label"/>
                            </div>

                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-8 p-2">
                <div class="card">
                    <div class="card-body">
                        <div v-if="this.selectedType === 1" class="blade_text">
&lt;form method="POST" action=""&gt;
    @csrf

    &lt;div class="form-group"&gt;
        &lt;div class="col-md-6"&gt;
            &lt;label for="{{ msg }}" class="m-0"&gt;{{ label }}&lt;/label&gt;
            &lt;input type="text" class="form-control" name="{{ msg }}" id="{{ msg }}"/&gt;
        &lt;/div&gt;
    &lt;/div&gt;

&lt;/form&gt;
                        </div>
                        <div v-else-if="this.selectedType === 2" class="blade_text">
&lt;form method="POST" action=""&gt;
    @csrf

    &lt;div class="form-group"&gt;
        &lt;div class="col-md-6"&gt;
            &lt;label for="{{ msg }}" class="m-0"&gt;{{ label }}&lt;/label&gt;
            &lt;textarea class="form-control" name="{{ msg }}" id="{{ msg }}" cols="30" rows="10"&gt;
            &lt;/textarea&gt;
        &lt;/div&gt;
    &lt;/div&gt;

&lt;/form&gt;
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                msg: '',
                label: '',
                selectedType: 1,
                inputs: [
                    {id: 1, type: 'text'},
                    {id: 2, type: 'textarea'},
                    {id: 3, type: 'radio'},
                    {id: 4, type: 'select'},
                ]
            }
        },
        methods: {
            changeType: function () {
                this.type = this.selectedType
            }
        }
    }
</script>

<style>
.blade_text {
    white-space: pre-wrap;
}
</style>