<script lang="ts">
    import "../app.postcss"
    import "iconify-icon"
    import "overlayscrollbars/styles/overlayscrollbars.css"
    import { OverlayScrollbars } from "overlayscrollbars"
    import { browser } from "$app/environment"

    if(browser) {
        OverlayScrollbars({
            target: document.querySelector("body") as HTMLBodyElement,
        }, {
            overflow: {
                x: 'hidden'
            },
            scrollbars: {
                theme: "os-theme-light",
                autoHide: "scroll",
            }
        })
    }
</script>


<header>
    <div class="flex flex-col md:flex-row space-y-7 md:space-y-0 bg-primary-400 text-white p-5">
        <div class="flex items-center w-full md:w-max space-x-2">
            <a href="/">
                <img class="rounded-full" height=64 width=64 src="/logo.png" alt="teamochi logo">
            </a>
            <b class="text-2xl"><a href="/">Teamochi</a></b>
            <div class="flex md:hidden w-full justify-end items-center">
                <span class="flex items-center transition-all duration-200 ease-in-out hover:rotate-6 hover:translate-x-0.5 hover:text-primary-200"><a href="https://www.instagram.com/team.o.chi" target="_blank" class="flex items-center"><iconify-icon height=45 width=45 icon="fa6-brands:square-instagram" /></a></span>
            </div>
        </div>
        <div class="flex items-center flex-grow justify-end md:mx-10">
            <nav class="flex items-center justify-end space-x-3">
                <a href="#about-us" class="text-primary-100 font-semibold border-r-2 border-primary-300 pr-3 transition-colors duration-200 hover:text-white">About Us</a>
                <a href="#our-product" class="text-primary-100 font-semibold border-r-2 border-primary-300 pr-3 transition-colors duration-200 hover:text-white">Our Products</a>
                <a href="#our-member" class="text-primary-100 font-semibold transition-colors duration-200 hover:text-white">Our Member</a>
            </nav>
        </div>
        <div class="hidden md:flex justify-end items-center">
            <span class="flex items-center transition-all duration-200 ease-in-out hover:rotate-6 hover:translate-x-0.5 hover:text-primary-200"><a href="https://www.instagram.com/team.o.chi" target="_blank" class="flex items-center"><iconify-icon height=45 width=45 icon="fa6-brands:square-instagram" /></a></span>
        </div>
    </div>
</header>
<slot />


<style global lang="scss">
    @font-face {
        font-family: 'OpenSans';
        src: url("/OpenSans-VariableFont_wdth,wght.ttf")
    }

    :root {
        @apply tracking-wide text-base md:text-lg;
        box-sizing: border-box;
        // @apply font-sans;
        font-family: 'OpenSans';  
    }

    :global(.os-theme-light) {
        --os-handle-bg: theme(backgroundColor.white)
    }
</style>