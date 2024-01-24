<template>
    <div class="row">
        <div class="col-md-3 m-0 p-0">
            <SideNav :selectedComponent="selectedComponent" @update:selectedComponent="updateSelectedComponent"/>
        </div>
        <div class="col-md-1"></div>
        <div class="col-md-7 pt-5">
            <Info v-if="selectedComponent === 'Info'"/>
            <Ads v-if="selectedComponent === 'Ads'"/>
            <Plans v-if="selectedComponent === 'Plans'"/>
            <Success v-if="selectedComponent === 'Success'"/>
            <Summary v-if="selectedComponent === 'Summary'"/>
        </div>
        <div class="col-md-1"></div>
    </div>
</template>

<script setup>
    import { ref } from "vue";
    import SideNav from "./SideNav.vue";
    import Ads from "./pages/Ads.vue"
    import Info from "./pages/Info.vue";
    import Plans from "./pages/Plans.vue";
    import Success from "./pages/Success.vue";
    import Summary from "./pages/Summary.vue";

    const selectedComponent = ref('Info');

    const updateSelectedComponent = (component) =>{
        selectedComponent.value = component
    };
</script>

<style scoped>
    .row{
        width: 60vw;
        height: auto;
        margin: 0;
        padding: 0;
    }
</style>
