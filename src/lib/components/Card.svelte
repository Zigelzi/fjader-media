<script lang="ts">
	export let title: string;
	export let content: string;
</script>

<div class="max-w-sm">
	<slot />
	<h2 class="font-bold text-xl lg:text-3xl mt-4 mb-2">
		{title}
	</h2>

	<p>{content}</p>
</div>
