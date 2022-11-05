<script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'
  import Header from './lib/Header.svelte';
  import Link from './lib/Link.svelte';
  import NextEvent from './lib/NextEvent.svelte';
</script>

<Header />
<main>
  <section id="landing-page" class="ph-m">
    <p class="fw-bold fs-secondary-heading" >Learn and ask the questions about game design that you always wanted to.</p>
    <p class="pv-m">Join meetups and community of professional and aspiring professional game designers in Finland. Find new friends and have thought provoking discussiong with fellow game design enthusiasts.</p>
    <div class="mt-m">
      <Link link="https://www.meetup.com/game-designers-finland/" text="Attend next event" />
    </div>
  </section>
  <section class="r-20 bg-secondary-100 p-m">
    <h2 class="fs-tetriary-heading" >Next event</h2>
    <NextEvent />
  </section>
</main>

<style>
#landing-page {
  height: 90vh;
  margin-top: 20%;
}
</style>
