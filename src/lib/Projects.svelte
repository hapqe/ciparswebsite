<script>
  import download from "../assets/dl.svg";
  import { district } from "./Vienna.svelte";
</script>

<main>
  <h1>Meine Projekte</h1>

  <div
    class="project shadow"
    on:pointerenter={() => ($district = 10)}
    on:pointerout={() => ($district = -1)}
  >
    <h2>Plakate für eine Initiative in Favoriten</h2>
    <div class="content">
      <img src="0.png" alt="" />
      <p>
        Willkommen auf meinem Portfolio. Hier finden Sie eine Auswahl meiner
        Projekte zu Stadtplanung, nachhaltiger Entwicklung und partizipativer
        Gestaltung. Ich kombiniere analytische Methoden mit kreativen
        Lösungsansätzen, um lebenswerte Räume für morgen zu schaffen.
      </p>
    </div>
  </div>
  <div class="project shadow">
    <h2>Projekt XY</h2>
    <div class="content">
      <img src="1.png" alt="" />
      <p>
        Willkommen auf meinem Portfolio. Hier finden Sie eine Auswahl meiner
        Projekte zu Stadtplanung, nachhaltiger Entwicklung und partizipativer
        Gestaltung. Ich kombiniere analytische Methoden mit kreativen
        Lösungsansätzen, um lebenswerte Räume für morgen zu schaffen.
      </p>
    </div>
  </div>
</main>

<style>
  h2 {
    font-weight: 400;
    margin: 0;
    margin-bottom: 0.5rem;
    pointer-events: all;
  }
  .project {
    pointer-events: all;
    width: 40rem;
    max-width: calc(100svw - 8rem);
    padding: 1rem;
  }
  .project * {
    pointer-events: none;
  }
  .project img {
    width: 21rem;
  }
  .project .content {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    gap: 1rem;
  }
  .project img {
    max-width: 100%;
  }
  .project p {
    margin-top: 0;
    width: 18rem;
  }
  div {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;

    justify-content: center;
    align-items: center;
    max-width: calc(100svw - 2 * var(--space) - 2rem);
  }
  main {
    padding: var(--space);

    height: fit-content;
    display: flex;
    flex-direction: column;
    gap: 3rem;
    max-width: 100svw;
  }
  h1 {
    color: white;
    mix-blend-mode: difference;
  }
</style>
