<script>
  import ItemSpeakerCard from '../speaker/ItemSpeakerCard.svelte';
  import Carousel from '../speaker/carousel.svelte';
	
	let colors = ['red', 'orange', 'yellow', 'green', 'blue', 'purple']

  const speakers = [
    {
      name: 'Adit Lal',
      imageUrl:
        '/profile_pics/adit.jpeg',
      designation: 'GDE for Android, Architect @ Viacom 18 - JioCinema'
    },
   
    {
      name: 'Inica Anand',
      imageUrl:
        '/profile_pics/incia.jpg',
      designation: 'Software Engineer @ Oracle '
    },
    {
      name: 'Avinash Bhat',
      imageUrl:
        '/profile_pics/avinash.jpeg',
      designation: 'RnD @ Mercedes Benz Research and Development'
    },
    {
      name: 'Tanvy Bhola',
      imageUrl:
        '/profile_pics/tanvy.jpeg',
      designation: 'Software Engineer @ Microsoft'
    },
    {
      name: 'Vaibhav Malpani',
      imageUrl:
        '/profile_pics/vaibhav.jpeg',
      designation: 'GDE for Cloud, Technical Lead @ Incedo Inc.s'
    },
    {
      name: 'Rhythm Rajiv Bhatia',
      imageUrl:
        '/profile_pics/rhythm.jpeg',
      designation: 'WTM Ambassador,  Founder & CEO @ Cognozire'
    },
    {
      name: 'Vrijraj Singh',
      imageUrl:
        '/profile_pics/vrijraj.png',
      designation: 'GDE for Web & Firebase, Tech Lead @ agprop '
    },
    {
      name: 'Anubhav Singh',
      imageUrl:
        '/profile_pics/anubhavv.jpg',
      designation: 'GDE for Cloud, Co-founder @ Dynopii'
    },
    {
      name: 'Guneet Singh',
      imageUrl:
        '/profile_pics/guneet.jpeg',
      designation: 'Senior Test Engineer @ GlobalLogic'
    },
    {
      name: 'Abhinandan Trilokia',
      imageUrl:
        '/profile_pics/abhinandan.png',
      designation: 'Organizer GDG Jammu'
    } ,
    {
      name: 'Atul Sharma',
      imageUrl:
        '/profile_pics/atul.jpg',
      designation: 'Co-Organizer GDG Jammu, ServiceNow developer @ Infosys '
    }
  ];
</script>

<section
  id="speaker"
  class="max-auto flex w-full flex-col items-center space-y-6 px-8"
>
  <div class="flex flex-col">
    <div class="flex justify-center pt-12 sm:pt-16 lg:pt-20">
      <div
        class="flex max-w-xs flex-col items-center justify-center text-center sm:max-w-7xl"
      >
        <h2
          class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl lg:text-5xl"
        >
          Our Speakers
        </h2>
        <p class="text-md mt-4 flex w-full max-w-3xl text-center text-gray-600">
          We have some of the best speakers in the industry who will be sharing
          their knowledge and experience with you.
        </p>
      </div>
    </div>

    <div
      class="mx-auto w-full max-w-7xl justify-center space-y-12 py-10 px-10 sm:space-y-0 sm:px-10 md:flex md:space-x-10 lg:space-x-10"
    >
    <Carousel autoplay="2000">
      {#each speakers as speaker}
        <ItemSpeakerCard
          name={speaker.name}
          imageUrl={speaker.imageUrl}
          designation={speaker.designation}
        />
      {/each}
      <!-- <span slot="left-control">Left</span>
      <span slot="right-control">Right</span> -->
    </Carousel>

    </div>
  </div>
</section>

<style>
	div {
		height: 100%;
		width: 100%;
	}

	span {
		display: inline-block;
	}
</style>