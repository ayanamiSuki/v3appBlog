<template>
    <div class="header p-20 ui-flex col-center row-between">
        <div class="logo">logo</div>
        <div class="list-wrapper ui-flex">
            <li
                v-for="item in list"
                :key="item.label"
                class="list f-m t-bolder pointer"
                :class="active === item.label && 'active'"
                @click="changeTbas(item)"
                >{{ item.label }}</li
            >
        </div>
        <div class="login">login</div>
    </div>
</template>

<script lang="ts" setup>
    import { ref } from 'vue';
    import { useRouter } from 'vue-router';

    const router = useRouter();
    // https://juejin.cn/post/7009282373476941831#heading-4 不会来查
    interface tabsList {
        label: string;
        url: string;
    }
    const list: Array<tabsList> = [
        { label: 'login', url: '/login' },
        { label: 'request', url: '/request' },
        { label: 'vueUse', url: '/vueUse' }
    ];
    let active = ref('example');
    const changeTbas = (item: tabsList) => {
        console.log(item.label);
        active.value = item.label;
        router.push(item.url);
    };
</script>

<style lang="scss" scoped>
    .logo {
        font-size: 34px;
        font-weight: bol;
    }
    .list-wrapper {
        .list {
            width: 150px;
            text-align: center;
            &.active {
                color: red;
            }
        }
    }
</style>
