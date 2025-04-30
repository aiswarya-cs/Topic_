<script>
  export let question;
  export let answer;
  let open = false;
</script>

<div class="border-0 my-1 w-full px-5 md:px-0 md:mx-0 md:w-4/5">
  <button
    on:click={() => (open = !open)}
    class="flex justify-between items-center w-full px-4 py-5 text-left font-semibold text-2xl
     text-gray-800 bg-transparent rounded-4xl hover:bg-blue-100 transition"
  >
    {question}
    <svg
      class="w-5 h-5 transform transition-transform"
      class:rotate-180={open}
      fill="none"
      stroke="currentColor"
      viewBox="0 0 24 24"
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        d="M19 9l-7 7-7-7"
      />
    </svg>
  </button>

  {#if open}
    <div class="px-4 pt-2 pb-4 text-start text-gray-600 text-lg">
      {@html answer}
    </div>
  {/if}
</div>
