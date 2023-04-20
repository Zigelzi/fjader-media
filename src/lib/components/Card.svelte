<script lang="ts">
	export let title: String;
	export let content: String;
</script>

<div class="border-2 border-gray-500 p-4 max-w-sm">
	<h2 class="font-bold mb-2 text-center">
		{title}
	</h2>

	<p>{content}</p>
</div>
