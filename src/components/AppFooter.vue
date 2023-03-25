<script>
    import AppTopFooter from './AppTopFooter.vue';
    import AppBottomFooter from './AppBottomFooter.vue';

    export default{
        name: 'Footer',
        components: {
            AppTopFooter,
            AppBottomFooter
        }
    }
</script>

<template>
    <AppTopFooter/>
    <AppBottomFooter/>
</template>