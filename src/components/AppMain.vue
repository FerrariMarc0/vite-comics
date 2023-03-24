<script>
    import AppMainTop from './AppMainTop.vue';
    import AppMainBottom from './AppMainBottom.vue';
    import AppCardsList from './AppCardsList.vue';
    export default{
        name: 'Dc Comics',
        components: {
            AppMainTop,
            AppCardsList,
            AppMainBottom

        }
    }
</script>

<template>
    <AppMainTop/>
    <AppCardsList/>
    <AppMainBottom/>
</template>