<script lang="ts">
    let { children } = $props();

	import { page } from '$app/state';
</script>


<div class="drawer-open drawer">
	<input id="my-drawer-4" type="checkbox" class="drawer-toggle" />
	<div class="drawer-content bg-base-200">
		<div class="px-16 pt-32 pb-8">
            {@render children()}
		</div>
	</div>

	<div class="drawer-side is-drawer-close:overflow-visible">
		<label for="my-drawer-4" aria-label="close sidebar" class="drawer-overlay"></label>
		<div
			class="flex min-h-full flex-col items-start bg-bluest pt-24 is-drawer-close:w-28 is-drawer-open:w-44"
		>
			<!-- Sidebar content here -->
			<ul class="menu flex w-full grow items-center justify-around">
				<!-- List item -->
				<li>
					<a
                        href="/admin/dashboard"
						class="is-drawer-close:tooltip is-drawer-close:tooltip-right"
						data-tip="Dashboard"
					>
						<svg
							class="h-8 w-8"
							width="44"
							height="40"
							viewBox="0 0 44 40"
							fill="none"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M42 20H34L28 38L16 2L10 20H2"
								stroke={page.url.pathname === '/admin/dashboard' ? '#F3F3F3' : '#B3B3B3'}
								stroke-width="4"
								stroke-linecap="round"
								stroke-linejoin="round"
							/>
						</svg>
						<span class="text-white is-drawer-close:hidden">Dashboard</span>
					</a>
				</li>

				<li>
					<a
                        href="/admin/camera"
                        class="is-drawer-close:tooltip is-drawer-close:tooltip-right"
                        data-tip="Cameras">
						<svg
							class="h-8 w-8"
							width="48"
							height="40"
							viewBox="0 0 48 40"
							fill="none"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M46 34C46 35.0609 45.5786 36.0783 44.8284 36.8284C44.0783 37.5786 43.0609 38 42 38H6C4.93913 38 3.92172 37.5786 3.17157 36.8284C2.42143 36.0783 2 35.0609 2 34V12C2 10.9391 2.42143 9.92172 3.17157 9.17157C3.92172 8.42143 4.93913 8 6 8H14L18 2H30L34 8H42C43.0609 8 44.0783 8.42143 44.8284 9.17157C45.5786 9.92172 46 10.9391 46 12V34Z"
								stroke={page.url.pathname === '/admin/camera' ? '#F3F3F3' : '#B3B3B3'}
								stroke-width="4"
								stroke-linecap="round"
								stroke-linejoin="round"
							/>
							<path
								d="M24 30C28.4183 30 32 26.4183 32 22C32 17.5817 28.4183 14 24 14C19.5817 14 16 17.5817 16 22C16 26.4183 19.5817 30 24 30Z"
								stroke="#B3B3B3"
								stroke-width="4"
								stroke-linecap="round"
								stroke-linejoin="round"
							/>
						</svg>
						<span class="text-white is-drawer-close:hidden">Cameras</span>
					</a>
				</li>
				<li>
					<a
                        href="/admin/member"
                        class="is-drawer-close:tooltip is-drawer-close:tooltip-right" data-tip="Members">
						<svg
							class="h-8 w-8"
							width="40"
							height="40"
							viewBox="0 0 40 40"
							fill="none"
							xmlns="http://www.w3.org/2000/svg"
						>
							<g clip-path="url(#clip0_4_39)">
								<path
									d="M28.3333 35V31.6667C28.3333 29.8986 27.631 28.2029 26.3807 26.9526C25.1305 25.7024 23.4348 25 21.6667 25H8.33333C6.56522 25 4.86953 25.7024 3.61929 26.9526C2.36905 28.2029 1.66667 29.8986 1.66667 31.6667V35M38.3333 35V31.6667C38.3322 30.1895 37.8406 28.7546 36.9356 27.5872C36.0306 26.4198 34.7635 25.5859 33.3333 25.2167M26.6667 5.21667C28.1007 5.58384 29.3717 6.41783 30.2794 7.58718C31.1871 8.75653 31.6797 10.1947 31.6797 11.675C31.6797 13.1553 31.1871 14.5935 30.2794 15.7628C29.3717 16.9322 28.1007 17.7662 26.6667 18.1333M21.6667 11.6667C21.6667 15.3486 18.6819 18.3333 15 18.3333C11.3181 18.3333 8.33333 15.3486 8.33333 11.6667C8.33333 7.98477 11.3181 5 15 5C18.6819 5 21.6667 7.98477 21.6667 11.6667Z"
									stroke={page.url.pathname === '/admin/member' ? '#F3F3F3' : '#B3B3B3'}
									stroke-width="3.5"
									stroke-linecap="round"
									stroke-linejoin="round"
								/>
							</g>
							<defs>
								<clipPath id="clip0_4_39">
									<rect width="40" height="40" fill="white" />
								</clipPath>
							</defs>
						</svg>

						<span class="text-white is-drawer-close:hidden">Members</span>
					</a>
				</li>
				<li>
					<a
                        href="/admin/warehouse"
						class="is-drawer-close:tooltip is-drawer-close:tooltip-right"
						data-tip="Warehouse"
					>
						<svg
							class="h-8 w-8"
							width="40"
							height="45"
							viewBox="0 0 40 45"
							fill="none"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M29 16.7959L11 6.4159M2.54 11.9159L20 22.0159L37.46 11.9159M20 42.1559V21.9959M38 29.9959V13.9959C37.9993 13.2944 37.8141 12.6055 37.4631 11.9982C37.112 11.3909 36.6075 10.8866 36 10.5359L22 2.5359C21.3919 2.18482 20.7021 2 20 2C19.2979 2 18.6081 2.18482 18 2.5359L4 10.5359C3.39253 10.8866 2.88796 11.3909 2.53692 11.9982C2.18589 12.6055 2.00072 13.2944 2 13.9959V29.9959C2.00072 30.6974 2.18589 31.3863 2.53692 31.9936C2.88796 32.6009 3.39253 33.1052 4 33.4559L18 41.4559C18.6081 41.807 19.2979 41.9918 20 41.9918C20.7021 41.9918 21.3919 41.807 22 41.4559L36 33.4559C36.6075 33.1052 37.112 32.6009 37.4631 31.9936C37.8141 31.3863 37.9993 30.6974 38 29.9959Z"
								stroke={page.url.pathname === '/admin/warehouse' ? '#F3F3F3' : '#B3B3B3'}
								stroke-width="4"
								stroke-linecap="round"
								stroke-linejoin="round"
							/>
						</svg>

						<span class="text-white is-drawer-close:hidden">Warehouse</span>
					</a>
				</li>
				<li>
					<a
                        href="/admin/setting"
						class="is-drawer-close:tooltip is-drawer-close:tooltip-right"
						data-tip="System Settings"
					>
						<svg
							class="h-8 w-8"
							width="44"
							height="39"
							viewBox="0 0 44 39"
							fill="none"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M10 9H10.02M10 30H10.02M6 2H38C40.2091 2 42 3.567 42 5.5V12.5C42 14.433 40.2091 16 38 16H6C3.79086 16 2 14.433 2 12.5V5.5C2 3.567 3.79086 2 6 2ZM6 23H38C40.2091 23 42 24.567 42 26.5V33.5C42 35.433 40.2091 37 38 37H6C3.79086 37 2 35.433 2 33.5V26.5C2 24.567 3.79086 23 6 23Z"
								stroke={page.url.pathname === '/admin/setting' ? '#F3F3F3' : '#B3B3B3'}
								stroke-width="4"
								stroke-linecap="round"
								stroke-linejoin="round"
							/>
						</svg>

						<span class="text-white is-drawer-close:hidden">Settings</span>
					</a>
				</li>
			</ul>
		</div>
	</div>
</div>