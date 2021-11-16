<script>
  import Clock from '../icons/Clock.svelte';
  let items = [
		{ id: 1, title: 'Rebasers' },
		{ id: 2, title: 'Liquidity Pools' },
		{ id: 3, title: 'Frog Nation' },
	];
</script>

<div class="container mx-auto px-4 xl:px-0">
  <nav class="text-white xl:flex items-center w-full justify-between">

    <div class="font-medium text-3xl ml-2 w-1/6">
      defair
    </div>

    <ul class="flex items-center no-underline w-5/6">
      {#each items as item (item.id)}
        <li>
          <a href="#" class="hover:text-green-100 text-m text-gray-50 hover:no-underline">
            <div class="flex items-center  
                        border-transparent border-b 
                        xl:ml-6 2xl:ml-11">
              <Clock class="h-5 w-5 mx-2" />
              <p>
                {item.title}
              </p>
            </div>
          </a>
        </li>
      {/each}
    </ul>

  </nav>
</div>