<script>
  import Footer from './lib/Footer.svelte';
  import Header from './lib/Header.svelte';
  import Link from './lib/Link.svelte';
  import NextEvent from './lib/NextEvent.svelte';
  import PastEvent from './lib/PastEvent.svelte';

  let pastEvents = [
    {
      name: 'Game Designers - Finland @ Skunkworks!',
      date: new Date('2022-04-19T19:00:00+02:00'),
      locationName: 'Skunkworks',
      link: 'https://www.meetup.com/game-designers-finland/events/284093445/'
    },
    {
      name: 'Game Designers of Finland Mentor BBQ',
      date: new Date('2022-06-14T18:30:00+02:00'),
      locationName: 'Arcade5',
      link: 'https://www.meetup.com/game-designers-finland/events/285927780/'
    },
    {
      name: 'Matt Dondelinger - Monetization Design',
      date: new Date('2022-09-27T18:30:00+02:00'),
      locationName: 'Arcade5',
      link: 'https://www.meetup.com/game-designers-finland/events/288132002/'
    }
  ]

</script>

<Header />
<main>
  <section id="landing-page" class="ph-m">
    <p class="fw-bold fs-secondary-heading" >Learn and ask the questions about game design that you always wanted to.</p>
    <p class="pv-m">Join meetups and community of professional and aspiring professional game designers in Finland. Find new friends and have thought provoking discussiong with fellow game design enthusiasts.</p>
    <div class="mt-m">
      <Link link="https://www.meetup.com/game-designers-finland/" isButton={true}>Attend next event</Link>
    </div>
  </section>
  <section class="r-20 bg-secondary-100 ph-m pv-l">
    <h2 class="fs-tetriary-heading" >Next event</h2>
    <NextEvent />
  </section>
  <section class="ph-m pv-l">
    <h2 class="fs-tetriary-heading">Past events</h2>
    {#each pastEvents as event, i}
      <PastEvent {...event} index={i}/>
    {/each}
    <p class="pv-m">Join the Game Designers of Finland Meetup group to stay up to date about new events</p>
    <Link link="https://www.meetup.com/game-designers-finland/" isButton={true}>Join group</Link>
  </section>
  <section class="r-20 bg-secondary-100 ph-m pt-l pb-xxl">
    <h2 class="fs-tetriary-heading mb-m" >Community for game designers</h2>
    <p class="mb-m">Game designers of Finland is all about connecting and sharing information with fellow game designers.</p>
    <p>If you enjoy making games, want to share your experiences about solving game design problems or get help and new ideas how to tackle your current design challenges, you’re in the right place!</p>
    <div>
      <div class="flex-1 mt-xxl">
        <img src="./images/logo_discord.png" alt="Discord logo" class="img-s">
        <p class="ml-m"><Link link="_blank">Join our Discord</Link> to discuss about game design.</p>
      </div>
      <div class="flex-1 mt-m">
        <img src="./images/logo_meetup.png" alt="Discord logo" class="img-s">
        <p class="ml-m"><Link link="https://www.meetup.com/game-designers-finland/">Join our Meetup group</Link> to keep up to date about our upcoming and past events.</p>
      </div>
    </div>
  </section>
</main>
<Footer />

<style>
#landing-page {
  height: 90vh;
  margin-top: 20%;
}
</style>
