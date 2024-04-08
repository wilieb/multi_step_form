
import { computed } from 'vue';

import { computed } from 'vue';

import { slotFlagsText } from '@vue/shared';
<template>
    <h2><b>Select your plan</b></h2>
    <p>You have the option of monthly or yearly billing.</p>
    <div class="row">
        <div class="col-sm-4 mb-3 mb-sm-0">
            <div class="card">
                <a href="#" class="btn">
                    <div class="card-body flex-column ps-1 py-1">
                        <img class="mb-4" src='@/assets/images/icon-arcade.svg' alt="svg">
                        <p class="card-text mb-0 pb-0"><b>Arcade</b></p>
                        <p class="py-0 my-0">$9/mo</p>
                    </div>
                </a>
            </div>
        </div>
        <div class="col-sm-4">
            <div class="card">
                <a href="#" class="btn">
                    <div class="card-body flex-column ps-1 py-1">
                        <img class="mb-4" src="@/assets/images/icon-advanced.svg" alt="svg">
                        <p class="card-text mb-0 pb-0"><b>Advanced</b></p>
                        <p class="py-0 my-0">$12/mo</p>
                    </div>
                </a>
            </div>
        </div>
        <div class="col-sm-4">
            <div class="card">
                <a href="#" class="btn">
                    <div class="card-body flex-column ps-1 py-1">
                        <img class="mb-4" src="@/assets/images/icon-pro.svg" alt="svg">
                        <p class="card-text mb-0 pb-0"><b>Pro</b></p>
                        <p class="py-0 my-0">$15/mo</p>
                    </div>
                </a>
            </div>
        </div>
    </div>
    <div class="switch form-check" id="switch">
        <p class="pb-0 mb-0 px-2 month" :class="{ switched: switchState === 'Monthly' }">Monthy</p>
        <v-switch class="" v-model="isYearly" id="flexSwitchCheckDefault" style="margin-top: 1.2em;"></v-switch>
        <p class="pb-0 mb-0 px-2 year" :class="{ switched: switchState === 'Yearly' }">Yearly</p>
    </div>
    <div class="btns-div">
        <a href="" class="btnp">Go Back</a>
        <button type="button" class="btn btn-dark">Next Step</button>
    </div>
</template>
<script setup>
    import { ref, computed } from "vue";
    const isYearly = ref(true)
    const switchState = computed(() => (isYearly.value ? "Yearly" : "Monthly"));
</script>

<style scoped>

    input, input:active, input:focus{
        background: hsl(213, 96%, 18%);
    }

    input:checked{
        background-color: hsl(213, 96%, 18%); 
    }

    .card-body{
        display: flex;
        align-items: flex-start;
    }

    h2, p.card-text{
        color: hsl(213, 96%, 18%);
        font-weight: 700;
        flex-grow: 1!important;
    }

    #switch{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        background-color: hsl(217, 100%, 97%);
        border-radius: 0.45em;
        margin-top: 1em;
        padding: 0 1em!important;
        height: 10%;
    }

    p, .switch p{
        color: hsl(231, 11%, 63%);
    }

    p.switched{
        color: hsl(213, 96%, 18%);
    }

    a:hover{
        border-color: hsl(243, 100%, 62%);
    }

    a:active, a:focus{
        border-color: hsl(243, 100%, 62%);
        background: hsl(217, 100%, 97%);
    }

    .btns-div {
        display: flex;
        justify-content: space-between;
        margin-top: 10.5%;
    }

    .btnp{
        text-decoration: none;
        color: hsl(213, 96%, 18%);
        font-weight: 700;
        margin-top: 8px;
    }

    .btn{
        margin: 5px;
    }

    button{
        background-color: hsl(213, 96%, 18%)!important;
        border: none;
        padding: 0.6em 1.2em;
        color: white;
    }

    button:hover, button:focus{
        /* background-color: hsl(217, 100%, 97%); */
        background-color: hsla(213, 96%, 18%, 0.651);
    }

</style>