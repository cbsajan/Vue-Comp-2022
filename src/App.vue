<template>
    <div>
        <app-header></app-header>
            <div class="container">
                <button @click="this.activeComp = 'mike-comp'">Mike</button>
                <button @click="this.activeComp = 'steve-comp'">Steve</button>
                    <!-- <mike-comp v-if="activeComp == 'mike-comp'"></mike-comp>
                    <steve-comp v-if="activeComp == 'steve-comp'"></steve-comp> -->
                <component :is="activeComp"></component>
            </div>
        <app-footer></app-footer>
    </div>
</template>

<script>
    import MikeComp from './components/Players/Mike-Comp.vue'
    import SteveComp from './components/Players/Steve-Comp.vue'
    export default {
        components:{
            MikeComp,
            SteveComp
        },
        data(){
            return {
               activeComp:'mike-comp'
            }
        },
        
    }
</script>

<style>
    body {
        padding: 0;
        margin:0;
        font-family: 'Roboto', sans-serif;;
    }
    .container{
        min-height: 84vh;
        box-sizing: border-box;
        padding: 20px;
    }
</style>