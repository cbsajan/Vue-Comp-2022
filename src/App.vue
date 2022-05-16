<template>
    <div>
        <app-header></app-header>
            <div class="container">
                <comp-cars></comp-cars>
               <car-brands>
                    <div>Content at the top</div>
                    <template v-slot:brands>
                        <ul>
                            <li v-for="(brand,index) in brands" :key="index">
                                {{ brand }}
                            </li>
                        </ul>
                    </template>
                    <template v-slot:other>
                        <div>Some other content</div>
                    </template>
                    <strong>Default slot</strong>
                </car-brands>
            </div>
        <app-footer></app-footer>
    </div>
</template>

<script>
    import compCars from './components/Cars/Cars-Main.vue';
    import CarBrands from './components/Cars/Brand-Cars.vue';
    export default {
        components:{
            compCars,
            CarBrands
        },
        data(){
            return {
                brands:['Mazda','Honda','Renault'],
                cars:[
                    {model:'F9',brand:'Ferrari'},
                    {model:'911',brand:'Porsche'},
                    {model:'Tipo',brand:'Fiat'}
                ]
            }
        },
        provide(){
            return {
                cars: this.cars,
                changeCar: this.changeCar
            }
        },
        methods:{
            changeCar(){
                this.cars[0].brand = 'Renault'
            }
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