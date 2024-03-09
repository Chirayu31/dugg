<script lang="ts">
  import BlogCard from './BlogCard.svelte'
  import ItemContainer from './ItemContainer.svelte'
  import BlogBorder from './BlogBorder.svelte'
  import BlogDateContainer from './BlogDateContainer.svelte'
  import ExperienceCompanyDetailContainer from './ExperienceCompanyDetailContainer.svelte'
  import ExperienceBorder from './ExperienceBorder.svelte'
  import ExperiencePositionAndLocationContainer from './ExperiencePositionAndLocationContainer.svelte'
  import * as Carousel from '$lib/components/ui/carousel/'

  export let timelineData: any
</script>

<div class="flex flex-col justify-center ml-5 md:ml-16 lg:ml-32 mt-10 mb-10">
  {#each timelineData as item}
    {#if item.type === 'blogs'}
      <ItemContainer>
        <BlogDateContainer>
          <p class="text-xs sm:text-base">{item.date}</p>
        </BlogDateContainer>
        <BlogBorder />
        <div class="col-span-9 h-56">
          <Carousel.Root>
            <Carousel.Content>
              {#each item.posts as post}
                <Carousel.Item class="md:basis-1/2"
                  ><BlogCard img={post.img} title={post.title} /></Carousel.Item
                >
              {/each}
            </Carousel.Content>
          </Carousel.Root>
        </div>
      </ItemContainer>
    {:else if item.type === 'experience'}
      <ItemContainer>
        <ExperienceCompanyDetailContainer>
          <img src={item.logo} alt="logo" class="w-8" />
          <p class="font-bold text-sm sm:text-lg text-black">{item.company}</p>
          <p class="text-[8px] sm:text-[10px] text-gray-500">{item.location}</p>
          <p class="text-[8px] sm:text-[10px] text-gray-500">Joined</p>
          <p class="text-[8px] sm:text-[10px] text-gray-500">{item.date}</p>
        </ExperienceCompanyDetailContainer>
        <ExperienceBorder />
        <ExperiencePositionAndLocationContainer>
          <h4 class="font-bold text-xl">{item.position}</h4>
          <p class="text-gray-500">{item.status}</p>
        </ExperiencePositionAndLocationContainer>
      </ItemContainer>
    {/if}
  {/each}
</div>
