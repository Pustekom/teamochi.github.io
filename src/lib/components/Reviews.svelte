<script lang="ts">
    import { inview } from "svelte-inview";

    let isInview: boolean;
</script>

<div id="our-product" class="md:mx-20 flex flex-col p-5 sm:p-10 w-full h-full" use:inview={{ rootMargin: '-1%' }} on:inview_change={({detail}) => isInview = detail.inView}>
    <h2 class="font-semibold text-center w-full pb-16 mt-0 text-3xl md:text-4xl opacity-0 transition-opacity" class:duration-1000={isInview} class:opacity-100={isInview}>
        Testimony
    </h2>
    <div class="flex justify-center items-center opacity-0 transition-opacity delay-200" class:duration-1000={isInview} class:opacity-100={isInview}>
        <ul id="reviews" class="grid grid-cols-1 grid-rows-8 gap-5 md:grid-cols-2 md:grid-rows-4 lg:gap-10">
            <li>“Rasanya enak dan unik, seperti Ice Cream”</li>
            <li>“Ukurannya cukup satu mulut”</li>
            <li>“Isian mochinya lembut dan lumer di mulut”</li>
            <li>“Enak, kulit luar mochinya kenyal”</li>
            <li>“Enak, manisnya pas. Rasa mochinya kerasa</li>
            <li>“Harganya terjangkau”</li>
            <li>“Ukurannya ideal”</li>
            <li>“Enak dan segar”</li>
        </ul>
    </div>
</div>


<style lang="scss">
    #reviews li {
        @apply bg-primary-100 p-5 flex items-center border-l-8 border-primary-900 rounded-r-sm;
    }
</style>