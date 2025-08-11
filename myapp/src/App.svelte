<script>
    import Icon from "@iconify/svelte";
    import ButtonNavStyle from "./components/ButtonNavStyle.svelte";
    import ButtonHeaderUser from "./components/ButtonHeaderUser.svelte";
    

</script>
<header>
    <img src="/image/logoMainEvent.png" alt="logo Main Event">
    
    <nav>
        <ButtonNavStyle href="/" label="Home" />
        <ButtonNavStyle href="/" label="Events" />
        <ButtonNavStyle href="/" label="Athletes" />
        <ButtonNavStyle href="/" label="Rankings" />
        <ButtonNavStyle href="/" label="News" />
        
        
    </nav>
    <form class="buttonHeader">

        <ButtonHeaderUser icone="hugeicons:search-01"  label="Search" />
        
        <ButtonHeaderUser icone="hugeicons:search-01"  label="Profile" />
        
    </form>
        
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


    .buttonHeader{
        display: flex;
        gap: 1rem;
        
    }
</style>
