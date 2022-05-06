<template>
<div>
    <h1>Welcome to the cars</h1>
    <div>
        <list-cars :cars="cars"></list-cars>
    </div>
</div>
</template>

<script>
import listCars from './List-Cars';
export default {
    props:['cars'],
    components:{
        listCars
    },
    data(){
        return{

        }
    }
}
</script>