<script lang="ts">
	import Menu from '../../../components/app/Menu.svelte';
</script>

<div class="fixed top-0 left-1/2 flex h-20 w-full -translate-x-1/2 justify-between py-2 sm:w-96">
	<span class="flex w-full items-center justify-between text-5xl"
		><a href="../">&lt;</a> <span class="text-2xl">Add Credit Card / Debit Card</span>
	</span>
</div>
<div class="mx-8 my-auto flex w-full flex-col items-center space-y-6 py-20 sm:w-96">
	<label class="w-full">
		<span class="text-sm">Set Your Balance</span>
		<input type="number" class="input w-full" placeholder="0.00" />
	</label>
	<button class="btn w-full bg-bluest btn-lg btn-neutral">SET BALANCE</button>

	<div class="divider"></div>

	<label class="w-full">
		<span class="text-sm text-gray-500">Credit/Debit Card Number</span>
		<input type="text" class="input w-full" placeholder="**** **** **** ****" disabled/>
	</label>

	<label class="w-full">
		<span class="text-sm text-gray-500">Expiry Date</span>
		<input type="text" class="input w-full" placeholder="MM/YY" disabled/>
	</label>

	<label class="w-full">
		<span class="text-sm text-gray-500">CVV/CVC</span>
		<input type="text" class="input w-full" placeholder="***" disabled/>
	</label>

	<label class="w-full">
		<span class="text-sm text-gray-500">Name on Card</span>
		<input type="text" class="input w-full" placeholder="Name" disabled/>
	</label>

	<button class="btn w-full btn-lg" disabled>ADD CARD</button>

	<Menu />
</div>
