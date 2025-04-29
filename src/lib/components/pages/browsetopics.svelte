<script lang="ts">
  import Cards from "./cards.svelte";
  import MarketingCard from "./marketingCard.svelte";
  import Finance from "./finance.svelte";
  import Music from "./music.svelte";
  import Education from "./education.svelte";

  let activeTab = "Design";

  const tab = ["Design", "Marketing", "Finance", "Music", "Education"];
</script>

<div class="py-10 flex flex-col justify-center items-center">
  <h1 class="text-[50px] font-bold">Browse Topics</h1>

  <div class="w-full border-b border-gray-200">
    <div class="flex justify-center space-x-10 pt-5">
      {#each tab as tab}
        <button
          on:click={() => (activeTab = tab)}
          class="pb-5 text-xl tracking-widest text-gray-500 hover:text-[#13547a] focus:outline-none relative"
          class:text-blue-700={activeTab === tab}
          class:font-medium={activeTab === tab}
        >
          {tab}
          {#if activeTab === tab}
            <span class="absolute left-0 bottom-0 w-full h-0.5 bg-[#13547a]"
            ></span>
          {/if}
        </button>
      {/each}
    </div>
  </div>
</div>

<div class="mt-8 p-4">
  {#if activeTab === "Design"}
    <div class="text-center text-xl font-semibold"><Cards /></div>
  {:else if activeTab === "Marketing"}
    <div class="text-center text-xl font-semibold"><MarketingCard/></div>
  {:else if activeTab === "Finance"}
    <div class="text-center text-xl font-semibold"><Finance/></div>
  {:else if activeTab === "Music"}
    <div class="text-center text-xl font-semibold"><Music/></div>
  {:else if activeTab === "Education"}
    <div class="text-center text-xl font-semibold"><Education/></div>
  {/if}
</div>
