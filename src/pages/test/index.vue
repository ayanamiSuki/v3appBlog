<template>
    <div class="app-container">
        <UsePinia />
        <br />
        <router-link to="/login">点击跳转至login</router-link>
        <br /><br />
        <router-link to="/vueUse">点击跳转至vueUse页面</router-link>
        <br /><br />
        <router-link to="/request">点击跳转至request请求页面</router-link>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';
    import UsePinia from '@/components/UsePinia.vue';

    export default defineComponent({
        name: 'IndexPage',
        components: {
            UsePinia
        }
    });
</script>
<style lang="scss" scoped>
    .app-container {
    }
</style>
