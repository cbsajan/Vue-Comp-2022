<template>
    <h3>Mike is on</h3>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Steve',
    activated() {
        console.log('hello Steve!!')
    },
    deactivated() {
        console.log('by Steve!!')
    },
    unmounted() {
        console.log('Steve unmounted')
    }
}
</script>