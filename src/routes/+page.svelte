<script>
  import NavBar from '$lib/components/NavBar.svelte'
  import BioAndLink from '$lib/components/Profile/BioAndLink.svelte'
  import Container from '$lib/components/Profile/Container.svelte'
  import UserInfo from '$lib/components/Profile/UserInfo.svelte'
  import TimelineContainer from '$lib/components/Timeline/TimelineContainer.svelte'
</script>

<NavBar />

<main class="flex flex-col">
  <Container>
    <UserInfo />
    <BioAndLink />
  </Container>
</main>
<TimelineContainer />
