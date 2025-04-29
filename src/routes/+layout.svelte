<script lang="ts">
  import "../app.css";
  import Account from "$lib/icons/account.svelte";
  import Logo from "$lib/icons/logo.svelte";
  import { onMount } from "svelte";

  let { children } = $props();

  let scrolled = $state(false);

  // Add an event listener to detect scrolling
  const handleScroll = () => {
    if (window.scrollY > 50) {
      scrolled = true;
    } else {
      scrolled = false;
    }
  };

  // Run the scroll handler when the component is mounted
  onMount(() => {
    window.addEventListener("scroll", handleScroll);

    // Clean up event listener when component is destroyed
    return () => {
      window.removeEventListener("scroll", handleScroll);
    };
  });

  let isOpen = $state(false);

  function toggleMenu() {
    isOpen = !isOpen;
  }
</script>

<div class="fixed z-50 w-full bg-transparent transition-all">
  <nav
    class={`flex items-center justify-between px-5 md:px-24 py-4 ${scrolled ? "bg-[#80d0c7]" : "bg-transparent"} transition-colors duration-300`}
  >
    <div class="text-lg flex gap-2">
      <Logo data="w-10 h-10" /><span class="font-bold text-3xl">Topic</span>
    </div>
    <ul class="hidden gap-8 md:flex">
      <li
        class="text-lg text-white hover:text-[#13547a] hover:decoration-2 hover:transition-all hover:duration-700 hover:ease-in-out"
      >
        <a href="#projects">HOME</a>
      </li>
      <li
        class="text-lg text-white hover:text-[#13547a] hover:decoration-2 hover:transition-all hover:duration-700 hover:ease-in-out"
      >
        <a href="#about">Browse Topics</a>
      </li>
      <li
        class="text-lg text-white hover:text-[#13547a] hover:decoration-2 hover:transition-all hover:duration-700 hover:ease-in-out"
      >
        <a href="#about">How It Works</a>
      </li>
      <li
        class="text-lg text-white hover:text-[#13547a] hover:decoration-2 hover:transition-all hover:duration-700 hover:ease-in-out"
      >
        <a href="#contact">FAQ's</a>
      </li>
      <li
        class="text-lg text-white hover:text-[#13547a] hover:decoration-2 hover:transition-all hover:duration-700 hover:ease-in-out"
      >
        <a href="#contact">Contact</a>
      </li>
      <li
        class="text-lg text-white hover:text-[#13547a] hover:decoration-2 hover:transition-all hover:duration-700 hover:ease-in-out"
      >
        <a href="#contact">PAGES</a>
      </li>
    </ul>

    <div>
      <Account data="hidden w-9 h-9 md:flex fill-[#13547a]" />
    </div>

    <button class="md:hidden" onclick={toggleMenu}>
      <!-- <Menu data="w-8 h-8 fill-[#dc3545]" /> -->
    </button>
  </nav>

  {#if isOpen}
    <ul class="hidden gap-5 md:flex">
      <li class="text-lg text-white hover:text-[#13547a]">
        <a href="#projects">HOME</a>
      </li>
      <li class="text-lg text-white hover:text-[#13547a]">
        <a href="#about">WHY US</a>
      </li>
      <li class="text-lg text-white hover:text-[#13547a]">
        <a href="#about">TRAINERS</a>
      </li>
      <li class="text-lg text-white hover:text-[#13547a]">
        <a href="#contact">CONTACT US</a>
      </li>
    </ul>
  {/if}
</div>

{@render children()}
