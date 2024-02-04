<script lang="ts">
    import Landing from "$lib/components/Landing.svelte";
	import Members from "$lib/components/Members.svelte";
	import Products from "$lib/components/Products.svelte";
</script>

<main>
    <div class="w-full bg-primary-400 text-white p-10 h-[80dvh] flex flex-col lg:flex-row items-center">
        <div class="transition-all duration-300 lg:w-1/2 flex justify-center items-center space-x-7">
            <img class="bg-white rounded-full p-2" src="https://smakstlouis1sby.sch.id/wp-content/uploads/2019/08/Logo-512-01.png" alt="sinlui logo" width=128 height=128>
            <h4 class="text-6xl font-bold rounded-full">X<span class="text-teal-100">H</span></h4>
        </div>
        <h2 class="font-semibold flex justify-around lg:w-full text-4xl mt-20 lg:m-0">
            <span>
                A P5 Project<br/>
                made by class XH Group 4<br/>
                from St. Louis 1 Surabaya<br/>
            </span>
        </h2>
    </div>
    <div class="w-full bg-primary-200 text-primary-900 min-h-screen h-full flex items-center" id="about-us">
        <Landing/>
    </div>
    <div class="w-full bg-indigo-500 text-white min-h-screen h-full flex" id="our-members">
        <Products/>
    </div>
    <div class="w-full bg-primary-800 text-primary-200 min-h-screen h-full flex" id="our-members">
        <Members/>
    </div>
</main>

<style lang="scss">
</style>
