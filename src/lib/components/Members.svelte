<script lang="ts">
    import { inview } from "svelte-inview";
	import MemberAvatar from "./MemberAvatar.svelte";

    let isInview: boolean;
</script>

<div class="sm:mx-20 flex flex-col p-5 sm:p-10 w-full h-full" use:inview={{ rootMargin: '-1%' }} on:inview_change={({detail}) => isInview = detail.inView}>
    <h2 class="font-semibold w-full py-10 sm:pb-16 mt-0 text-3xl md:text-4xl opacity-0 transition-opacity" class:duration-1000={isInview} class:opacity-100={isInview}>
        Meet our members!
    </h2>
    <div class="grid grid-cols-2 grid-rows-5 lg:grid-cols-5 lg:grid-rows-2 md:grid-cols-3 md:grid-rows-3 gap-5 opacity-0 transition-opacity delay-100" class:duration-1000={isInview} class:opacity-100={isInview}>
        {#each ["Peter", "Cindy", "Rei", "Steven", "Sansan", "Jesslyn Felisha", "Kayne", "Gavin", "Gratia"] as member}
            <MemberAvatar url="/128.jpeg" name={member}></MemberAvatar>
        {/each}
    </div>
</div>