<script lang="ts">
  interface Cards {
    name: string;
    paragraph: string;
    Image: string;
  }

  const designCards: Cards[] = [
    {
      name: "Educator",
      paragraph: "Topic Listing Template on Bootstrap 5",
      Image: "images/designs/undraw_Educator_re_ju47.png",
    },
    {
      name: "Graduation",
      paragraph: "Lorem ipsum dolor sit, amet consectetur adipisicing elit.",
      Image:"images/designs/undraw_Graduation_re_gthn.png",
    },
  ];
</script>

<div class="flex justify-center mx-8">
  <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
    {#each designCards as design}
    <div class="bg-white rounded-2xl shadow-lg p-6 flex flex-col items-center text-center relative hover:shadow-2xl transition">
      <div class="absolute top-4 right-4 bg-green-800 text-white text-sm font-bold px-2 py-1 rounded-full">
        15
      </div>
      <h2 class="text-xl text-start font-bold mb-2">{design.name}</h2>
      <p class="text-gray-500 mb-6 text-start">{design.paragraph}</p>
      <img src={design.Image} alt={design.name} class="h-40 object-contain" />
    </div>
    {/each}
  </div>
</div>
