<script>
    import { onMount } from 'svelte';
    import Link from './Link.svelte';
    let event = {
        name: 'Battle systems',
        date: new Date('2022-11-29T18:30:00+02:00'),
        locationName: 'Metacore',
        address: 'Porkkalankatu 24',
        city: 'Helsinki',
        description: "When you create a game that has battle and combat, they’re the systems that  the players interact with the most. Designing a combat system that supports the player experience you want to deliver is key for creating games that players enjoy and want to return to. To learn what you should consider when designing a great combat and battle system for your game, join us at Metacore office!",
        link: 'https://www.meetup.com/game-designers-finland/'
    }

    let daysToEvent; 
    onMount(() => {
        const oneDay = 24 * 60 * 60 * 1000; // Number of milliseconds in one day, hours * hinutes * seconds * milliseconds in a single day
        const differenceInMs = event.date.valueOf() - Date.now();
        daysToEvent = Math.round(differenceInMs / oneDay);
        
    });
    
</script>
<div class="pv-m">
    <h3 class="fw-bold fs-heading-l">{event.name}</h3>
    <p class="text-accent-500">{event.date.toLocaleString('en-GB', {weekday: 'long'})} - {event.date.toLocaleDateString('fi')} - {event.date.toLocaleTimeString('fi')}</p>
    {#if daysToEvent > 0}
    <p class="text-accent-500">In { daysToEvent } days</p> 
    {:else if daysToEvent === 0}
    <p class="text-accent-500">Today!</p> 
    {/if}
    <div class="pv-m text-grey-400">
        <p>{event.locationName}</p>
        <p>{event.address}, {event.city}</p>
    </div>
    <p>{event.description}</p>
    <div class="pv-m">
        <Link link={ event.link } isButton={true}>Attend</Link>
    </div>
</div>
