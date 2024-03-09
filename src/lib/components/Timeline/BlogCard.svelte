<script lang="ts">
  import * as Card from '$lib/components/ui/card'

  export let img: string
  export let title: string
</script>

<Card.Root class="w-[200px] sm:w-[300px]">
  <Card.Content>
    <img src={img} alt="blog" class="h-40 w-full rounded-t-xl object-cover" />
    <p class="px-6 py-2 text-xs sm:text-sm">
      {title}
    </p>
  </Card.Content>
</Card.Root>
