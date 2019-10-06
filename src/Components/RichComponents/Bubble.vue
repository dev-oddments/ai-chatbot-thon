<template>

         <span class="bubble" :class="{'me': from == 'me', 'loading': loading}">
          {{text}}
        </span>


</template>

<style lang="sass" scoped>
.bubble
    padding: 12px
    border-radius: 0px 15px 15px 15px
    color: var(--text)
    border: 1px solid var(--border)
    display: inline-block
    position: relative
    background-color: rgb(230,237,241)
    min-width: 26px


    &.me
        float: right
        background-color: rgb(74,77,137)
        border: 1px solid var(--element-background)
        color: white
        margin-top: 0px
        border-radius: 15px 15px 0px 15px

        &::before
            content: ''




    &.loading
        height: 16px
        animation: loading .8s ease infinite

@keyframes loading
    0%
        opacity: 0
    50%
        opacity: 1
    100%
        opacity: 0
</style>

<script>
export default {
    name: 'Bubble',
    props: ['text', 'from', 'loading']
}
</script>