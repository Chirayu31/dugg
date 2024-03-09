<script>
  import NavBar from '$lib/components/NavBar.svelte'
  import BioAndLink from '$lib/components/Profile/BioAndLink.svelte'
  import Container from '$lib/components/Profile/Container.svelte'
  import UserInfo from '$lib/components/Profile/UserInfo.svelte'
  import TimelineContainer from '$lib/components/Timeline/TimelineContainer.svelte'
  import data from '$lib/data.json'

  const profile = data.profile
  const timeline = data.timeline
</script>

<NavBar />

<main class="flex flex-col">
  <Container>
    <UserInfo imgUrl={profile.profilePic} name={profile.fullName} />
    <BioAndLink
      bio={profile.bio}
      companyLogo={profile.companyLogo}
      companyName={profile.company}
      position={profile.position}
      website={profile.website}
    />
  </Container>
</main>
<TimelineContainer timelineData={timeline}/>
