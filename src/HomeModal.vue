<template>
    <modal v-model="show" effect="fade">

        <div slot="modal-header" class="modal-header" >
            <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
            <h4 class="modal-title">Sign Up Form</h4>
        </div>
        <div slot="modal-body" class="modal-body">
            <p>One fine body&hellip;</p>
        </div>
        <div slot="modal-footer" class="modal-footer">
            <button type="button" class="btn btn-default" data-dismiss="modal" @click="show = false">Close</button>
        </div>

    </modal>
</template>
<script>
    import Modal from 'vue-strap/src/Modal.vue';

    export default {
        props: ['show'],
        components: {
            Modal
        }
    }
</script>
