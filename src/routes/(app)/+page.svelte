<script lang="ts">
	import howto from '$lib/images/howto.png';
    import wallet from '$lib/images/wallet.png';

    import Header from '../../components/app/Header.svelte';
    import Menu from '../../components/app/Menu.svelte';
</script>

<div class="sm:mx-8 flex w-full flex-col justify-betwen py-20 sm:w-96">
    <Header />
    <div class="border-l-20 border-l-bluest border-[#999999] border-6 my-4 mx-2 rounded-xl flex flex-col">
        <div class="flex items-center">
        <img src={wallet} alt="" srcset="" class="h-30">
            <div class="text-xl">
                Balance:
                <br>
                ฿100.00
            </div>
        </div>
        <a href="./card" class="btn btn-sm">
            Connected the Credit Card
        </a>
    </div>
	<img src={howto} alt="" srcset="" />
    <Menu />
</div>
