<script lang="ts">
	export let href: string;
</script>

<a
	{href}
	class="px-4 py-4 bg-stone-950 text-stone-50 border-2 border-stone-950 inline-block no-underline rounded-2xl hover:text-stone-950 hover:bg-white hover:border-2 hover:border-stone-950"
	><slot /></a
>
