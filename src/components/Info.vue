<template>
    <div id="info">
       <button @click="onStepChanged('QUIZ')">TAKE THE QUIZ</button> 
    </div> 
</template>

<script>
export default {
    data(){
        return {
            
        }
    },
    methods:{
        onStepChanged(step) {
            this.$emit('step-changed', step);
        },
    }
    
}
</script>

<style>

</style>