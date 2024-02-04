<script lang="ts">
    import { inview } from "svelte-inview";

    let isInview: boolean;
</script>

<div id="our-product" class="mx-5 sm:mx-20 flex flex-col p-5 sm:p-10 w-full h-full" use:inview={{ rootMargin: '-1%' }} on:inview_change={({detail}) => isInview = detail.inView}>
    <div class="lg:grid opacity-0 transition-opacity delay-200" class:duration-1000={isInview} class:opacity-100={isInview}>
        
    </div>
</div>