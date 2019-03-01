<template>
    <div>
        <div class="intro-cover">
            <div class="intro-cover__info">
                <h1> <span>{{ boldHead }}</span> {{ heading }} </h1>
                <h3> {{ subInfo }} </h3>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderIntro',
    props: {
        heading: String,
        boldHead: String,
        subInfo: String
    }
}
</script>

<style lang="scss">

</style>
