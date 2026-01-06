<script>
	import Camera from '../../../../components/admin/Camera.svelte';

	const urlCam = [
		'https://camerai1.iticfoundation.org/hls/pty74.m3u8', //ATC4-18 แยกสุขุมวิท-พัทยาเหนือ
		'https://camera1.iticfoundation.org/hls/10.8.0.22_8555.m3u8', // (กรุงเทพมหานคร) รพ.บางปะกอก
		'https://camera1.iticfoundation.org/hls/10.8.0.21_8001.m3u8', // บางนาตราด
		'https://camera1.iticfoundation.org/hls/10.8.0.21_8002.m3u8' // บางนาตราด
	];
	let currentCam = urlCam[0];
</script>

<div class="flex justify-between">
	<h1 class="text-2xl font-bold">AI VISION ENGINE</h1>

	<div>DB CONNECTED</div>
	<div>
		<div class="badge badge-xs badge-error"></div>
		REC
	</div>
	<div>14:45:32 15 DEC 2025</div>
	<div>Active Cameras (8/8)</div>
</div>

<div class="flex justify-center">
	<div class="flex h-screen w-1/3 flex-col space-y-8 overflow-y-scroll p-8">
		<!-- {#each urlCam as url}
			<button
				class="relative aspect-video w-full shrink-0 overflow-hidden rounded-xl bg-black shadow-md"
				onclick={() => (currentCam = url)}
			>
				<div class="absolute inset-0 z-0 flex items-center justify-center">
					<span class="loading loading-sm loading-spinner text-primary"></span>
					<span class="ml-2 text-white">Loading...</span>
				</div>
				<div class="relative z-10 h-full w-full">
					<Camera src={url} />
				</div>
			</button>
		{/each} -->
	</div>
	<div class="flex w-2/3 flex-col items-center space-y-8 p-8">
		<div
			class="relative aspect-video w-full shrink-0 overflow-hidden rounded-xl bg-black shadow-md"
		>
			<div class="absolute inset-0 z-0 flex items-center justify-center">
				<span class="loading loading-lg loading-spinner text-primary"></span>
				<span class="ml-2 text-white">Loading...</span>
			</div>
			<div class="relative z-10 h-full w-full">
				<img src="http://127.0.0.1:8000/" style="width: 100%; border-radius: 10px;">
				<img src="http://127.0.0.1:8000/1" style="width: 100%; border-radius: 10px;">
			<!-- {#key currentCam}
				<Camera src={currentCam} />
			{/key} -->
			</div>
		</div>
		<div class="h-64 w-full shrink-0 bg-base-300"></div>
	</div>
</div>
