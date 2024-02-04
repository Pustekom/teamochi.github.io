<script lang="ts">
    export let url: string;
    export let name: string;
</script>
<div class="flex flex-col items-center">
    <img class="rounded-full bg-white p-0.5 min-w-max min-h-20" src={url} alt="{name} avatar">
    <span class="font-semibold p-2">{name}</span>
    <div class="flex items-center">
        <slot />
    </div>
</div>