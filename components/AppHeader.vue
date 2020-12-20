<template>
    <div>
        <h1>Header</h1>
        <ul>
            <li>
                <nuxt-link to="/">Home Page</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/about">About</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/jokes">Jokes</nuxt-link>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'AppHeader'
}
</script>