<script lang="ts">
  import Twitter from "$lib/icons/twitter.svelte";
  import Facebook from "$lib/icons/Facebook.svelte";
  import Pinterest from "$lib/icons/pinterest.svelte";
  interface Cards {
    name: string;
    paragraph: string;
    Image: string;
  }

  const designCards: Cards[] = [
    {
      name: "Avertising",
      paragraph: "Topic Listing Template on Bootstrap 5",
      Image: "images/designs/mar1.png",
    },
    {
      name: "Video Content",
      paragraph: "Lorem ipsum dolor sit, amet consectetur adipisicing elit.",
      Image: "images/designs/mar2.png",
    },
  ];
</script>

<div class="flex justify-center mx-8">
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8">
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
</div>
