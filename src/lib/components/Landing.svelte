<script lang="ts">
    import { fade } from "svelte/transition";
    import { inview } from "svelte-inview";

    let isInview: boolean;
</script>

<div class="sm:mx-20 flex flex-col items-center sm:items-start justify-center w-full h-full" use:inview={{ rootMargin: '10px' }} on:inview_change={({detail}) => isInview = detail.inView}>
    <span id="about-us" class="invisible"></span>
    {#if isInview}
            <h2 class="font-semibold w-full mt-36 md:mt-0 text-4xl md:text-5xl" in:fade={{duration:1000}}>
                We're here<br/>
                to sweeten up<br/>
                your day!<br/>
            </h2>
            <span class="text-md pt-10 max-w-screen-md" in:fade={{delay: 200, duration: 1000}}>
                With our smooth Mochi, sweet and creamy Teh Tarik, and freezingly cold Es Serut
            </span>
    {/if}
</div>