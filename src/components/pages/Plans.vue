
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
    <div class="switch form-check form-switch d-flex flex-row justify-content-center align-items-center">
        <p class="my-2 py-2 month" :class="{ switched: switchState === 'Monthly' }">Monthy</p>
        <input v-model="isYearly" class="form-check-input mx-2 my-1" type="checkbox" role="switch" id="flexSwitchCheckDefault">
        <p class="my-2 py-2 year" :class="{ switched: switchState === 'Yearly' }">Yearly</p>
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

</style>