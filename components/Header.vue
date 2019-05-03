<template>
    <header>
        <nav>
            <ul>
                <li> <nuxt-link to="/" >Starting page</nuxt-link> </li>
                <li> <nuxt-link to="/recipes" >Recipes</nuxt-link> </li>
                <li> <nuxt-link to="/about" >About</nuxt-link> </li>
             
            </ul>
        </nav>
    </header>
</template>

<style scoped>
    header {
        width: 100%;
        height: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #521751

    }

    ul {
        list-style: none;
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    li {
        margin: 0 10px;

    }

    a {
        text-decoration: none;
        color: white;
    }

    a:hover {
        color: whitesmoke;
    }
</style>

