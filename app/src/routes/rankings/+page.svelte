<script>
    let rankings = [
        {
            name: "Ranked Saber",
            icon: "https://cdn.discordapp.com/attachments/1128488966665015307/1132486634936475728/rs.png",
            activeUsers: 0,
            weeklyScores: 0
        },
        {
            name: "Tech Saber",
            icon: "https://cdn.discordapp.com/icons/1077667009996800131/0a8f79277b89595cccc3d034bbc13bf8.webp?size=96",
            activeUsers: 0,
            weeklyScores: 0
        }
    ]
</script>

<svelte:head>
    <title>Support</title>
    <meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="Container">
    <div class="topSection">
        <p class="header">All Rankings</p>
        <div class="seperator"/>
        <div class="texts">
            <p class="activeUsers">Active Users</p>
            <p class="weeklyScores">Weekly Scores</p>
        </div>
    </div>
    <div class="rankingsContainer">
        {#each rankings as ranking}
            <div class="ranking">
                <img class="rankingImg" src="{ranking.icon}" />
                <p class="rankingName">{ranking.name}</p>
                <div class="textsContainer">
                    <div class="rankingTexts">
                        <p class="rankActive">{ranking.activeUsers}</p>
                        <p class="rankWeekly">{ranking.weeklyScores}</p>
                    </div>
                    <div class="rankingTexts">
                        <div class="textSeperator"/>
                        <div class="textSeperator"/>
                    </div>
                </div>
            </div>
        {/each}
    </div>
</div>

<style>
    .rankingName {
        margin-left: 15px;
        width: 50%;

        color: #FFF;
        font-family: Montserrat Alternates;
        font-size: 20px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
    }

    .seperator {
        width: 100%;
        height: 5px;

        border-radius: 3px;
        background: rgba(217, 217, 217, 0.40);
    }

    .header {
        margin-top: 0px;
        margin-bottom: 10px;

        color: #FFF;
        text-align: center;
        text-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
        font-family: Montserrat Alternates;
        font-size: 50px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
    }

    .Container {
        position: fixed;
        min-width: 380px;
        width: 46%;
        height: 78%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        border-radius: 30px;
        background: #252525;
        box-shadow: 0px 4px 4px 2px rgba(0, 0, 0, 0.25);
    }

    .rankingsContainer {
        width: 95%;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: auto;
    }

    .ranking {
        min-width: 350px;
        width: 100%;
        height: 60px;
        margin-bottom: 31px;

        display: flex;
        flex-direction: row;
        align-items: center;

        border-radius: 19px;
        background: #535353;
        box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);

    }

    .rankingImg {
        width: 50px;
        height: 50px;
        margin-top: auto;
        margin-bottom: auto;
        margin-left: 8px;

        border-radius: 10px;
    }

    .topSection {
        width: 90%;
        height: 160px;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .texts {
        margin: 0px 0px 0px auto;
        padding-right: 0px;
        display: flex;
        flex-direction: row;
        width: 35%;
        min-width: 160px;
        justify-content: space-around;
        position: relative;
        align-items: end;
    }

    .weeklyScores,.activeUsers {
        color: #FFF;
        text-align: center;
        font-family: Heebo;
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
        margin-bottom: 0px;
    }

    .textsContainer {
        padding-right: 15px;
        width: 100%;
        display: flex;
        flex-direction: column;
        height: fit-content;
    }

    .rankingTexts {
        margin-left: auto;
        padding-right: 20px;
        width: 55%;

        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-around;
    }

    .rankActive,.rankWeekly {
        color: #FFF;
        text-align: center;
        font-family: Heebo;
        font-size: 20px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
        margin-bottom: 0px;
        margin-top: 0px;
    }

    .textSeperator {
        height: 5px;
        width: 15px;

        border-radius: 3px;
        background: rgba(217, 217, 217, 0.40);
    }
</style>