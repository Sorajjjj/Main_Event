<script>
    import Icon from "@iconify/svelte";
    export let label;
    export let icone;

    
</script>

<button class="buttonUser" type="button">
    {#if icone}<Icon icon={icone} width="18" height="18" />{/if}
    {label}

</button>

<style>

    
.buttonUser{
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 8px;
        height: 40px;
        width:120px ;
        font-size: 0.8rem;  
        gap: 0.5rem;
        font-weight: 600;
        background-color: #1B1D25;
        color: var(--colorTextPrimary);
        border: solid 1px var(--borderColorDark);
        transition: box-shadow 0.8s ease, border 0.2s ease ;
        background-image: linear-gradient(90deg,
        );
        cursor: pointer;

        /* effet vague */
        position: relative;
        background: transparent;
        overflow: hidden;

}

.buttonUser:hover{
    border: solid 1px var(--colorOpponentOne);
    transition: box-shadow 0.6s ease, border 0.3s ease ;
    box-shadow:
    0 0 8px var(--colorOpponentOne),
    inset 0 0 5px var(--colorOpponentOne);
    
    
    
}

.buttonUser::after{
    content: "";
    position: absolute;
    z-index: 0;
    top:0; left:0;
    height: 100%;
    width: 100%;
    background: linear-gradient(
    90deg,
    transparent 0%,
    rgba(223, 233, 236, 0.15),
    transparent 100%);

    transform: translateX(-100%);
}

.buttonUser:hover::after{
    animation: forward 1.2s ease forwards;

}

.buttonUser:not(:hover)::after{
    animation: backward 1.5s ease forwards;
}

@keyframes forward {
    0%   { transform: translateX(-150%); opacity: 0; }
    10%  { opacity: 1; }
    95%  { opacity: 1; }
    90%  { opacity: 1; }
    100% { transform: translateX(100%);  opacity: 0; }
}

@keyframes backward {
0%   { transform: translateX(120%);  opacity: 0; }
10%  { opacity: 1; }
90%  { opacity: 1; }
100% { transform: translateX(-120%); opacity: 0; }
}



</style>