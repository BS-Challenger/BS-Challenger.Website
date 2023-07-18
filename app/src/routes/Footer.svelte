<script>
    import Seperator from "./Seperator.svelte";
</script>

<footer>
    <nav>
        <div class="footer">
            <a href="https://github.com/BS-Challenger" class="footerItem">
                Github
            </a>
            <Seperator/>
            <a href="/" class="footerItem">
                API
            </a>
            <Seperator/>
            <a href="/" class="footerItem">
                Support
            </a>
            <Seperator/>
            <a href="/"  class="footerItem">
                Patreon
            </a>
            <Seperator/>
            <a href="https://discord.gg/wh5nJse4tQ" class="footerItem">
                Discord
            </a>
        </div>
    </nav>
</footer>

<style>
    p, a {
        color: #FFF;
        font-family: Montserrat Alternates;
        font-size: 35px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
    }

    .footer {
        width: 90%;
        height: 50px;
        flex-shrink: 0;
        border-radius: 25px 25px 0px 0px;
        border: 8px solid #804228;
        background: linear-gradient(90deg, #A8684E 0%, #824B35 100%);
        box-shadow: 0px 4px 4px 4px rgba(0, 0, 0, 0.25);

        display: flex;
        justify-content: center;
        align-items: center;

        bottom: -8px;
        position: fixed;
    }

    .footerItem {
        font-size: 20px;
        transition-duration: 0.1s;
    }

    .footerItem:hover {
        color: #CAA8F5;
        transform: rotateX(25deg);
        transition-duration: 0.1s;
        cursor: pointer;
    }

    nav {
        display: flex;
        justify-content: center;
        --background: rgba(255, 255, 255, 0.7);
    }
</style>
