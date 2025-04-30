<script lang="ts">
  import Search from "$lib/icons/search.svelte";
  import Twitter from "$lib/icons/twitter.svelte";
  import Facebook from "$lib/icons/Facebook.svelte";
  import Faq from "$lib/components/pages/faq.svelte";
  import Pinterest from "$lib/icons/pinterest.svelte";
  import Contact from "$lib/components/pages/contact.svelte";
  import Browsetopics from "$lib/components/pages/browsetopics.svelte";

  const steps = [
    {
      icon: "🔍",
      title: "Search your favourite topic",
      description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. 
        Reiciendis, cumque magnam? Sequi, cupiditate quibusdam alias illum sed esse 
        ad dignissimos libero sunt, quisquam numquam aliquam? Voluptas, accusamus omnis?`,
    },
    {
      icon: "🔖",
      title: "Bookmark & Keep it for yourself",
      description: `Lorem ipsum dolor, sit amet consectetur adipisicing elit. 
        Sint animi necessitatibus aperiam repudiandae nam omnis est vel quo, 
        nihil repellat quia velit error modi earum similique odit labore. Doloremque, repudiandae?`,
    },
    {
      icon: "📖",
      title: "Read & Enjoy",
      description: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. 
        Animi vero quisquam, rem assumenda similique voluptas distinctio, iste est hic 
        eveniet debitis ut ducimus beatae id? Quam culpa deleniti officiis autem?`,
    },
  ];
</script>

<section class="h-auto w-full bg-teal-50">
  <div
    class="h-[500px] bg-gradient-to-tr from-[#13547a] to-[#80d0c7] flex justify-center items-center"
  >
    <div class="text-center">
      <h1
        class="text-white text-3xl md:text-[60px] lg:text-[70px] font-extrabold"
      >
        Discover. Learn. Enjoy
      </h1>
      <h5 class="text-[#093b58] text-lg md:text-2xl font-bold mt-5">
        platform for creatives around the world
      </h5>

      <div class="w-full max-w-[800px] mx-auto mt-5 px-4 sm:px-6">
        <div
          class="h-16 md:h-20 w-full bg-white rounded-full flex items-center gap-2 px-3 shadow-sm"
        >
          <!-- Search Icon -->
          <div class="flex-shrink-0">
            <Search data="w-6 h-6 md:w-8 md:h-8" />
          </div>

          <!-- Input -->
          <input
            type="text"
            class="flex-1 h-full text-base md:text-xl px-4 focus:outline-none"
            placeholder="Design, Code, Marketing, Finance.."
          />

          <!-- Button -->
          <div
            class="flex-shrink-0 bg-[#80d0c7] rounded-full px-4 py-2 md:px-6 md:py-3 cursor-pointer flex items-center justify-center"
          >
            <h2
              class="text-white font-semibold text-sm md:text-lg whitespace-nowrap"
            >
              Search
            </h2>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div
    class="bg-[#80d0c7] lg:rounded-b-[200px] flex flex-col md:flex-row items-center
     justify-center gap-5 py-10 px-4 md:px-10"
  >
    <!-- Card 1: Web Designer -->
    <div
      class="w-full md:w-[400px] min-h-[400px] bg-white rounded-3xl p-4 md:-mt-32"
    >
      <div class="flex justify-between items-start">
        <h2 class="text-2xl md:text-3xl font-bold">Web Designer</h2>
        <div
          class="bg-blue-500 text-white text-xs font-bold rounded-full w-8 h-8 flex items-center justify-center"
        >
          14
        </div>
      </div>
      <p class="pt-3 text-base md:text-lg pr-2">
        When you search for free CSS templates, you will notice that TemplateMo
        is one of the best websites.
      </p>
      <img
        src="images/web-design.png"
        alt="web designer"
        class="w-full h-auto mt-4"
      />
    </div>

    <!-- Card 2: Finance -->
    <div
      class="w-full md:w-[550px] min-h-[440px] p-4 rounded-3xl bg-cover bg-center md:-mt-32"
      style="background-image: linear-gradient(rgba(19,84,122,0.6), rgba(19,84,122,0.6)), url('/images/businesswoman-using-tablet-analysis.jpg');"
    >
      <div class="flex flex-col justify-between h-full">
        <div>
          <div class="flex justify-between items-start">
            <h2 class="text-white text-2xl md:text-3xl font-bold">Finance</h2>
            <div
              class="bg-blue-500 text-white text-xs font-bold rounded-full w-8 h-8 flex items-center justify-center"
            >
              25
            </div>
          </div>

          <p class="text-white text-base md:text-lg mt-4">
            Topic Listing Template includes homepage, listing page, detail page,
            and contact page. You can feel free to edit and adapt for your CMS
            requirements.
          </p>

          <button
            class="mt-6 bg-[#80d0c7] text-white font-semibold py-2 px-6 rounded-full hover:bg-[#5bb5a8] transition-colors"
          >
            Learn More
          </button>
        </div>

        <div class="mt-20">
          <p class="text-white text-sm mb-2">Share:</p>
          <div class="flex space-x-4">
            <!-- Replace with actual icons or images if not using React -->
            <button
              class="w-10 h-10 bg-[#80d0c7] rounded-full flex items-center justify-center text-white"
            >
              <Twitter />
            </button>

            <button
              class="w-10 h-10 bg-[#80d0c7] rounded-full flex items-center justify-center text-white"
            >
              <Facebook />
            </button>

            <button
              class="w-10 h-10 bg-[#80d0c7] rounded-full flex items-center justify-center text-white"
            >
              <Pinterest />
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="my-5" id="browse-topics">
  <Browsetopics />
</section>

<section
  class="my-8 bg-[linear-gradient(rgba(19,84,122,0.8),rgba(19,84,122,0.8)),url('/images/colleagues-working-cozy-office-medium-shot.jpg')]
   h-auto w-full bg-cover bg-no-repeat"
   id="how-it-works"
>
  <div
    class="flex flex-col justify-center items-center gap-14 py-10 text-white"
  >
    <h1 class="text-[50px] text-center font-extrabold mb-5">
      How does it work?
    </h1>
    <div class="max-w-5xl mx-auto grid md:grid-cols-[auto_1fr] gap-6">
      <div class="hidden lg:flex flex-col items-center relative">
        <div class="absolute top-8 bottom-8 w-1 bg-teal-400"></div>
        {#each steps as step, i}
          <div class="relative z-10 mt-16 last:mb-0">
            <div
              class="w-16 h-16 rounded-full flex items-center justify-center text-2xl font-bold border-4 border-white bg-cyan-800"
            >
              {step.icon}
            </div>
          </div>
        {/each}
      </div>
      <div class="space-y-16">
        {#each steps as step}
          <div class="mx-5 lg:mx-0">
            <h3 class="text-3xl font-bold mb-3">{step.title}</h3>
            <p class="text-white/90 text-lg md:text-xl leading-relaxed">{step.description}</p>
          </div>
        {/each}
      </div>
    </div>

    <div class="mb-10 flex flex-col gap-5 md:flex-row">
      <span class="text-xl mr-5">Want to learn more? </span>
      <button
        class="border-2 -mt-2 p-3 rounded-4xl text-lg border-[#6bb8e6] text-[#6bb8e6]"
        >Check Out Youtube?</button
      >
    </div>
  </div>
</section>


<section id="faq">
  <Faq />
</section>

<section id="contact-us">
  <Contact />
</section>
