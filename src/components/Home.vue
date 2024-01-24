<template>
    <div class="row">
        <div class="col-md-3 m-0 p-0">
            <SideNav/>
        </div>
        <div class="col-md-1"></div>
        <div class="col-md-7 pt-5">
            <Info/>
        </div>
        <div class="col-md-1"></div>
    </div>
</template>

<script setup>
    import SideNav from "./SideNav.vue";
    // import Ads from "./pages/Ads.vue"
    import Info from "./pages/Info.vue";
    // import Plans from "./pages/Plans.vue";
    // import Success from "./pages/Success.vue";
    // import Summary from "./pages/Summary.vue";
</script>

<style scoped>
    .row{
        width: 60vw;
        height: auto;
        margin: 0;
        padding: 0;
    }
</style>
