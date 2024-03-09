<script lang="ts">
  import { ChevronUp } from 'svelte-radix'
</script>

<div class="col-span-1">
  <div class="flex flex-col items-center w-full h-full">
    <div class="-ml-[8px] text-xl p-0 m-0">
      <ChevronUp class="text-gray-500" />
    </div>
    <div class="flex w-full h-full items-center justify-center">
      <div
        class="border-l-[3px] border-dotted w-0 h-full border-l-gray-400"
      ></div>
      <div
        class="bg-white w-4 h-4 rounded-full -ml-[8.75px] border-[6px] border-blue-500"
      ></div>
    </div>
  </div>
</div>
