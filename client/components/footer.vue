<style lang="sass" module>
.footer
    margin-top: 1.5em
    font-size: 13px
    color: #a0a0a0
    min-height: 196px !important

.list
    margin-bottom: .6em !important

.item:not(:last-child)
    margin-right: 1.6em !important

.toTop
    opacity: .7

    i
        margin-right: .6em
</style>

<template lang="pug">
    .ts.bottom.attached.very.padded.horizontally.fitted.fluid.secondary.segment(:class="$style.footer")
        .ts.narrow.container
            //- 連結清單
            .ts.horizontal.link.list(:class="$style.list")
                .item(:class="$style.item"): a(href="#!", :class="$style.toTop", @click="toTop")
                    i.arrow.up.icon
                    | 回到頂部
                .item(:class="$style.item"): a(href="//github.com/TeaMeow/TocasUI/" target="_blank") GitHub
                .item(:class="$style.item"): router-link(to="/examples/") 實際範例
                .item(:class="$style.item"): router-link(to="/about/") 關於

            //- 說明
            p.
                由 <a href="http://www.facebook.com/yamiodymel">Yami Odymel</a> 所設計，還有<a href="https://github.com/TeaMeow/TocasUI/graphs/contributors">貢獻者們</a>的愛心 ❤️。原始碼授權方式為 <a href="https://github.com/TeaMeow/TocasUI/blob/master/LICENSE">MIT</a>，文件則為 <a href="https://creativecommons.org/licenses/by/4.0/deed.zh_TW">CC BY 4.0</a>，還請盡情地使用和分享，或者是一同改進 :)
</template>

<script lang="coffee">
export default
    name   : 'Footer'
    methods:
        toTop: ->
            window.scrollTo 0, 0
            document.querySelector('.pusher').scrollTop = 0
</script>