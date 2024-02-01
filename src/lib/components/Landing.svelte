<script lang="ts">
    import { fade } from "svelte/transition";
    import { inview } from "svelte-inview";

    let isInview: boolean;
</script>

<div class="md:mx-20 flex flex-col md:flex-row items-center md:justify-between w-full h-full" use:inview={{ rootMargin: '10px' }} on:inview_change={({detail}) => isInview = detail.inView}>
    <span id="about-us" class="invisible"></span>
    {#if isInview}
            <h2 class="font-semibold mt-36 md:mt-0 text-4xl md:text-5xl" in:fade={{duration:1000}}>
                We're here<br/>
                to sweeten up<br/>
                your day!<br/>
            </h2>
            <span class="text-sm" in:fade={{delay: 200, duration: 1000}}>
                
            </span>
    {/if}
</div>