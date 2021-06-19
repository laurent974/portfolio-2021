<template>
    <article>
        <nuxt-content :document="portfolio" />
    </article>
</template>

<script>
export default {
    async asyncData({ $content, params}) {
        const portfolio = await $content('portfolio', params.slug).fetch()

        return { portfolio }
    }
}
</script>

<style scoped>

</style>