<script>
  import BlogCard from './BlogCard.svelte'
  import ItemContainer from './ItemContainer.svelte'
  import BlogBorder from './BlogBorder.svelte'
  import BlogDateContainer from './BlogDateContainer.svelte'
  import ExperienceCompanyDetailContainer from './ExperienceCompanyDetailContainer.svelte'
  import ExperienceBorder from './ExperienceBorder.svelte'
  import ExperiencePositionAndLocationContainer from './ExperiencePositionAndLocationContainer.svelte'
</script>

<div class="flex flex-col justify-center mt-10 mb-10">
  <ItemContainer>
    <BlogDateContainer>
      <p>Dec 2023</p>
    </BlogDateContainer>
    <BlogBorder />
    <div class="col-span-9 h-56">
      <BlogCard />
    </div>
  </ItemContainer>

  <ItemContainer>
    <ExperienceCompanyDetailContainer>
      <img src="./logo.png" alt="logo" class="w-8" />
      <p class="font-bold text-lg text-black">Duggup</p>
      <p class="text-[10px] text-gray-500">San Francisco Bay Area</p>
      <p class="text-[10px] text-gray-500">Joined</p>
      <p class="text-[10px] text-gray-500">Nov, 2023</p>
    </ExperienceCompanyDetailContainer>
    <ExperienceBorder />
    <ExperiencePositionAndLocationContainer>
      <h4 class="font-bold text-xl">Co-founder and CEO</h4>
      <p class="text-gray-500">Full-time, Remote</p>
    </ExperiencePositionAndLocationContainer>
  </ItemContainer>
</div>
