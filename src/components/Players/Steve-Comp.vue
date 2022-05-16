<template>
    <h3>Mike is on</h3>
    <teleport to="#dialog_here">
        <comp-modal></comp-modal>
    </teleport>
</template>

<script>
import compModal from "../Utils/Modal-Comp.vue";
export default {
    components: {
        compModal
    },
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Steve',

    unmounted() {
        console.log('Steve unmounted')
    }
}
</script>