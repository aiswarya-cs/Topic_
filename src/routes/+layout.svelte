<script lang="ts">
  import "../app.css";
  import Account from "$lib/icons/account.svelte";
  import Logo from "$lib/icons/logo.svelte";
  import Menu from "$lib/icons/menu.svelte";
  import { onMount } from "svelte";

  let { children } = $props();

  const navItems = [
    { name: "HOME", href: "#projects" },
    { name: "Browse Topics", href: "#about" },
    { name: "How It Works", href: "#about" },
    { name: "FAQ's", href: "#contact" },
    { name: "Contact", href: "#contact" },
    { name: "PAGES", href: "#contact" },
  ];

  let scrolled = $state(false);

  const handleScroll = () => {
    if (window.scrollY > 50) {
      scrolled = true;
    } else {
      scrolled = false;
    }
  };

  onMount(() => {
    window.addEventListener("scroll", handleScroll);
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
    <ul class="hidden gap-8 lg:flex">
      {#each navItems as item}
        <li
          class="text-lg text-white hover:text-[#13547a] hover:decoration-2 hover:transition-all hover:duration-500 hover:ease-in-out relative group inline-block"
        >
          <a href={item.href}>
            {item.name}
            <span
              class="absolute left-0 bottom-0 w-0 h-[2px] bg-[#13547a] transition-all duration-500 ease-initial group-hover:w-full"
            ></span>
          </a>
        </li>
      {/each}
    </ul>

    <div>
      <Account data="w-9 h-9 md:flex fill-[#13547a]" />
    </div>

    <button class="lg:hidden" onclick={toggleMenu}>
      <Menu data="w-8 h-8 fill-[#13547a]" />
    </button>
  </nav>

  {#if isOpen}
    <ul class="flex flex-col bg-[#13547a] p-5 gap-5 lg:hidden">
      {#each navItems as item}
        <li
          class="text-lg text-white hover:text-[#13547a] hover:decoration-2 hover:transition-all hover:duration-500 hover:ease-in-out relative group inline-block"
        >
          <a href={item.href}>
            {item.name}
            <span
              class="absolute left-0 bottom-0 w-0 h-[2px] bg-[#13547a] transition-all duration-500 ease-initial group-hover:w-full"
            ></span>
          </a>
        </li>
      {/each}
    </ul>
  {/if}
</div>

{@render children()}

<footer class="bg-white dark:bg-gray-50 py-5">
  <div class="mx-auto w-full max-w-screen-xl px-4 py-6 lg:py-8">
    <div class="md:flex md:justify-start md:gap-5">
      <div class="mb-6 md:mb-0 w-full md:w-96">
        <a href="/" class="flex items-center">
          <Logo data="w-10 h-10" />
          <span class="font-bold text-3xl ml-2">Topic</span>
        </a>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 w-full">
        <div>
          <h2
            class="mb-6 text-xl font-bold tracking-wide text-gray-900 uppercase dark:text-gray-900"
          >
            Resources
          </h2>
          <ul class="text-gray-500 dark:text-gray-400 font-medium space-y-2">
            <li>
              <a href="/" class="relative group inline-block text-[#80d0c7]">
                Home
                <span
                  class="absolute left-0 bottom-0 w-0 h-[2px] bg-[#80d0c7] transition-all duration-300 ease-in-out group-hover:w-full"
                ></span>
              </a>
            </li>
            <li>
              <a href="/" class="relative group inline-block text-[#80d0c7]">
                How it Works
                <span
                  class="absolute left-0 bottom-0 w-0 h-[2px] bg-[#80d0c7] transition-all duration-300 ease-in-out group-hover:w-full"
                ></span>
              </a>
            </li>
            <li>
              <a href="/" class="relative group inline-block text-[#80d0c7]">
                FAQ's
                <span
                  class="absolute left-0 bottom-0 w-0 h-[2px] bg-[#80d0c7] transition-all duration-300 ease-in-out group-hover:w-full"
                ></span>
              </a>
            </li>
            <li>
              <a href="/" class="relative group inline-block text-[#80d0c7]">
                Contact
                <span
                  class="absolute left-0 bottom-0 w-0 h-[2px] bg-[#80d0c7] transition-all duration-300 ease-in-out group-hover:w-full"
                ></span>
              </a>
            </li>
          </ul>
        </div>

        <div>
          <h2
            class="mb-6 text-xl font-bold tracking-wide text-gray-900 uppercase dark:text-gray-900"
          >
            Information
          </h2>
          <ul class="text-gray-500 dark:text-gray-400 font-medium space-y-2">
            <li>
              <a href="/" class="relative group inline-block text-[#80d0c7]">
                305-240-9671
                <span
                  class="absolute left-0 bottom-0 w-0 h-[2px] bg-[#80d0c7] transition-all duration-300 ease-in-out group-hover:w-full"
                ></span>
              </a>
            </li>
            <li>
              <a href="/" class="relative group inline-block text-[#80d0c7]">
                info@company.com
                <span
                  class="absolute left-0 bottom-0 w-0 h-[2px] bg-[#80d0c7] transition-all duration-300 ease-in-out group-hover:w-full"
                ></span>
              </a>
            </li>
          </ul>
        </div>

        <div>
          <button
            class="mb-6 text-sm border-2 border-[#80d0c7] px-4 py-2 rounded-xl bg-[#80d0c7] font-semibold
             text-gray-900 uppercase dark:text-white"
          >
          <select name="" id="">
            <option value="">English</option>
            <option value="">Hindi</option>
          </select>
           
          </button>
          <ul class="text-gray-500 dark:text-gray-400 font-medium space-y-2">
            <li>
              <a
                href="https://flowbite.com/"
                class="hover:underline text-[#80d0c7]"
              >
                Copyright © 2048 Topic Listing Center. All rights reserved.
              </a>
            </li>
            <li>
              <a
                href="https://tailwindcss.com/"
                class="hover:underline text-[#80d0c7]"
              >
                Design
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</footer>
