<script>
  import {
    ActivityLog,
    Home,
    ViewVertical,
    Plus,
    ChevronDown,
  } from 'svelte-radix'
  import { Button } from './ui/button'
  import * as DropdownMenu from '$lib/components/ui/dropdown-menu'
</script>

<nav
  class="flex mx-2 sm:mx-5 md:mx-10 lg:mx-24 justify-between py-4 border-b-[1px] border-gray-300 text-gray-600"
>
  <div class="flex items-center gap-3">
    <img src="./logo.png" alt="logo" class="w-8 h-8" />
    <p class="font-bold text-lg text-black hidden sm:block">duggup</p>
  </div>

  <div class="flex gap-3 sm:gap-5 md:gap-3 lg:gap-10 items-center">
    <p class="flex items-center text-gray-600 hover:text-black">
      <Home class="w-4 h-4 mr-2" />
      <span class="hidden md:block">Home</span>
    </p>

    <p class="flex items-center text-gray-600 hover:text-black">
      <ActivityLog class="w-4 h-4 mr-2" />
      <span class="hidden md:block">Explore</span>
    </p>
    <p class="flex items-center text-gray-600 hover:text-black">
      <ViewVertical class="w-4 h-4 mr-2" />
      <span class="hidden md:block">Learn</span>
    </p>
    <Button
      variant="secondary"
      class="bg-white border-[1px] drop-shadow-[0_4px_0px_rgba(77,77,77,1)] hover:bg-white text-gray-600 hover:text-black"
    >
      <Plus class="w-4 h-4 mr-2" />
      <p class="hidden md:block">Post</p>
    </Button>

    <DropdownMenu.Root>
      <DropdownMenu.Trigger>
        <div class="flex gap-4 items-center font-semibold">
          <img
            src="https://s3-alpha-sig.figma.com/img/8ed8/92f8/c135d62b39e8cc0f1e2dfce61ea32106?Expires=1710720000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=RKaA5Kcb70gvKNoo9YauvfaxT04LsCUqLYTn7qHkiOuYPcaQTuovvHkj2sU8DgkClYN56W8Q50~Zpb7bEBtkEeZS-xx4-8z7f80~95goddInZDQ7bkdQtIuACuNYotlDGl4C~VVZhiNM7oM5Y-NlPzosE1D8jHPtdoFaDiHF8g4uhikuaIPgtEc4rdtKes7nteMWYJbnDLW1ZR8~zew4527Stene~jnzcLOuI7Iko1-IXmuujNxMPlPEq07C~mOouek9TPIuvOdFyFTrGTxXiLT6eK6c1z~Rcbhwc4c1EZxyEWWXSSl5~O3msyeLdc-A0f63nEUsyNq67Ug2v7q-DQ__"
            alt="profile-pic"
            class="w-10 h-10 rounded-full border-[3px] border-gray-300 object-cover"
          />
          <p class="hidden md:block">Krishna Kiran</p>
          <ChevronDown />
        </div>
      </DropdownMenu.Trigger>
      <DropdownMenu.Content>
        <DropdownMenu.Group>
          <DropdownMenu.Label>My Account</DropdownMenu.Label>
          <DropdownMenu.Separator />
          <DropdownMenu.Item>Profile</DropdownMenu.Item>
          <DropdownMenu.Item>Courses</DropdownMenu.Item>
          <DropdownMenu.Item>Logout</DropdownMenu.Item>
        </DropdownMenu.Group>
      </DropdownMenu.Content>
    </DropdownMenu.Root>
  </div>
</nav>
