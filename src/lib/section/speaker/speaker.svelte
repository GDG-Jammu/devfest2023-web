<script>
  import ItemSpeakerCard from '../speaker/ItemSpeakerCard.svelte';
  import Carousel from '../speaker/carousel.svelte';
  import { onMount } from 'svelte';

  const speakers = [
    { name: 'Adit Lal', imageUrl: '/profile_pics/adit.jpeg', designation: 'GDE for Android, Architect @ Viacom 18 - JioCinema' },
    { name: 'Inica Anand', imageUrl: '/profile_pics/incia.jpg', designation: 'Software Engineer @ Oracle' },
    { name: 'Avinash Bhat', imageUrl: '/profile_pics/avinash.jpeg', designation: 'RnD @ Mercedes Benz Research and Development' },
    { name: 'Tanvy Bhola', imageUrl: '/profile_pics/tanvy.jpeg', designation: 'Software Engineer @ Microsoft' },
    { name: 'Vaibhav Malpani', imageUrl: '/profile_pics/vaibhav.jpeg', designation: 'GDE for Cloud, Technical Lead @ Incedo Inc.' },
    { name: 'Rhythm Rajiv Bhatia', imageUrl: '/profile_pics/rhythm.jpeg', designation: 'WTM Ambassador, Founder & CEO @ Cognozire' },
    { name: 'Vrijraj Singh', imageUrl: '/profile_pics/vrijraj.png', designation: 'GDE for Web & Firebase, Tech Lead @ agprop' },
    { name: 'Anubhav Singh', imageUrl: '/profile_pics/anubhavv.jpg', designation: 'GDE for Cloud, Co-founder @ Dynopii' },
    { name: 'Guneet Singh', imageUrl: '/profile_pics/guneet.jpeg', designation: 'Senior Test Engineer @ GlobalLogic' },
    { name: 'Abhinandan Trilokia', imageUrl: '/profile_pics/abhinandan.png', designation: 'Organizer GDG Jammu' },
    { name: 'Atul Sharma', imageUrl: '/profile_pics/atul.jpg', designation: 'Co-Organizer GDG Jammu, ServiceNow developer @ Infosys' },
  ];

  export let autoplay = 3000; // Auto-scroll every 3 seconds
  let perPage = 1; // Default to 1 image per page for mobile

  // Adjust `perPage` dynamically based on screen size
  onMount(() => {
    function updatePerPage() {
      if (window.innerWidth >= 1024) {
        perPage = 3; // Show 3 images per page on large screens
      } else if (window.innerWidth >= 768) {
        perPage = 2; // Show 2 images per page on medium screens
      } else {
        perPage = 1; // Show 1 image per page on small screens
      }
    }

    updatePerPage();
    window.addEventListener('resize', updatePerPage);

    return () => {
      window.removeEventListener('resize', updatePerPage);
    };
  });
</script>

<section id="speaker" class="speaker-section">
  <div class="speaker-header">
    <h2>Previous Speakers</h2>
    <p>We have some of the best speakers in the industry who will be sharing their knowledge and experience with you.</p>
  </div>

  <div class="carousel">
    <Carousel autoplay={autoplay} {perPage} loop={true} duration={300}>
      {#each speakers as speaker}
        <ItemSpeakerCard
          name={speaker.name}
          imageUrl={speaker.imageUrl}
          designation={speaker.designation}
        />
      {/each}
    </Carousel>
  </div>
</section>

<style>
.speaker-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px 16px;
}

.speaker-header {
  text-align: center;
}

.carousel {
  display: flex;
  overflow-x: auto;
  gap: 16px;
}

.carousel > :global(div) {
  flex: 0 0 auto;
  scroll-snap-align: center;
}
</style>
