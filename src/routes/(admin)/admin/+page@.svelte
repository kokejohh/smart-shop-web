<div class="flex flex-col items-center justify-center h-[calc(100vh-16rem)]">
    Admin Page
	<form class="fieldset w-xs rounded-box border border-base-300 bg-base-200 p-4">
		<fieldset class="fieldset">
			<label for="username" class="label">Username</label>
			<input id="username" type="text" class="validator input" placeholder="Username" required />
			<p class="validator-hint hidden">Required</p>
		</fieldset>

		<label class="fieldset">
			<span class="label">Password</span>
			<input type="password" class="validator input" placeholder="Password" required />
			<span class="validator-hint hidden">Required</span>
		</label>

		<button class="btn mt-4 btn-neutral" type="submit">Login</button>
	</form>
</div>
