<template>
    <div>
        <h1>Welcome to the cars</h1>
        <div>
            <comp-list></comp-list>
        </div>
    </div>
</template>

<script>
import compList from './List-Cars.vue';
export default {
    props:['cars'],
    components:{
        compList
    },
    data(){
        return {
        }
    }
}
</script>