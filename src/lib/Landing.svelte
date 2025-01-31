<script>
  import me from "../assets/me.png";
  import { district } from "./Vienna.svelte";
</script>

<main>
  <div>
    <h1>
      Vanesa <span class="box">Cipar</span>
    </h1>
    <h3>
      Studentin in
      <a
        class="box"
        target="_blank"
        href="https://www.tuwien.at/studium/studienangebot/bachelorstudien/raumplanung-und-raumordnung"
        on:pointerenter={() => ($district -= 1)}
      >
        Raumplanung und Raumordnung
      </a>
      an der
      <a
        class="box"
        target="_blank"
        on:pointerenter={() => ($district = 4)}
        on:pointerout={() => ($district = -1)}
        href="https://tuwien.ac.at"
      >
        TU Wien
      </a>
    </h3>
    <img id="me" style="width: 200px;" src={me} alt="" />
  </div>

  <p>
    Willkommen auf meinem Portfolio. Hier finden Sie eine Auswahl meiner
    <span class="box light">Projekte</span> zu
    <span class="box light">Stadtplanung</span>, nachhaltiger Entwicklung und
    partizipativer Gestaltung. Ich kombiniere analytische Methoden mit kreativen
    Lösungsansätzen, um <span class="box light">lebenswerte Räume</span> für morgen
    zu schaffen.
  </p>
</main>

<style>
  .box {
    background: white;
    color: black;
  }
  div * {
    mix-blend-mode: difference;
  }
  #me {
    mix-blend-mode: normal;
  }
  main {
    padding: var(--space);
    display: flex;
    flex-direction: column;

    justify-content: space-between;

    height: calc(100svh - 2 * var(--space));
    color: white;
  }
  h1 {
    color: white;
  }
  a {
    cursor: pointer;
    mix-blend-mode: difference;
    text-decoration: underline;
  }
  h3 {
    width: fit-content;
    font-weight: 300;

    transition: all, 100ms;
  }
  p {
    width: 400px;
    padding: 1rem;
    max-width: calc(100svw - 2 * var(--space) - 2rem);
    font-weight: 400;
    mix-blend-mode: difference;
  }
</style>
