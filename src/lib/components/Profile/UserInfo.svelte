<script lang="ts">
  export let imgUrl: string
  export let name: string
</script>

<div class="flex flex-row items-center md:flex-col">
  <img
    src={imgUrl}
    alt="profile-pic"
    class="w-28 h-28 rounded-full border-[3px] border-gray-300 object-cover"
  />
  <p class="w-28 text-center text-xl text-gray-500 font-semibold mt-2">
    {name}
  </p>
</div>
