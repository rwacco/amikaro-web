---
title: 
toc: false
---

<script type="module">
  import { animate, scrambleText } from 'https://esm.sh/animejs';

  const namen = [
    "Amsterdamse Studentenvereniging voor <b>Interlinguïstiek</b>",
    "Amsterdam Student Association for <b>Interlinguistics</b>",
    "Amsterdama Studentasocio por <b>Interlingvistiko</b>"
  ];

  const animatieDuur = 1200;
  const pauze = 10000;
  let index = 1;

  function transitie() {
    index = (index + 1) % namen.length;

    animate('.transition', {
        innerHTML: scrambleText({
            text: namen[index],
            duration: animatieDuur,
          }),
        loop: false,
        onComplete: () => {
          setTimeout(transitie, pauze);
        },
    });
  };

  
  setTimeout(transitie, pauze);
</script>

Amsterdam Student Association for **Interlinguistics**
{class="main-quote transition"}

...