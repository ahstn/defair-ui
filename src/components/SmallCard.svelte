<script lang="ts">
    export let title : string
    export let desc : string
    export let amount : string
    export let accent : string
    export let background : string = "white"
</script>

<div class="hover:shadow-lg p-4 bg-{background} rounded-lg border border-gray-200">
    <p class="text-base font-medium leading-none text-gray-800">{title}</p>
    <div class="flex items-center justify-between mt-1">
        <p class="text-xs leading-3 text-gray-600 mr-4">{desc}</p>
        <p class="text-base font-semibold leading-none text-{accent}-700">${amount}</p>
    </div>
    <div class="w-full rounded-full mt-3.5 h-1.5 bg-{accent}-50">
        <div class="w-1/4 h-1.5 bg-{accent}-500 rounded-full"></div>
    </div>
</div>