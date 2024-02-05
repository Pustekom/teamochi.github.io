<script lang="ts">
    export let url: string;
    export let name: string;
</script>
<div class="flex flex-col items-center">
    <img width=128px height=128px class="bg-white p-0.5 min-w-64 min-h-64" src={url} alt="{name} avatar">
    <span class="font-bold text-xl p-2">{name}</span>
    <div class="flex items-center">
        <slot />
    </div>

</div>