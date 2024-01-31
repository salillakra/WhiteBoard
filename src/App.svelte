<script>
  import "./app.css";
  import Header from "./lib/Header.svelte";
  import Body from "./lib/Body.svelte";
</script>

<Header />
<main class="flex justify-center">
  <section class="w-3/4 border border-red-500 min-h-[30rem] m-4">
    <Body />
  </section>
</main>
