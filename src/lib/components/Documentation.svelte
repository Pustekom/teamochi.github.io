<script lang="ts">
    import { inview } from "svelte-inview";

    let isInview: boolean;
</script>

<div id="our-product" class="md:mx-20 flex flex-col py-10 md:py-5 sm:p-10 w-full h-full" use:inview={{ rootMargin: '-1%' }} on:inview_change={({detail}) => isInview = detail.inView}>
    <h2 class="font-semibold text-center w-full pb-16 mt-0 text-3xl md:text-4xl opacity-0 transition-opacity" class:duration-1000={isInview} class:opacity-100={isInview}>
        In the making
    </h2>
    <div class="flex justify-center items-center opacity-0 transition-opacity delay-200" class:duration-1000={isInview} class:opacity-100={isInview}>
        <img class="md:w-3/5" src="/documentation.jpg" alt="documentation">
    </div>
</div>