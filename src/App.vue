<script>
import DigitalClock from "./components/DigitalClock.vue";

export default {
  components: {
    DigitalClock: DigitalClock,
  },
};
</script>

<template lang="">
  <main class="container">
    <section class="clock"><DigitalClock /></section>
    <section class="search">
      <form action="https://www.google.com/search" method="get">
        <input name="q" type="text" placeholder="Buscar" />
      </form>
    </section>
    <section class="section1">
      <h2>Media</h2>
      <p><a href="https://web.whatsapp.com/">WhatsApp</a></p>
      <p><a href="https://www.facebook.com/">Facebook</a></p>
      <p><a href="https://tweetdeck.twitter.com/">Twitter</a></p>
      <p><a href="https://www.youtube.com/">Youtube</a></p>
      <p><a href="https://www.instagram.com/?hl=es-la">Instagram</a></p>
      <p><a href="https://discordapp.com/activity">Discord</a></p>
    </section>

    <section class="section2">
      <h2>Work</h2>
      <p><a href="https://github.com/">GitHub</a></p>
      <p><a href="https://docs.google.com/document/u/0/">GoogleDocs</a></p>
      <p><a href="https://mail.google.com/mail/u/0/">Gmail</a></p>
      <p><a href="https://outlook.live.com/owa/">Hotmail</a></p>
      <p><a href="https://devdocs.io">Programing docs</a></p>
      <p>
        <a href="https://www.onenote.com/notebooks?auth=2&nf=1">One note</a>
      </p>
      <p>
        <a href="https://chat.openai.com/chat">ChatGPT</a>
      </p>
      <p>
        <a
          href="https://www.notion.so/6d979632c4874dd88cb9dd79be3b1fdf?v=4bc440859532467e9df43e3ae7ab6d6d"
          >Notion</a
        >
      </p>
    </section>

    <section class="section3">
      <h2>Stuff</h2>
      <p><a href="http://logs.tf/">Logs.tf</a></p>
      <p><a href="https://www.teamfortress.tv/">TFTV</a></p>
      <p><a href="https://www.twitch.tv/">Twitch</a></p>
    </section>
  </main>
</template>

<style>
.container {
  display: grid;

  grid-template-columns: 1fr;
  grid-template-rows: 1.3fr 0.1fr 0.5fr 0.5fr 0.5fr;
  justify-content: center;
  justify-items: center;
  gap: 50px 0;
  grid-template-areas:
    "clock"
    "search"
    "section1"
    "section2"
    "section3";
}
p {
  text-align: center;
}
p a {
  color: white;
  text-align: center;
  text-decoration: none;
}

h2 {
  font-size: 40px;
  font-weight: bold;
  color: white;
  text-align: center;
}

.clock {
  grid-area: clock;
}

.section1 {
  grid-area: section1;
}

.section2 {
  grid-area: section2;
}

.section3 {
  grid-area: section3;
}

.search {
  align-self: center;
  border-radius: 30px;
  grid-area: search;
  padding-bottom: 50px;
}

input {
  width: 100%;
  height: 100%;
  border-radius: 10px;
  border: none;
  padding: 10px;
  font-size: 20px;
  text-align: center;
  background-color: black;
  color: white;
  opacity: 0.7;
}
section {
  color: white;
}
.section1,
.section2,
.section3 {
  background-color: black;
  opacity: 0.7;
  width: 40%;
  padding: 20px;
  border-radius: 20px;
}

@media (min-width: 1440px) {
  .container {
    display: grid;
    grid-auto-columns: 1fr;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 0.1fr 1fr;
    gap: 0px 0px;
    justify-content: space-around;
    grid-template-areas:
      ". clock ."
      ". search ."
      "section1 section2 section3";
  }

  .section1 {
    justify-self: end;
    grid-area: section1;
  }

  .section2 {
    grid-area: section2;
  }

  .section3 {
    justify-self: start;
    grid-area: section3;
  }
}
</style>
