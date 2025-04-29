<script lang="ts">
  import Search from "$lib/icons/search.svelte";
  import Twitter from "$lib/icons/twitter.svelte";
  import Facebook from "$lib/icons/Facebook.svelte";
  import Pinterest from "$lib/icons/pinterest.svelte";
  import Browsetopics from "$lib/components/pages/browsetopics.svelte";
</script>

<section class="h-auto w-full bg-teal-50">
  <div
    class="h-[500px] bg-gradient-to-tr from-[#13547a] to-[#80d0c7] flex justify-center items-center"
  >
    <div class="text-center">
      <h1 class="text-white text-4xl md:text-[70px] font-extrabold">
        Discover. Learn. Enjoy
      </h1>
      <h5 class="text-[#093b58] text-lg md:text-2xl font-bold mt-5">
        platform for creatives around the world
      </h5>

      <div
        class="h-16 md:h-20 w-[350px] md:w-[800px] mx-5 bg-white mt-5 rounded-full flex justify-between items-center px-2"
      >
        <div class="pl-3">
          <Search data="w-12 h-8" />
        </div>

        <input
          type="text"
          class="h-full border-0 flex-1 text-xl px-5 focus:outline-none"
          placeholder="Design, Code, Marketing, Finance.."
        />

        <div
          class="w-12 md:w-32 h-12 md:h-14 bg-[#80d0c7] rounded-full flex justify-center items-center cursor-pointer"
        >
          <h2 class="text-white font-semibold text-sm md:text-lg">Search</h2>
        </div>
      </div>
    </div>
  </div>

  <div
    class="h-1/2 bg-[#80d0c7] md:rounded-b-[200px] md:flex md:justify-center gap-5 pb-20"
  >
    <div class="md:w-[400px] h-[400px] p-4 bg-white rounded-3xl py-4 md:-mt-20">
      <div class="flex justify-between items-start">
        <h2 class="text-3xl font-bold">Web Designer</h2>
        <div
          class="bg-blue-500 text-white text-xs font-bold rounded-full w-8 h-8 flex items-center justify-center"
        >
          14
        </div>
      </div>
      <p class="pr-4 pt-3 text-lg">
        When you search for free CSS templates, you will notice that TemplateMo
        is one of the best websites.
      </p>
      <img src="images/web-design.png" alt="" srcset="" class="w-auto" />
    </div>

    <div
      class="w-[550px] h-[400px] p-4 bg-white rounded-3xl
    bg-[linear-gradient(rgba(19,84,122,0.6),rgba(19,84,122,0.6)),url('/images/businesswoman-using-tablet-analysis.jpg')]
     bg-cover bg-center md:-mt-20"
    >
      <div>
        <div class="flex justify-between items-start">
          <h2 class="text-white text-3xl font-bold">Finance</h2>
          <div
            class="bg-blue-500 text-white text-xs font-bold rounded-full w-8 h-8 flex items-center justify-center"
          >
            25
          </div>
        </div>

        <p class="text-white text-lg mt-4">
          Topic Listing Template includes homepage, listing page, detail page,
          and contact page. You can feel free to edit and adapt for your CMS
          requirements.
        </p>

        <button
          class="mt-6 bg-[#80d0c7] text-white font-semibold py-2 px-6 rounded-full hover:bg-[#5bb5a8]"
        >
          Learn More
        </button>
      </div>

      <div class="mt-24">
        <p class="text-white text-sm mb-2">Share:</p>
        <div class="flex space-x-4">
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
</section>

<section class="my-5">
  <Browsetopics />
</section>

<section
  class="my-8 bg-[linear-gradient(rgba(19,84,122,0.6),rgba(19,84,122,0.6)),url('/images/colleagues-working-cozy-office-medium-shot.jpg')]
   h-auto w-full bg-cover bg-no-repeat"
>
  <div class="flex flex-col justify-center items-center py-8 text-white">
    <h1 class="text-[50px] font-extrabold mb-5">How does it work?</h1>
    <div class="w-1/2 mb-8">
      <h1 class="text-3xl font-bold tracking-wider">
        Search your favourite topic
      </h1>
      <p class="text-lg mt-5 leading-8">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis,
        cumque magnam? Sequi, cupiditate quibusdam alias illum sed esse ad
        dignissimos libero sunt, quisquam numquam aliquam? Voluptas, accusamus
        omnis?
      </p>
    </div>

    <div class="w-1/2 mb-8">
      <h1 class="text-3xl font-bold tracking-wider">
        Bookmark & Keep it for yourself
      </h1>
      <p class="text-lg mt-5 leading-8">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sint animi
        necessitatibus aperiam repudiandae nam omnis est vel quo, nihil repellat
        quia velit error modi earum similique odit labore. Doloremque,
        repudiandae?
      </p>
    </div>

    <div class="w-1/2 mb-8">
      <h1 class="text-3xl font-bold tracking-wider">Read & Enjoy</h1>
      <p class="text-lg mt-5 leading-8">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Animi vero
        quisquam, rem assumenda similique voluptas distinctio, iste est hic
        eveniet debitis ut ducimus beatae id? Quam culpa deleniti officiis
        autem?
      </p>
    </div>

    <div>
      <span class="text-xl mr-5">Want to learn more? </span>
      <button
        class="border-2 p-3 rounded-4xl text-lg border-[#6bb8e6] text-[#6bb8e6]"
        >Check Out Youtube?</button
      >
    </div>
  </div>
</section>
