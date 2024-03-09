<script>
  import { ExternalLink } from 'svelte-radix'
  import Button from '../ui/button/button.svelte'
  import * as DropdownMenu from '$lib/components/ui/dropdown-menu'
</script>

<div class="flex flex-col gap-4">
  <div class="grid grid-cols-4">
    <div class="col-span-3">
      <p class="text-xs sm:text-sm md:text-base">
        Co-Founder and CEO at Duggup - Social network for people in tech.
        Ex-Amazon Head of Engineering. I write hot-takes on building a business,
        shipping delightful products and accelerating product and career growth.
      </p>
    </div>
    <div class="flex flex-col items-end col-span-1 gap-1">
      <img src="./logo.png" alt="logo" class="w-8" />
      <p class="font-bold text-sm sm:text-base md:text-lg">Duggup</p>
      <p class="text-[6px] sm:text-[10px] text-gray-500">Co-founder and CEO</p>
    </div>
  </div>
  <div class="flex justify-between items-center">
    <Button
      class="px-8 bg-white hover:bg-blue-600 hover:text-white text-black drop-shadow-[0_4px_0px_rgba(100,100,100,1)] hover:drop-shadow-[0_4px_0px_rgba(30,64,175,1)] "
    >
      Follow
    </Button>
    <div class="flex items-center gap-2">
      <a href="/">
        <div class="text-xs flex items-center gap-2">
          <p>My Website</p>
          <ExternalLink class="w-4" />
        </div>
      </a>
      <DropdownMenu.Root>
        <DropdownMenu.Trigger
          ><p class="text-lg font-bold mb-2">...</p></DropdownMenu.Trigger
        >
        <DropdownMenu.Content>
          <DropdownMenu.Group>
            <DropdownMenu.Item>View Followers</DropdownMenu.Item>
            <DropdownMenu.Item>Block User</DropdownMenu.Item>
            <DropdownMenu.Item>Mute User</DropdownMenu.Item>
          </DropdownMenu.Group>
        </DropdownMenu.Content>
      </DropdownMenu.Root>
    </div>
  </div>
</div>
