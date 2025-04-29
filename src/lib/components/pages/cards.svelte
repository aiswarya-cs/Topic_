<script lang="ts">
  interface Cards {
    name: string;
    paragraph: string;
    Image: string;
  }

  const designCards: Cards[] = [
    {
      name: "Web Design",
      paragraph: "Topic Listing Template on Bootstrap 5",
      Image: "images/designs/design1.png",
    },
    {
      name: "Graphics",
      paragraph: "Lorem ipsum dolor sit, amet consectetur adipisicing elit.",
      Image: "images/designs/design2.png",
    },
    {
      name: "Logo Design",
      paragraph: "Lorem ipsum dolor sit, amet consectetur adipisicing elit.",
      Image: "images/designs/design3.png",
    },
  ];
</script>

<div class="flex justify-center mx-8">
  <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    {#each designCards as design}
    <div class="bg-neutral-100 rounded-2xl shadow-lg p-6 flex flex-col items-center text-center relative hover:shadow-2xl transition">
      <div class="absolute top-4 right-4 bg-blue-600 text-white text-sm font-bold px-2 py-1 rounded-full">
        15
      </div>
      <h2 class="text-xl text-start font-bold mb-2">{design.name}</h2>
      <p class="text-gray-500 mb-6 text-start">{design.paragraph}</p>
      <img src={design.Image} alt={design.name} class="h-40 object-contain" />
    </div>
    {/each}
  </div>
</div>
