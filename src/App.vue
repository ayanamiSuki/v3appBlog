<template>
    <pageHeader />
    <RouterView />
</template>

<script lang="ts" setup>
    import pageHeader from '@/pages/layout/pageHeader.vue';
</script>
<style lang="scss">
    // https://www.ui8.net/?rel=tmtt 素材库
    @import '@/assets/scss/index.scss';
</style>
