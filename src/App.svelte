<script>
  import viteLogo from "/vite.svg";
  import Vienna from "./lib/Vienna.svelte";
  import Landing from "./lib/Landing.svelte";
  import Cv from "./lib/Cv.svelte";
  import Projects from "./lib/Projects.svelte";
  import Contact from "./lib/Contact.svelte";
</script>

<main>
  <Vienna />
  <Landing />
  <Cv />
  <Projects />
  <Contact />
</main>

<style>
  div {
    z-index: 10;
  }
</style>
