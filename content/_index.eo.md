---
title: 
toc: false
---

<script type="module">
  import { animate, scrambleText } from 'https://esm.sh/animejs';

  const namen = [
    "Amsterdamse Studentenvereniging voor Interlinguïstiek",
    "Amsterdam Study Association for Interlinguistics",
    "Amsterdama Studentasocio por Interlingvistiko"
  ];

  const animatieDuur = 1200;
  const pauze = 10000;
  let index = 2;

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

Amsterdama Studentasocio por **Interlingvistiko**
{class="main-quote transition"}
---

...

