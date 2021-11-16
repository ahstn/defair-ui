<script lang="ts">
	import Navigation from './components/Navigation.svelte'
	import SmallCard from './components/SmallCard.svelte'
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
							<div class="flex items-center mt-4 sm:mt-0 w-1/3">
								<div class="flex items-center pl-3 w-full bg-white border rounded-md border-gray-200">
									<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
										<path d="M8.33333 13.1667C11.555 13.1667 14.1667 10.555 14.1667 7.33333C14.1667 4.11167 11.555 1.5 8.33333 1.5C5.11167 1.5 2.5 4.11167 2.5 7.33333C2.5 10.555 5.11167 13.1667 8.33333 13.1667Z" stroke="#9CA3AF" stroke-width="1.25" stroke-linecap="round" stroke-linejoin="round" />
										<path d="M17.5 17.5L12.5 12.5" stroke="#9CA3AF" stroke-width="1.25" stroke-linecap="round" stroke-linejoin="round" />
									</svg>
									<input type="text" class="py-3 pl-1 border-none focus:outline-none text-sm rounded-md text-gray-600 placeholder-gray-400" placeholder="Search" />
								</div>
							</div>
                        </div>
                    </div>
					<div class="bg-white shadow px-4 md:px-10 pt-4 md:pt-7 pb-5 overflow-y-auto flex flex-row flex-wrap gap-4">
						<SmallCard title="Wallet" desc="Balance(s) available of token(s)" amount="1875" accent="indigo" />
						<SmallCard title="Lending" desc="Balance being provided as collateral" amount="2100" accent="blue" />
						<SmallCard title="Staking" desc="Balance(s) provided in Liquidity Pools" amount="625" accent="green" />
						<SmallCard title="Debt" desc="Borrowed Balance" amount="340" accent="pink" background="pink-100" />
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