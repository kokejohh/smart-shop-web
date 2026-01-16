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
		<span class="text-2xl">History</span>
	</span>
</div>
<div class="mx-2 flex w-full flex-col items-center space-y-6 py-20 sm:mx-8 sm:w-96">
	<!-- name of each tab group should be unique -->
	<div class="tabs w-full">
		<input
			type="radio"
			name="my_tabs_6"
			class="tab w-20 flex-1 rounded-xl shadow-sm checked:bg-bluest checked:text-white"
			aria-label="All"
		/>
		<div class="tab-content bg-base-100">
			<CardHistory />
		</div>

		<input
			type="radio"
			name="my_tabs_6"
			class="tab w-20 flex-1 rounded-xl shadow-sm checked:bg-bluest checked:text-white"
			aria-label="Today"
			checked={true}
		/>
		<div class="tab-content bg-base-100">
			<CardHistory />
			<CardHistory />
		</div>

		<input
			type="radio"
			name="my_tabs_6"
			class="tab w-20 flex-1 rounded-xl shadow-sm checked:bg-bluest checked:text-white"
			aria-label="7 Days"
		/>
		<div class="tab-content bg-base-100">
			<CardHistory />
			<CardHistory />
			<CardHistory />
			<CardHistory />
			<CardHistory />
			<CardHistory />
			<CardHistory />
			<CardHistory />
			<CardHistory />
		</div>
	</div>
	<Menu />
</div>
