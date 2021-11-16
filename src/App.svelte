<script lang="ts">
	import Navigation from './components/Navigation.svelte';
	export let name: string;
</script>

<body class="bg-gray-50">
	<div class="h-40 pt-6 md:pt-8 xl:pt-12 bg-green-600 bg-header-dashboard">
		<Navigation />
	</div>
	
	<div class="px-4 xl:px-0">
        <div class="mx-auto container">
            <div class="">
                <div class="width-full -mt-8 xl:-mt-16">
                    <div class="px-4 md:px-10 py-4 md:py-7 bg-gray-100 rounded-tl-lg rounded-tr-lg">
                        <div class="sm:flex items-center justify-between">
                            <p class="text-base sm:text-lg md:text-xl lg:text-2xl font-bold leading-normal text-gray-800">Address Overview</p>
							<div class="flex items-center mt-4 sm:mt-0">
								<div class="flex items-center pl-3 bg-white border rounded-md border-gray-200">
									<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
										<path d="M8.33333 13.1667C11.555 13.1667 14.1667 10.555 14.1667 7.33333C14.1667 4.11167 11.555 1.5 8.33333 1.5C5.11167 1.5 2.5 4.11167 2.5 7.33333C2.5 10.555 5.11167 13.1667 8.33333 13.1667Z" stroke="#9CA3AF" stroke-width="1.25" stroke-linecap="round" stroke-linejoin="round" />
										<path d="M17.5 17.5L12.5 12.5" stroke="#9CA3AF" stroke-width="1.25" stroke-linecap="round" stroke-linejoin="round" />
									</svg>
									<input type="text" class="py-3 pl-1 w-full border-none focus:outline-none text-sm rounded-md text-gray-600 placeholder-gray-400" placeholder="Search" />
								</div>
								<div
									class="ml-4 py-3 px-4 flex items-center text-sm font-medium leading-none text-gray-600 bg-gray-200 hover:bg-gray-300 cursor-pointer rounded">
									<p class="text-gray-600 font-medium">Networks:</p>
									<select class="focus:outline-none bg-transparent ml-1 ">
										<option class="text-sm text-gray-600 font-medium ">All</option>
										<option class="text-sm text-gray-600 font-medium ">Avalance</option>
										<option class="text-sm text-gray-600 font-medium ">Ethereum</option>
										<option class="text-sm text-gray-600 font-medium ">Fantom</option>
									</select>
								</div>
							</div>
                        </div>
                    </div>
                    <div class="bg-white shadow px-4 md:px-10 pt-4 md:pt-7 pb-5 overflow-y-auto">
						<div class="pt-3 pb-4 px-3 bg-white shadow rounded">
							<p class="text-base font-medium leading-none text-gray-800">Wallet</p>
							<div class="flex items-center justify-between mt-1">
								<p class="text-xs leading-3 text-gray-600 ">Current Balance(s) Available</p>
								<p class="text-base font-semibold leading-none text-indigo-700">$1,323</p>
							</div>
							<div class="w-full rounded-full mt-3.5 h-1.5 bg-indigo-50">
								<div class="w-1/4 h-1.5 bg-indigo-500 rounded-full"></div>
							</div>
						</div>
						<div class="pt-3 pb-4 px-3 bg-white shadow rounded mt-3">
							<p class="text-base font-medium leading-none text-gray-800">Lending</p>
							<div class="flex items-center justify-between mt-1">
								<p class="text-xs leading-3 text-gray-600 ">Current Balance(s) Being Lent</p>
								<p class="text-base font-semibold leading-none text-blue-500">$1,323</p>
							</div>
							<div class="w-full rounded-full mt-3.5 h-1.5 bg-blue-50">
								<div class="w-2/3 h-1.5 bg-blue-500 rounded-full"></div>
							</div>
						</div>
						<div class="pt-3 pb-4 px-3 bg-white shadow rounded mt-3">
							<p class="text-base font-medium leading-none text-gray-800">Staking</p>
							<div class="flex items-center justify-between mt-1">
								<p class="text-xs leading-3 text-gray-600 ">Current Balance(s) Being Staked in Liquidity Pools</p>
								<p class="text-base font-semibold leading-none text-green">$1,323</p>
							</div>
							<div class="w-full rounded-full mt-3.5 h-1.5 bg-green-50">
								<div class="w-1/2 h-1.5 bg-green rounded-full"></div>
							</div>
						</div>
						<div class="pt-3 pb-4 px-3 bg-white shadow rounded mt-3">
							<p class="text-base font-medium leading-none text-gray-800">Debt</p>
							<div class="flex items-center justify-between mt-1">
								<p class="text-xs leading-3 text-gray-600 ">Current Balance(s) Being Borrowed</p>
								<p class="text-base font-semibold leading-none text-pink-500">$1,323</p>
							</div>
							<div class="w-full rounded-full mt-3.5 h-1.5 bg-pink-50">
								<div class="w-1/3 h-1.5 bg-pink-500 rounded-full"></div>
							</div>
						</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>

<style global lang="postcss">
	@tailwind base;
  	@tailwind components;
  	@tailwind utilities;

	body {
		padding: 0;
	}
	main {
		text-align: center;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>