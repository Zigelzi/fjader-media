<script lang="ts">
	export let title: string;
	export let content: string;
</script>

<div class="p-4 max-w-sm">
	<slot />
	<h2 class="font-bold mt-4 mb-2 text-center">
		{title}
	</h2>

	<p>{content}</p>
</div>
