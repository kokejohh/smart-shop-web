<script lang="ts">
	import logo from '$lib/images/logo.png';
</script>

<div class="mx-8 my-auto flex w-full flex-col items-center space-y-6 sm:w-96">
	<img src={logo} alt="Logo" class="w-1/2" />
	<span class="self-start text-4xl font-bold">Login</span>
	<label class="input w-full">
		<svg width="32" height="37" viewBox="0 0 32 37" fill="none" xmlns="http://www.w3.org/2000/svg">
			<path
				fill-rule="evenodd"
				clip-rule="evenodd"
				d="M8.88889 8.22222C8.88889 6.04155 9.63809 3.9502 10.9717 2.40823C12.3053 0.866267 14.114 0 16 0C17.886 0 19.6947 0.866267 21.0283 2.40823C22.3619 3.9502 23.1111 6.04155 23.1111 8.22222C23.1111 10.4029 22.3619 12.4942 21.0283 14.0362C19.6947 15.5782 17.886 16.4444 16 16.4444C14.114 16.4444 12.3053 15.5782 10.9717 14.0362C9.63809 12.4942 8.88889 10.4029 8.88889 8.22222ZM8.88889 20.5556C6.53141 20.5556 4.27049 21.6384 2.6035 23.5658C0.936505 25.4933 0 28.1075 0 30.8333C0 32.4688 0.561903 34.0374 1.5621 35.1938C2.56229 36.3503 3.91885 37 5.33333 37H26.6667C28.0812 37 29.4377 36.3503 30.4379 35.1938C31.4381 34.0374 32 32.4688 32 30.8333C32 28.1075 31.0635 25.4933 29.3965 23.5658C27.7295 21.6384 25.4686 20.5556 23.1111 20.5556H8.88889Z"
				fill="#030F59"
			/>
		</svg>

		<input type="username" required placeholder="Username" />
	</label>

	<label class="input w-full">
		<svg width="32" height="39" viewBox="0 0 34 39" fill="none" xmlns="http://www.w3.org/2000/svg">
			<path
				d="M29.75 13H27.625V9.28571C27.625 4.16 22.865 0 17 0C11.135 0 6.375 4.16 6.375 9.28571V13H4.25C1.9125 13 0 14.6714 0 16.7143V35.2857C0 37.3286 1.9125 39 4.25 39H29.75C32.0875 39 34 37.3286 34 35.2857V16.7143C34 14.6714 32.0875 13 29.75 13ZM17 29.7143C14.6625 29.7143 12.75 28.0429 12.75 26C12.75 23.9571 14.6625 22.2857 17 22.2857C19.3375 22.2857 21.25 23.9571 21.25 26C21.25 28.0429 19.3375 29.7143 17 29.7143ZM23.5875 13H10.4125V9.28571C10.4125 6.11 13.3663 3.52857 17 3.52857C20.6338 3.52857 23.5875 6.11 23.5875 9.28571V13Z"
				fill="#030F59"
			/>
		</svg>
		<input type="password" required placeholder="Password" />
	</label>

	<div class="flex w-full justify-between">
		<label>
			<input type="checkbox" name="" id="" />
			Remember me
		</label>
		<a href="./">Forgot password?</a>
	</div>
	<button class="btn w-full bg-bluest btn-lg btn-neutral">LOGIN</button>
	<div>
		Don't have an account ? <a href="./register" class="text-bluest underline">Sign Up</a>
	</div>
</div>
