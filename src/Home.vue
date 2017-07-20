<template>
    <div>
        <div class="jumbotron">
            <h1>Jumbotron heading</h1>
            <p class="lead">Cras justo odio, dapibus ac facilisis in, egestas eget quam. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.</p>
            <p><button class="btn btn-lg btn-success" role="button" @click="show = true">Sign up today</button></p>
        </div>

        <!--<async-component></async-component>-->

        <div v-if="below">
            <below-fold></below-fold>
        </div>

        <home-modal v-if="show":show="show"></home-modal>

    </div>
</template>
<script>

    import Vue from 'vue';
    //Vue.component('async-component', () => import(/* webpackChunkName: "async" */ './AsyncComponent.js'));

    //const HomeModal = () => import(/* webpackChunkName: "modal" */ './HomeModal.vue');
    import HomeModal from './HomeModal.vue';
    //const BelowFold = () => import(/* webpackChunkName: "below-fold" */ './BelowFold.vue');
    import BelowFold from './BelowFold.vue';


    export default {
        data() {
            return {
                show: false,
                below: false
            }
        },
        created() {
            setTimeout(() => {
                this.below = true;
            }, 2000);
        },
        components: {
            HomeModal,
            BelowFold
        }
    }

</script>
