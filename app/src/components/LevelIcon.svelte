<script>
    export let level;
</script>

<div class="level">
    <div class="levelBadge">
        <p class="badgeText">Lvl: {level.levelNumber}</p>
    </div>
    <div class="iconGradient" style="
                                        background-image: linear-gradient(90deg, {level.color0}, {level.color1});
                                    ">
        <img class="icon" src={level.iconURL}/>
    </div>
</div>

<style>
    .level {
        width: 90px;
        height: 90px;

        border-radius: 25px;
        background: #3E3E3E;
        transition-duration: 0.2s;

        box-shadow: 0 30px 40px rgba(0,0,0,.21);
    }

    .level:hover {
        margin-top: -10px;
        transition-duration: 0.2s;
        cursor: pointer;
    }

    .level:active {
        transform: rotateZ(8deg);
    }

    .iconGradient{
        position:relative;
        display:inline-block;
        left: 15px;
        top: -18px;
        height: 78px;
        border-radius: 15px;
    }
    .iconGradient:after {
        content:'';
        position:absolute;
        left:0; top:0;
    }

    .icon {
        width: 60px;
        height: 78px;
        border-radius: 5px;
    }

    .levelBadge {
        z-index: 100000;
        width: 65px;
        height: 25px;
        position: relative;
        left: 12.5px;
        top: 7px;

        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;

        border-radius: 10px;
        background: linear-gradient(180deg, #70008C 0%, #491656 99.99%, rgba(0, 0, 0, 0.00) 100%);
    }

    .badgeText {
        margin: 0px;

        color: #FFF;
        text-align: center;
        font-family: Teko;
        font-size: 18px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
        letter-spacing: 2.2px;
    }
</style>