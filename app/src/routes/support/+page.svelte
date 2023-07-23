<svelte:head>
    <title>Support</title>
    <meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="supportContainer">
    <p class="supportSubText">If you need support you can visit our Discord</p>
</div>


<style>
    .supportContainer {
        position: fixed;
        top: 30%;
        width: 40%;
        height: 312px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        left: 50%;
        margin-left: -20%;

        border-radius: 30px;
        background: #252525;
        box-shadow: 0px 4px 4px 2px rgba(0, 0, 0, 0.25);
    }

    .supportSubText {
        color: #FFF;
        text-align: center;
        font-family: Heebo;
        font-size: 25px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
    }
</style>