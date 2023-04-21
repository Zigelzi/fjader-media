<script lang="ts">
	export let href: string = '';
	export let isLink: boolean = true;
</script>

{#if isLink}
	<a
		{href}
		class="px-4 py-4 bg-stone-950 text-stone-50 border-2 border-stone-950 inline-block no-underline rounded-2xl hover:text-stone-950 hover:bg-white hover:border-2 hover:border-stone-950"
		><slot /></a
	>
{:else}
	<button
		on:click
		class="px-4 py-4 bg-stone-950 text-stone-50 border-2 border-stone-950 inline-block no-underline rounded-2xl hover:text-stone-950 hover:bg-white hover:border-2 hover:border-stone-950"
		><slot /></button
	>
{/if}
