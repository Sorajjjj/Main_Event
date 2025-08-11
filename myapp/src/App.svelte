<script>
    import Icon from "@iconify/svelte";

</script>
<header>
    <img src="" alt="logo Main Event">
    <nav>
        <a href="">Home</a>
        <a href="">Events</a>
        <a href="">Athletes</a>
        <a href="">Rankings</a>
        <a href="">News</a>
    </nav>
    <div>
        <button type="button">
            <Icon icon="hugeicons:search-01" width="24" height="24" />
            Search</button>
        <button type="button">
            <Icon icon="hugeicons:user" width="24" height="24" />
            Profile</button>
    </div>
        
</header>

<style>

    :root{
        --primaryColor: #0F1119;
    }

    :global(body){
        background-color: var(--primaryColor);
    }

    header{
        display: flex;
        justify-content: space-between;
    }

</style>
