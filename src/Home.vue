<template>
    <div>
        <div class="jumbotron">
            <h1>Jumbotron heading</h1>
            <p class="lead">Cras justo odio, dapibus ac facilisis in, egestas eget quam. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.</p>
            <p><button class="btn btn-lg btn-success" role="button" @click="show = true">Sign up today</button></p>
        </div>

        <div class="row marketing">
            <div class="col-lg-6">
                <h4>Subheading</h4>
                <p>Donec id elit non mi porta gravida at eget metus. Maecenas faucibus mollis interdum.</p>

                <h4>Subheading</h4>
                <p>Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Cras mattis consectetur purus sit amet fermentum.</p>

                <h4>Subheading</h4>
                <p>Maecenas sed diam eget risus varius blandit sit amet non magna.</p>
            </div>

            <div class="col-lg-6">
                <h4>Subheading</h4>
                <p>Donec id elit non mi porta gravida at eget metus. Maecenas faucibus mollis interdum.</p>

                <h4>Subheading</h4>
                <p>Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Cras mattis consectetur purus sit amet fermentum.</p>

                <h4>Subheading</h4>
                <p>Maecenas sed diam eget risus varius blandit sit amet non magna.</p>
            </div>
        </div>

        <modal v-model="show" effect="fade">

                    <div slot="modal-header" class="modal-header" >
                        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
                        <h4 class="modal-title">Modal title</h4>
                    </div>
                    <div slot="modal-body" class="modal-body">
                        <p>One fine body&hellip;</p>
                    </div>
                    <div slot="modal-footer" class="modal-footer">
                        <button type="button" class="btn btn-default" data-dismiss="modal" @click="show = false">Close</button>
                    </div>

        </modal>


    </div>
</template>
<script>

    import Modal from 'vue-strap/src/Modal.vue';

    export default {
        data() {
            return {
                show: false
            }
        },
        components: {
            Modal
        }
    }

</script>
