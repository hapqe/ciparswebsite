<script>
  import download from "../assets/dl.svg";
  import { district } from "./Vienna.svelte";
</script>

<main>
  <h1>Mein Lebenslauf</h1>
  <div>
    <a on:pointerenter={() => ($district -= 1)} class="box" href=""
      ><img src={download} alt="download icon" /> Lebenslauf herunterladen</a
    >
  </div>
</main>

<style>
  div {
    display: flex;
    flex-direction: column;

    justify-content: center;
    align-items: center;
  }
  main {
    padding: var(--space);

    height: fit-content;
    mix-blend-mode: difference;
    color: white;
    background: white;
  }
  a {
    padding: 10px;
    background: black;
    font-weight: 600;
    display: flex;

    justify-content: center;
    align-items: center;
  }
  a:not(:hover) {
    color: white;
  }
  a:hover * {
    filter: invert(1);
    color: unset !important;
  }
  img {
    height: 24px;
    margin-right: 3px;
  }
</style>
