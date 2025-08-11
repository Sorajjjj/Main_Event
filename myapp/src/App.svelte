<script>
    import Icon from "@iconify/svelte";
    import ButtonNavStyle from "./components/ButtonNavStyle.svelte";

</script>
<header>
    <img src="/image/logoMainEvent.png" alt="logo Main Event">
    
    <nav>
        <ButtonNavStyle href="/" label="Home" />
        <a href="">Events</a>
        <a href="">Athletes</a>
        <a href="">Rankings</a>
        <a href="">News</a>
    </nav>
    <div class="buttonHeader">
        <button type="button">
            <Icon icon="hugeicons:search-01" width="16" height="16" />
            Search</button>
        <button type="button">
            <Icon icon="hugeicons:user" width="16" height="16" />
            Profile</button>
    </div>
        
</header>

<style>

    :root{
        /* todo : a enlever pour tester les elements */
        --borderColorTest: solid red 2px;

        --borderColorDark : #414141;
        --primaryColor: #0F1119;
        --colorTextPrimary: #f7f7f7;
        --colorOpponentOne: #00E4FF;
    }

    :global(body){
        font-family: "Arimo", sans-serif;
        
        background-color: var(--primaryColor);

    }

    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 2rem;
        border-bottom: solid 1px var(--borderColorDark);
        border-image: linear-gradient(
        to right,
        rgba(0, 0, 0, 0),
        var(--borderColorDark),
        rgba(0, 0, 0, 0)
    ) 1;
    }

    /* image logo */
    header img{
        width: 150px;
    }

    header nav a{
        text-decoration: none;
        color: var(--colorTextPrimary);
        margin: 0 1rem;
        font-weight: 700;
    }

    header button[type="button"]{
        display: flex;
        align-items: center;
        border-radius: 8px;
        height: 35px;
        font-size: 0.8rem;  
        gap: 0.5rem;
        font-weight: 600;
        background-color: #1B1D25;
        color: var(--colorTextPrimary);
        border: solid 1px var(--borderColorDark);
    }

    .buttonHeader{
        display: flex;
        gap: 1rem;
        
    }
</style>
