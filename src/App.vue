<template>
    <div>
        <app-header></app-header>
            <div class="container">
                <comp-cars :cars="cars"></comp-cars>
            </div>
        <app-footer></app-footer>
    </div>
</template>

<script>
    import compCars from './components/Cars/Cars-Main.vue';
    export default {
        components:{
            compCars
        },
        data(){
            return {
                cars:[
                    {model:'F9',brand:'Ferrari'},
                    {model:'911',brand:'Porsche'},
                    {model:'Tipo',brand:'Fiat'}
                ]
            }
        },
        methods:{
         
        }
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