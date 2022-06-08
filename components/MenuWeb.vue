<template>
    <div class="nav_menu">
        <nav class="menu_icons">
            <NuxtLink to="/index">
                <button class="nav_button_w">
                    inicio        
                </button>
            </NuxtLink>
            <NuxtLink to= "/horario">
                <button class="nav_button_w">
                    horario               
                </button>
            </NuxtLink>
            <NuxtLink to="/noticias">
                <button class="nav_button_w">
                    noticias
                </button>
            </NuxtLink>
            <NuxtLink to="/biblioteca">
                <button class="nav_button_w">
                    biblioteca
                </button>
            </NuxtLink>
            <NuxtLink to="/search">
                <button class="nav_button_search">
                   <img src="/isearch.svg" alt="search_bar">
                </button>
            </NuxtLink>
        </nav>
        <div class="background"></div>
    </div>
</template>

<style lang="postcss" scoped>


    .nav_menu{
        display: block;
        top: 0;

    }
    .menu_icons{
        display: flex;
        top: 0;
        position: fixed;
        z-index: 9999;
        width: 100%;
        height: 85px;
        justify-content: center;
        flex-direction: row;
        align-items: center;
        list-style-type: none;

    }
    .nav_button_w{
        display: flex;
        flex-direction: column;
        font-size: 20px;
        height: 40px;
        background-color: transparent;
        border-color: transparent;
        /* 0grey_light */
        background: #E6E9EB;
        border-radius: 50%;
        padding: 24px 40px;
        align-items: center;
        justify-content: center;
        /* button light */
        box-shadow: 0px 7px 7px rgba(0, 0, 0, 0.05), 0px -1px 5px rgba(8, 8, 10, 0.02), inset 0px -3px 17px rgba(0, 0, 0, 0.04);
    }
    .nav_button_search{
        background: #E6E9EB;
        border-radius: 100%;
        border-color: transparent;
        box-shadow: 0px 7px 7px rgba(0, 0, 0, 0.05), 0px -1px 5px rgba(8, 8, 10, 0.02), inset 0px -3px 17px rgba(0, 0, 0, 0.04);
    }
    .nav_button_search img{
        height: 40px;
    }
    .background{
        position: fixed;
        left: 0;
        width: 100%;
        height: 85px;
        top:0;
        z-index: 1;
        display: block;
        background: #43DB7F;
        border-radius: 0px 0px 50px 50px;
    }
@media (max-width: 511px){
   .nav_menu{
        display: none;
        bottom: 0;
    }
}
</style>