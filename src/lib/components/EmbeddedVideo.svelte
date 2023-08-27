<script lang="ts">
	export let height = '100%';
	export let width = '100%';
	export let videoId = '';

	let player;
	let isPlaceHolderHidden = false;

	const id = crypto.randomUUID();

	function loadYouTubeplayer() {
		isPlaceHolderHidden = true;
		player = new YT.Player(id, {
			height,
			width,
			videoId,
			playerlets: {
				playsinline: 1
			},
			events: {
				onReady,
				onStateChange
			}
		});
	}

	function onReady(event: Event) {
		if (event.target) {
			event.target.playVideo();
		}
	}

	function onStateChange(event: Event) {}
</script>

<svelte:head>
	<script src="https://www.youtube.com/iframe_api"></script>
</svelte:head>

<div class="youtube-container relative">
	<div
		id="video-placeholder"
		class:hidden={isPlaceHolderHidden}
		class="aspect-video"
		on:click={loadYouTubeplayer}
		on:keyup={loadYouTubeplayer}
	>
		<img src="https://img.youtube.com/vi/{videoId}/mqdefault.jpg" class="w-full h-full" alt="" />
		<button class="yt-play-button" title="Play embedded video" />
	</div>
	<div class:hidden={!isPlaceHolderHidden}>
		<div {id} class="aspect-video" />
	</div>
</div>

<style>
	#video-placeholder > .yt-play-button {
		display: block;
		width: 68px;
		height: 48px;
		position: absolute;
		cursor: pointer;
		transform: translate3d(-50%, -50%, 0);
		top: 50%;
		left: 50%;
		z-index: 1;
		background-color: transparent;
		/* YT's actual play button svg */
		background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 68 48"><path d="M66.52 7.74c-.78-2.93-2.49-5.41-5.42-6.19C55.79.13 34 0 34 0S12.21.13 6.9 1.55c-2.93.78-4.63 3.26-5.42 6.19C.06 13.05 0 24 0 24s.06 10.95 1.48 16.26c.78 2.93 2.49 5.41 5.42 6.19C12.21 47.87 34 48 34 48s21.79-.13 27.1-1.55c2.93-.78 4.64-3.26 5.42-6.19C67.94 34.95 68 24 68 24s-.06-10.95-1.48-16.26z" fill="red"/><path d="M45 24 27 14v20" fill="white"/></svg>');
		filter: grayscale(100%);
		transition: filter 0.1s cubic-bezier(0, 0, 0.2, 1);
		border: none;
	}

	#video-placeholder:hover > .yt-play-button,
	#video-placeholder:focus > .yt-play-button {
		filter: none;
	}
</style>
