<script>
    import Icon from "@iconify/svelte";
    export let label;
    export let icone;
    
</script>

<button class="buttonUser" type="button">
    {#if icone}<Icon icon={icone} width="16" height="16" />{/if}
    {label}

</button>

<style>

.buttonUser{
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
        transition: box-shadow 0.8s ease, border 0.2s ease ;
}

.buttonUser:hover{
    border: solid 1px var(--colorOpponentOne);
    transition: box-shadow 0.6s ease, border 0.3s ease ;
    box-shadow:
    0 0 8px var(--colorOpponentOne),
    inset 0 0 5px var(--colorOpponentOne);
    
}
</style>