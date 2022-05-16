
<template>
    <h3>Mike is on</h3>
</template>

<script>
export default {
    /* eslint-disable */

    name: "Mike",
    activated() {
        console.log('hello mike!!')
    },
    deactivated() {
        console.log('by mike!!')
    },
    unmounted() {
        console.log('Mike unmounted')
    }
}
</script>