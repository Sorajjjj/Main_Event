<script>
    export let href;
    export let label;
</script>

<a class="nav_button" href={href}>{label}</a>

<style>


.nav_button::after{
    content: "";
    position: absolute;
    bottom: -6px;
    left: 0;
    width: 0%;
    height: 3px;
    background: linear-gradient(90deg,
    var(--colorOpponentOne),
    var(--colorOpponentOne)
    );
    transition: width 0.5s ease;
}

.nav_button:hover::after{
    width: 100%;
}

.nav_button:hover{
    color: var(--colorOpponentOne);
    
}

.nav_button{
        text-decoration: none;
        color: var(--colorTextPrimary);
        margin: 0 1rem;
        font-weight: 700;
        position: relative;
        display: inline-block; 
}


</style>