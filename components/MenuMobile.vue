<template>
    <div class="nav_menu">
        <nav class="menu_icons">
            <NuxtLink to="/index">
                <button class="nav_button">
                    <img src="/inicio.svg" alt="Inicio">
                    <a>inicio</a>                    
                </button>
            </NuxtLink>
            <NuxtLink to= "/horario">
                <button class="nav_button">
                    <img src="/horario.svg" alt="Horario">
                    <a>horario</a>                  
                </button>
            </NuxtLink>
            <NuxtLink to="/buscador">
                <button class="nav_button">
                    <img src="/search_green.svg" alt="buscador">
                </button>
            </NuxtLink>
            <NuxtLink to="/noticias">
                <button class="nav_button">
                    <img src="/noticias.svg" alt="Noticias">
                    <a>noticias</a> 
                    </button>
            </NuxtLink>
            <NuxtLink to="/biblioteca">
                <button class="nav_button">
                    <img src="/biblioteca.svg" alt="Biblioteca">
                    <a>biblioteca</a> 
                </button>
            </NuxtLink>
        </nav>
        <div class="blur"></div>
    </div>
</template>

<style lang="postcss" scoped>
    .nav_menu{
        display: none;
        bottom: 0;
    }

@media (max-width: 510px){
    .nav_menu{
        display: block;
        width: 100%;
        bottom: 0;
    }
    .menu_icons{
        display: flex;
        bottom: 0;
        position: fixed;
        z-index: 9999;
        width: 100%;
        height: 85px;
        flex-direction: row;
        align-items: center;
        justify-content: space-around;
        list-style: none;
        list-style-type: none;

    }
    .nav_button{
        display: flex;
        flex-direction: column;
        font-size: 12px;
        height: 40px;
        background-color: transparent;
        border-color: transparent;
    }
    .nav_button img{
        width: 40px;
    }
    .menu_icons nav_button:nth-child(){
        align-self: stretch;
    }
    .blur{
        position: fixed;
        width: 100%;
        height: 85px;
        bottom:0;
        background: linear-gradient(152.97deg, rgba(255, 255, 255, 0) 0%, rgba(230, 233, 235, 0.5) 92.19%);
        z-index: 1;
        display: block;
        backdrop-filter: blur( 35px );
    }
}
</style>