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
        Das Projekt „Favoriten zu Fuß“ widmet sich der qualitativen Aufwertung
        eines dicht bebauten Stadtgebiets im 10. Wiener Gemeindebezirk. Anders
        als bei einer Neuplanung steht hier nicht die Neugestaltung von
        Brachflächen im Mittelpunkt, sondern die Aktivierung und Verbesserung
        bestehender Infrastrukturen. Das Ziel ist ein lebendiges, durchgrüntes
        und fußgängerfreundliches Grätzel – klimaresilient, sicher und sozial
        vernetzt.
      </p>
    </div>
  </div>
  <div
    class="project shadow"
    on:pointerenter={() => ($district = 23)}
    on:pointerout={() => ($district = -1)}
  >
    <h2>Zam' Wachsen!</h2>
    <div class="content">
      <img src="1.png" alt="" />
      <p>
        ZamWachsen – Das neue Kulturherz Atzgersdorf (Universitätsprojekt TU
        Wien) Das Projekt „ZamWachsen“ ist ein universitärer Entwurf zur
        Umgestaltung eines Brachfelds in Atzgersdorf. Ziel ist die Schaffung
        eines lebendigen, grünen und kulturell aktiven Stadtteils. Ein zentrales
        „grünes Kreuz“ verbindet Wohnraum, Freiflächen und
        Gemeinschaftseinrichtungen miteinander. Bestehende Potenziale wie
        Grünflächen und Gewerbebauten werden integriert, während neue
        Verbindungen und Mobilitätsangebote die Erreichbarkeit und
        Lebensqualität im Quartier verbessern.
        <br />
        <br />

        <a target="_blank" href="ZamWachsen.pdf">Pdf anzeigen</a>
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
  .project a {
    pointer-events: all;
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
