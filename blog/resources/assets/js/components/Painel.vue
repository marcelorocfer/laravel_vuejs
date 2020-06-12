<template>
    <div v-bind:class="defineCor">
        <div class="panel-heading">{{titulo}}</div>

        <div class="panel-body">
            <slot></slot>
        </div>
    </div>
</template>

<script>
    export default {
        props:['titulo', 'cor'],
        computed:{
            defineCor: function(){
                return "panel "+ (this.cor || "panel-default");
            }
        }
    }
</script>

<style media="screen">
    .blue
    {
        border-color: #0d4a96;
    }
    .blue > .panel-heading 
    {
        color: #f7f7f7;
        background-color: #0d4a96;
        border-color: #0d4a96;
    }

    .orange
    {
        border-color: #fd9800;
    }
    .orange > .panel-heading 
    {
        color: #f7f7f7;
        background-color: #fd9800;
        border-color: #fd9800;
    }

    .red
    {
        border-color: #e80d0d;
    }
    .red > .panel-heading 
    {
        color: #f7f7f7;
        background-color: #e80d0d;
        border-color: #e80d0d;
    }
</style>
