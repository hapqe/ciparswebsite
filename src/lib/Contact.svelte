<script>
  import mail from "../assets/mail.svg";
  import phone from "../assets/phone.svg";
  import location from "../assets/location.svg";
  import { district } from "./Vienna.svelte";
</script>

<main>
  <h1>Kontakt</h1>
  <div>
    <a
      href="mailto:vanesa.cipar@gmail.com"
      on:pointerenter={() => ($district -= 1)}
      ><img src={mail} alt="mail icon" /> vanesa.cipar@gmail.com</a
    >
    <a href="tel:+436609769510" on:pointerenter={() => ($district -= 1)}
      ><img src={phone} alt="phone icon" /> +43 6609769510</a
    >
    <a
      target="_blank"
      href="https://maps.app.goo.gl/twhm4fggkSr9iYN69"
      on:pointerenter={() => ($district = 11)}
      on:pointerout={() => ($district = -1)}
      ><img src={location} alt="location icon" /> Fuchsröhrenstr. 39/1/4, 1110 Wien</a
    >
  </div>
</main>

<style>
  div {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;

    justify-content: center;
    align-items: center;
    max-width: calc(100svw - 2 * var(--space) - 2rem);

    gap: 2rem;
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
    color: black;
    font-weight: 600;
    display: flex;

    justify-content: center;
    align-items: center;
  }
  img {
    height: 24px;
    margin-right: 5px;
  }
  @media only screen and (max-width: 500px) {
    div {
      justify-content: left;
      align-items: center;
    }
  }
</style>
