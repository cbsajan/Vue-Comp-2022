<template>
    <div>
        <app-header></app-header>
            <div class="container">
                <comp-user-profile 
                    :alsoKnowAs="name"
                    :userLastname="lastname"
                    :userAge="age"
                    :userParents="parents"
                    @update-lastname="lastname = $event"
                    @say-hello="alertHello" 
                    :updateAge="updateAge"
                ></comp-user-profile>
                <button @click="updateName">Update name</button>
            </div>
        <app-footer></app-footer>
    </div>
</template>

<script>
    import compUserProfile from './components/User/Profile-Comp.vue';
    export default {
        components:{
            compUserProfile
        },
        data(){
            return {
                name: 'Rocket',
                lastname:'C B ',
                age:28,
                parents:{
                    father:'Something...',
                    mother:'Something...'
                }
            }
        },
        methods:{
            updateName(){
                this.name ='Intelligent'
            },
            alertHello(){
                alert('Hello ' + this.name)
            },
             updateAge(age_new){
                this.age = age_new
                console.log(age_new)
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