<script>
    import Link from './Link.svelte';
    let event = {
        name: 'Battle systems',
        date: new Date('2022-11-29T18:30:00+02:00'),
        locationName: 'Metacore',
        address: 'Porkkalankatu 24',
        city: 'Helsinki',
        description: "When you create a game that has battle and combat, they’re the systems that  the players interact with the most. Designing a combat system that supports the player experience you want to deliver is key for creating games that players enjoy and want to return to. To learn what you should consider when designing a great combat and battle system for your game, join us and the following experts at Metacore office! Arto Koistinen from Random Potion will share how to control randomness in battle design. Alex Clark from Nitro Games will tell",
        link: 'https://www.meetup.com/game-designers-finland/'
    }
</script>
<div class="pv-m">
    <h3 class="fw-bold fs-tetriary-heading">{event.name}</h3>
    <p class="text-accent-500">{event.date.toLocaleString('en-GB', {weekday: 'long'})} - {event.date.toLocaleDateString('fi')} - {event.date.toLocaleTimeString('fi')}</p>
    <div class="pv-m text-primary-400">
        <p>{event.locationName}</p>
        <p>{event.address}, {event.city}</p>
    </div>
    <p>{event.description}</p>
    <div class="pv-m">
        <Link link="https://www.meetup.com/game-designers-finland/" text="Attend" />
    </div>
</div>
