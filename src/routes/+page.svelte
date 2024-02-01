<script lang="ts">
    import Landing from "$lib/components/Landing.svelte";
</script>

<svelte:head>
    <title>Teamochi</title>
</svelte:head>

<main>
    <div class="w-full bg-primary-400 text-white p-10 h-screen flex flex-col md:flex-row items-center">
        <div class="transition-all duration-300 px-20 md:px-36 flex flex-col md:flex-row justify-center items-center md:space-x-7">
            <img class="bg-white rounded-full p-2" src="https://smakstlouis1sby.sch.id/wp-content/uploads/2019/08/Logo-512-01.png" alt="sinlui logo" width=128 height=128>
            <h4 class="text-6xl font-bold rounded-full">X<span class="text-teal-300">H</span></h4>
        </div>
        <h2 class="font-semibold text-4xl mt-20 md:m-0">
            A P5 Project<br/>
            made by class XH Group 4<br/>
            from St. Louis 1 Surabaya<br/>
        </h2>
    </div>
    <div class="w-full bg-primary-200 text-primary-900 p-10 h-screen flex items-center">
        <Landing/>
    </div>
</main>

<style lang="scss">
</style>
