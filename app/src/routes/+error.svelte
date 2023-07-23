<script>
    import { page } from '$app/stores';
    import {onMount} from "svelte";

    let url = '';
    onMount(async () => {
        let api = Math.random() < 0.5;
        url = api ? 'https://httpcats.com/' : 'https://http.cat/';
    });
</script>

<svelte:head>
    <title>Error</title>
    <meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="errorContainer">
    <img class="image" src="{url + $page.status + '.jpg'}">
</div>


<style>
    .errorContainer {
        position: fixed;
        width: 44%;
        height: fit-content;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        left: 50%;
        margin-left: -22%;


        border-radius: 19px;
        box-shadow: 0px 4px 4px 2px rgba(0, 0, 0, 0.25);
    }

    .image {
        margin-top: 17px;
        margin-bottom: 20px;
        width: 95%;

        border-radius: 25px;
        box-shadow: 0px 4px 4px 2px rgba(0, 0, 0, 0.25);
    }
</style>