<script lang="ts">
  import Blur from '$lib/section/blur/Blur.svelte';
  import Hero from '$lib/section/hero/Hero.svelte';
  import Memories from '$lib/section/memories/Memories.svelte';
  import Sponsors from '$lib/section/sponsors/Sponsors.svelte';
  import Partners from '$lib/section/partners/Partners.svelte';
  import Tickets from '$lib/section/tickets/Tickets.svelte';
  import Why from '$lib/section/why/Why.svelte';
  import Cfp from '$lib/section/CFP/cfp.svelte'
  import Youtube from '$lib/section/youtube/youtube.svelte';
  import Corporate from '$lib/section/coporate Partners/corporate.svelte';
  import Faq from '$lib/section/faq/FAQ.svelte';
</script>

<svelte:head>
  <title>GDG Jammu - Devfest 2023</title>
  <meta name="description" content="GDG Jammu - Devfest 2023" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#ffffff" />
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:site" content="@gdgjammu" />
  <meta name="twitter:creator" content="@gdgjammu" />
  <meta name="twitter:title" content="GDG Jammu - Devfest 2023" />
  <meta name="twitter:description" content="GDG Jammju - Devfest 2023" />
  <meta
    name="twitter:image"
    content="https://devfest.gdgjammu.com/gdgjammu-banner.png"
  />
  <meta property="og:type" content="website" />
  <meta property="og:title" content="GDG Jammu - Devfest 2023" />
  <meta property="og:description" content="GDG Jammu - Devfest 2023" />
  <meta property="og:site_name" content="GDG Jammu - Devfest 2023" />
  <meta property="og:url" content="https://devfest.gdgjammu.com/" />
  <meta
    property="og:image"
    content="https://devfest.gdgjammu.com/gdgjammu-banner.png"
  />
</svelte:head>

<div
  class="flex min-h-screen flex-col items-center justify-start overflow-hidden p-8"
>
  <div class="space-y-16 md:space-y-44 m-1">
    <Blur />
    <Hero />
    
    <!--<Cfp />-->
    <Why />
    <Tickets />
    <Partners />
    <!--<Sponsors />-->
    <Faq/>
     
  
   <!-- <Corporate />-->
   <Memories />
  </div>
</div>
