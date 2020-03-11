<template>
    <nav>
        <h1>{{ title }}</h1>
    </nav>
</template>
<script>
export default {
    data: () => {
       return {
            title: 'Hello from Header',
       }
    },
}
</script>
<style lang="scss" scoped>
    nav {
        border: 1px solid black;
        background: #fff;
    }
</style>