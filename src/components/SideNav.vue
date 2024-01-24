<template>
    <section class="d-flex justify-content-start align-items-top pt-4">
        <ol>
            <li>
                <h6>STEP 1</h6>
                <h5>YOUR INFO</h5>
            </li>
            <li>
                <h6>STEP 2</h6>
                <h5>SELECT PLAN</h5>
            </li>
            <li>
                <h6>STEP 3</h6>
                <h5>ADD-ONS</h5>
            </li>
            <li>
                <h6>STEP 4</h6>
                <h5>SUMMARY</h5>
            </li>
        </ol>
    </section>
</template>
<script>

</script>
<style scoped>

    @font-face {
        font-family: 'Ubuntu-Bold';
        src: url('../assets/fonts/Ubuntu-Bold.ttf') format('woff2');
        font-weight: normal;
        font-style: normal;
    }

    @font-face{
        font-family: 'Ubuntu-Regular';
        src: url('../assets/fonts/Ubuntu-Regular.ttf') format('woff2');
        font-weight: normal;
        font-style: normal;
    }

    section{
        height: calc(75vh - 1.6em)!important;
        margin: 0;
        padding: 0;
        /* width: 18vw; */
        background: url("../assets/images/bg-sidebar-desktop.svg") no-repeat center center / cover;
        border-radius: 0.6em;
    }

    ol{
        /* list-style: none; */
        counter-reset: my-counter;
        padding-left: 1em;
    }

    ol > li{
        position: relative;
        margin: 0 0 6px 2em;
        padding: 4px 16px;
        list-style:none;
        color: #ffffff;
        cursor: pointer;
    }

    ol > li::before{
        content: counter(my-counter);
        counter-increment: my-counter;
        border: 1px #ffffff solid!important;
        position: absolute;
        left: -1.8em;
        top: 1px;
        -moz-box-sizing: border-box;
        -webkit-box-sizing: border-box;
        box-sizing: border-box;
        width: 2em;
        height: 2em;
        color: #ffffff;
        border-radius: 50%;
        padding-top: 1px;
        margin-top: 4px;
        font-size: 0.8em;
        font-family: 'Ubuntu-Regular';
        text-align: center!important;
    }

    ol > li:hover::before{
        background-color: hsl(206, 94%, 87%);
        border: 1px hsl(206, 94%, 87%) solid!important;
        color: hsl(213, 96%, 18%);
    }

    ol li{
        margin: 1.25em 1em 0em 2em;
    }

    ol li h6, ol li h5{
        margin: 0;
        padding: 0;
    }

    ol li h6{
        font-family: 'Ubuntu-Regular';
        font-weight: 400;
        opacity: 0.6;
        font-size: 65%;
    }

    ol li h5{
        font-size: 0.7em;;
        font-family: 'Ubuntu-Bold';
        letter-spacing: 0.125em;
        font-weight: 500;
    }

</style>