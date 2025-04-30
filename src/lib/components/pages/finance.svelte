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

<div class="flex justify-center px-4 md:px-8 py-8">
  <div class="grid grid-cols-1 md:grid-cols-2 gap-8 w-full max-w-7xl">
    <!-- Investment Card -->
    <div class="w-full min-h-[300px] p-4 bg-white rounded-3xl shadow-md flex flex-col justify-between">
      <div>
        <div class="flex justify-between items-start">
          <h2 class="text-2xl md:text-3xl font-bold text-gray-900">Investment</h2>
          <div class="bg-blue-500 text-white text-xs font-bold rounded-full w-8 h-8 flex items-center justify-center">
            30
          </div>
        </div>
        <p class="pt-3 text-gray-600 text-base text-start md:text-lg">
          Lorem Ipsum dolor sit amet consectetur
        </p>
      </div>
      <img src="images/web-design.png" alt="Investment Graph" class="w-full h-[250px] mt-4 object-contain" />
    </div>

    <!-- Finance Card -->
    <div
      class="w-full p-4 rounded-3xl bg-cover bg-center text-white flex flex-col justify-between"
      style="background-image: linear-gradient(rgba(19,84,122,0.6), rgba(19,84,122,0.6)), url('/images/businesswoman-using-tablet-analysis.jpg');"
    >
      <div class="flex flex-col justify-start">
        <div class="flex justify-between items-start">
          <h2 class="text-2xl md:text-3xl font-bold">Finance</h2>
          <div class="bg-blue-500 text-white text-xs font-bold rounded-full w-8 h-8 flex items-center justify-center">
            25
          </div>
        </div>

        <p class="mt-4 text-base text-start md:text-lg">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sint animi necessitatibus aperiam repudiandae nam omnis.
        </p>

        <button class="mt-6 bg-[#80d0c7] w-52 text-white font-semibold py-2 px-6 rounded-full hover:bg-[#5bb5a8] transition duration-300">
          Learn More
        </button>
      </div>

      <div class="mt-24">
        <p class="text-white text-start text-sm mb-2">Share:</p>
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
