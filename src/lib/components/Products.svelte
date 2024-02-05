<script lang="ts">
    import { inview } from "svelte-inview";
	import ProductAvatar from "./ProductAvatar.svelte";

    let isInview: boolean;
    const products = [
        {name: "Mochi", description: "We chose to combine mochi, which is a typical Japanese food that is very popular in Indonesia, in the form of a cake made from sticky rice which has a soft and sticky texture and is shaped into small balls with various flavors of local specialties, namely 'Es Doger', 'Pisang Ijo', 'Soda Gembira', 'Kopi', and 'Klepon'", icon: "/mochi.jpg"},
        {name:"Teh Tarik", description: "Our Teh Tarik is unique, where all the ingredients we use come from Indonesia. Starting from the tea leaves to the milk, everything is local. The uniqueness of our tea also comes from the attractions that we will do in sales. We sell this Teh Tarik in 500 ml size, which is the ideal size because it is suitable for the price.", icon: "/teh_tarik.jpg"},
        {name:"Es Serut", description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed fringilla nisi vitae rutrum aliquet. Curabitur vitae pellentesque ex, a pulvinar lectus. Integer vitae dapibus libero. Cras dignissim dui eu tortor porta, nec feugiat quam volutpat. Cras eget massa quis sem venenatis sagittis et pellentesque lectus. Vivamus gravida rutrum interdum. Lorem.", icon: "/128.jpeg"}
    ]
</script>

<div id="our-product" class="mx-5 sm:mx-20 flex flex-col p-5 sm:p-10 w-full h-full" use:inview={{ rootMargin: '-1%' }} on:inview_change={({detail}) => isInview = detail.inView}>
    <h2 class="font-semibold w-full text-center py-10 sm:pb-28 mt-0 text-3xl md:text-4xl opacity-0 transition-opacity" class:duration-1000={isInview} class:opacity-100={isInview}>
        Our products
    </h2>
    <div class="lg:grid grid-cols-3 grid-flow-row gap-5 opacity-0 transition-opacity delay-200 [&>*:last-child]:border-none" class:duration-1000={isInview} class:opacity-100={isInview}>
        {#each products as item}
            <div class="mb-16 pb-10 lg:pb-0 border-b lg:border-none border-white">
                <ProductAvatar url={item.icon} name={item.name}>
                    <span>{item.description}</span>
                </ProductAvatar>
            </div>
        {/each}
    </div>
</div>