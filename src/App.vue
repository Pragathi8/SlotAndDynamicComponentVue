<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click="selectedComponent='appBlue'">Load Blue Template</button>
                <button class="btn btn-success" @click="selectedComponent='appGreen'">Load Green Template</button>
                <button class="btn btn-danger" @click="selectedComponent='appRed'">Load Red Template</button>
                <hr>
                <component :is="selectedComponent">
                    <h1 slot="heading">{{heading}}</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                        Neque officia esse adipisci explicabo dignissimos nemo
                        earum harum cupiditate vero quisquam repellendus provident assumenda cum perferendis impedit, 
                        error culpa voluptates natus.
                    </p>

                </component>
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        data: function() {
            return{
            heading: "Hello World!",
            selectedComponent: ""
            }
        },
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        }
    }
</script>

<style>
</style>
