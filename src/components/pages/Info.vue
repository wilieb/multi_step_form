<template>
    <h2><b>Personal Info</b></h2>
    <p>Please provide your name, email address, and phone number</p>
    <form class="pt-1">
        <div>
            <div class="lable">
                <p class="mb-0 mt-2">Name</p>
                <p class="err mb-0 mt-2">This field is required</p>
            </div>
            <input class="form-control" type="text" name="text" id="text" placeholder="eg. Stephen King">
            <input class="err" type="text" name="text" id="text" placeholder="eg. Stephen King">
        </div>
        <div>
            <div class="lable">
                <p class="mb-0 mt-2">Email Address</p>
                <p class="err mb-0 mt-2">This field is required</p>
            </div>
            <input class="form-control" type="email" name="email" id="email" placeholder="eg. stephenking@lorem.com">
            <input class="err" type="email" name="email" id="email" placeholder="eg. stephenking@lorem.com">
        </div>
        <div>
            <div class="lable">
                <p class="mb-0 mt-2">Phone</p>
                <p class="err mb-0 mt-2">This field is required</p>
            </div>
            <input class="form-control" type="number" name="number" id="number" placeholder="eg. +1 234 567 890">
            <input class="err" type="number" name="number" id="number" placeholder="eg. +1 234 567 890">
        </div>
    </form>
    <div class="d-flex flex-row-reverse pt-4 mb-0 me-0 pe-0">
        <button type="button" class="btn btn-dark">Next Step</button>
    </div>
</template>

<script setup>

</script>

<style scoped>
    .err{
        display: none;
    }

    h2{
        color: hsl(213, 96%, 18%);
        font-weight: 700;
    }

    p{
        color: hsl(231, 11%, 63%);
    }

    .lable p{
        color: hsl(213, 96%, 18%);
    }

    button{
        background-color: hsl(213, 96%, 18%)!important;
        border: none;
        padding: 0.6em 1.2em;
    }

    button:hover, button:active, button:focus{
        background-color: hsla(213, 96%, 18%, 0.815);
    }
</style>