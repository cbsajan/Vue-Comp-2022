<template>

    <div v-awesome.red.big="textToRender"></div>
    <div v-awesome.blue.small="textToRender"></div>

    <button @click="this.textToRender = 'Something else'">
        Trigger update
    </button>

</template>



<script>
export default {
    data() {
        return {
            textToRender: 'Text from data'
        }
    }
}    
</script> 