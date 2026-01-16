<script lang="ts">
	import Menu from '../../../components/app/Menu.svelte';
	import CardHistory from '../../../components/app/CardHistory.svelte';
</script>

<div class="fixed top-0 left-1/2 flex h-20 w-full -translate-x-1/2 justify-between p-2 sm:w-96">
	<span class="relative flex w-full items-center justify-center text-5xl text-gray-500">
		<a href="../" aria-label="back" class="absolute left-0">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				stroke-width="2.5"
				stroke="currentColor"
				class="h-6 w-6"
			>
				<path stroke-linecap="round" stroke-linejoin="round" d="M15.75 19.5L8.25 12l7.5-7.5" />
			</svg>
		</a>
		<span class="text-2xl">Report a Problem</span>
	</span>
</div>

<div class="mx-2 flex w-full flex-col items-center space-y-2 py-20 sm:mx-8 sm:w-96">
	<span class="self-start">
		Problems & Issues
	</span>
	<div class="p-4 border w-full shadow-sm rounded-xl bg-gray-100">
		Missing or Incorrect Items
	</div>
	<div class="p-4 border w-full shadow-sm rounded-xl bg-bluest text-white">
		App Freezing or Crashing
	</div>
	<div class="p-4 border w-full shadow-sm rounded-xl bg-gray-100">
		Other (Please specify)
		<input type="text" name="" id="" class="input">
	</div>
	<button class="btn w-full bg-bluest btn-lg btn-neutral">REPORT</button>
</div>

<Menu />
