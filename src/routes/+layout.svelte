<script lang="ts">
  import Footer from '$lib/footer/Footer.svelte';
  import Header from '$lib/header/Header.svelte';
  import { Modals, closeModal } from 'svelte-modals';
  import '../app.css';
  import Speaker from '$lib/section/speaker/speaker.svelte';
  import Blur from '$lib/section/blur/Blur.svelte';
  import Hero from '$lib/section/hero/Hero.svelte';
  import Memories from '$lib/section/memories/Memories.svelte';
  import Sponsors from '$lib/section/sponsors/Sponsors.svelte';
  import Partners from '$lib/section/partners/Partners.svelte';
  import Tickets from '$lib/section/tickets/Tickets.svelte';
  import Why from '$lib/section/why/Why.svelte';
  import Cfp from '$lib/section/CFP/cfp.svelte';
  import Youtube from '$lib/section/youtube/youtube.svelte';
  import Corporate from '$lib/section/coporate Partners/corporate.svelte';
  import Faq from '$lib/section/faq/FAQ.svelte';
</script>

<svelte:head>
  <script src="https://kit.fontawesome.com/3e56677f9e.js" crossorigin="anonymous"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
  <style>
    @import url('https://fonts.googleapis.com/css?family=Google+Sans:400,500&display=swap');
  </style>
  <meta name="description" content="An amazing event with industry-leading speakers, sponsors, and activities. Don't miss out!" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</svelte:head>

<main>
  <div id="container" class="mx-auto">
    <Modals>
      <div
        slot="backdrop"
        class="backdrop"
        role="button"
        aria-label="Close modal"
        on:click={closeModal}
      />
    </Modals>
    <Header />
    <Blur />
    <Hero />
    <Why />
    <Cfp />
    <Speaker />
    <Tickets />
    <Sponsors />
    <Partners />
    <Faq />
    <Memories />
    <Footer />
  </div>
</main>

<style>
  #container {
    margin: 0 auto;
    max-width: 1200px;
    padding: 0 16px;
    box-sizing: border-box;
  }

  .backdrop {
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    z-index: 40;
    background: rgba(0, 0, 0, 0.5);
  }
</style>
