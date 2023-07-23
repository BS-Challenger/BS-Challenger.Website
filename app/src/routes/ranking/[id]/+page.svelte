<script>
    import LevelIcon from "../../../components/LevelIcon.svelte";

    let levels = [
        {
            levelNumber: 1,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 2,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 3,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 4,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 5,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 6,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 7,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 8,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 9,
            iconURL: '/Default.png',
            color0 : '#249F76',
            color1 : '#249F76',
        },
        {
            levelNumber: 10,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 11,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 12,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        },
        {
            levelNumber: 13,
            iconURL: '/Default.png',
            color0 : '#249D76',
            color1 : '#217a5e'
        }
    ]
</script>

<svelte:head>
    <title>Support</title>
    <meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="Container">
    <div class="topSection">
        <div class="header">
            <img class="img" src="https://cdn.discordapp.com/attachments/1128488966665015307/1132486634936475728/rs.png"/>
            <p class="headerText">Ranked Saber</p>
        </div>
        <div class="seperator"/>
        <grid class="levelGrid">
            {#each levels as level}
                <LevelIcon level={level}/>
            {/each}
        </grid>
    </div>
</div>

<style>
    .Container {
        position: fixed;
        min-width: 380px;
        width: 46%;
        height: 70%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        margin-top: 2%;

        border-radius: 30px;
        background: #252525;
        box-shadow: 0 4px 4px 2px rgba(0, 0, 0, 0.25);
    }

    .topSection {
        margin-bottom: auto;
        margin-top: 15px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .header {
        display: flex;
        flex-direction: row;
        width: 600px;
        justify-content: center;
        align-items: center;
    }

    .img {
        width: 50px;
        height: 50px;
        position: relative;
        z-index: 10;

        filter: drop-shadow(5px 6px 4px #131313);
    }

    .headerText {
        margin: 0px;
        margin-left: 30px;

        color: #FFF;
        text-align: center;
        text-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
        font-family: Montserrat Alternates;
        font-size: 50px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
    }

    .seperator {
        margin-top: 10px;
        height: 5px;
        width: 700px;

        border-radius: 3px;
        background: rgba(217, 217, 217, 0.40);
    }

    .levelGrid {
        margin-top: 30px;
        width: 700px;
        height: 300px;

        display: grid;
        grid-template-columns: repeat(6, 1fr);
        grid-template-rows: repeat(6, 1fr);
        grid-column-gap: 30px;
        grid-row-gap: 20px;
    }
</style>