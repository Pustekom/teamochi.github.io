<script lang="ts">
    import { fade } from "svelte/transition";
    import { inview } from "svelte-inview";

    let isInview: boolean;
</script>

<div class="sm:mx-20 flex flex-col p-10 items-center sm:items-start justify-center w-full h-full" use:inview={{ rootMargin: '-1%' }} on:inview_change={({detail}) => isInview = detail.inView}>
    <h2 class="font-semibold w-full text-4xl md:text-5xl opacity-0 transition-opacity delay-100" class:duration-1000={isInview} class:opacity-100={isInview}>
        We're here<br/>
        to bring<br/>
        familiar flavours<br/>
        to your tastebud!<br/>
    </h2>
    <span class="text-md pt-10 max-w-screen-md opacity-0 transition-opacity delay-200" class:duration-1000={isInview} class:opacity-100={isInview}>
        We embody the spirit of innovation fused with the richness of local flavors. As a collective of young entrepreneurs, we are passionate about redefining modern cuisine by infusing it with the authentic essence of our cultural heritage.
        <br/><br/>
        Our journey began with a deep-rooted appreciation for traditional flavors, which we skillfully blend with contemporary techniques to create culinary experiences that resonate with the discerning palate of today's consumers.
        <br/><br/>
        Committed to sustainability and community engagement, we source our ingredients locally, forging meaningful partnerships with farmers and producers who share our commitment to quality and ethical practices. By championing local suppliers, we not only uphold the integrity of our dishes but also contribute to the socio-economic growth of our communities.
    </span>
</div>