<script lang="ts">
  import Accordation from "./accordation.svelte";
  interface faq {
    question: string;
    answer: string;
  }

  const Faq: faq[] = [
    {
      question: "What is Topic Listing?",
      answer: `Topic Listing is free Bootstrap 5 CSS template. You are not allowed to
      redistribute this template on any other template collection website
      without our permission. Please contact TemplateMo for more detail. Thank
      you.`,
    },
    {
      question: "How to find a Topic?",
      answer: `You can search on Google with keywords such as templatemo portfolio,
       templatemo one-page layouts, photography, digital marketing, etc.`,
    },
    {
      question: "What is Topic Listing?",
      answer: `You can modify any of this with custom CSS or overriding our default
       variables. It's also worth noting that just about any HTML can go within the. 
       accordion-body, though the transition does limit overflow.`,
    },
  ];
</script>

<div class="w-full bg-white md:flex justify-center">
  <div class="w-full md:w-1/2 flex flex-col justify-center items-center">
    <h1 class="items-start text-[40px] md:text-[50px] p-5 font-bold">
      Frequently Asked <br /> Questions
    </h1>
    <img src="images/faq_graphic.jpg" alt="" class="w-3/5" />
  </div>

  <div class="w-full md:w-1/2 flex flex-col justify-center top-1/2 text-center md:text-start">
    {#each Faq as items}
      <Accordation question={items.question} answer={items.answer} />
    {/each}
  </div>
</div>
