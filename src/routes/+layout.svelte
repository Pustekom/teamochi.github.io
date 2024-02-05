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
    <div class="flex flex-col md:flex-row bg-primary-400 text-white h-[20dvh]">
        <div class="flex items-center w-full md:w-max space-x-2 min-w-max p-5">
            <a href="/" class="min-w-max">
                <img class="rounded-full max-w-full" height=64 width=64 src="/logo.png" alt="teamochi logo">
            </a>
            <b class="text-2xl"><a href="/">Teamochi</a></b>
            <div class="flex md:hidden w-full justify-end items-center">
                <span class="flex items-center transition-all duration-200 ease-in-out hover:rotate-6 hover:translate-x-0.5 hover:text-primary-200"><a href="https://www.instagram.com/team.o.chi" target="_blank" class="flex items-center"><iconify-icon height=45 width=45 icon="fa6-brands:square-instagram" /></a></span>
            </div>
        </div>
        <div class="flex items-center w-full flex-grow justify-center  md:justify-end md:mx-5 md:py-0 text-sm">
            <nav class="flex items-center justify-end space-x-3 scroll-smooth">
                <a href="#about-us" class="text-primary-100 font-semibold border-r-2 border-primary-300 pr-3 transition-colors duration-200 hover:text-white" data-sveltekit-reload>About Us</a>
                <a href="#our-products" class="text-primary-100 font-semibold border-r-2 border-primary-300 pr-3 transition-colors duration-200 hover:text-white" data-sveltekit-reload>Our Products</a>
                <a href="#our-members" class="text-primary-100 font-semibold transition-colors duration-200 hover:text-white" data-sveltekit-reload>Our Members</a>
            </nav>
        </div>
        <div class="hidden md:flex px-5 justify-end items-center">
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
        @apply tracking-wide text-base sm:text-lg transition-all duration-200;
        box-sizing: border-box;
        // @apply font-sans;
        font-family: 'OpenSans';
    }

    :global(.os-theme-light) {
        --os-handle-bg: theme(backgroundColor.white)
    }
</style>