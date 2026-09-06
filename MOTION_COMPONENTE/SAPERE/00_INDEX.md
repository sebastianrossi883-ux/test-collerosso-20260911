# SAPERE — indice

Otto skill di motion design, **complete**: sono le cartelle originali, non una
selezione di file. Insieme ai reference, agli script e agli esempi che portano.

Se il tuo ambiente supporta le Agent Skills, caricale per nome. Altrimenti leggi
i file: `SKILL.md` e' sempre il punto di ingresso di ogni cartella.

## Ordine di lettura

| # | Skill | Leggila per |
|---|---|---|
| 1 | `cinematic-gsap-lenis-motion-system/` | La regia: init order, token di curve e durate, reveal, parallax, pin, cursore, coreografia, QA finale. Porta anche `REFERENCES.md` e una pagina demo funzionante in `demo/` |
| 2 | `gsap-core/` | Tween, stagger, `gsap.matchMedia()` per responsive e reduced-motion |
| 3 | `gsap-timeline/` | Timeline, position parameter, sequenze incastrate |
| 4 | `gsap-scrolltrigger/` | `start`/`end`, scrub, pin, `refresh()`, cleanup |
| 5 | `gsap-plugins/` | SplitText, Flip, Observer, ScrollSmoother, CustomEase, Draggable, Inertia — dalla 3.13 sono tutti gratuiti |
| 6 | `gsap-utils/` | `clamp`, `mapRange`, `random`, `snap`, `wrap`: servono per adattare la matematica del componente al numero reale di elementi del sito |
| 7 | `gsap-performance/` | Solo transform, batching, niente layout thrashing |
| 8 | `ui-animation/` | Animazione in CSS puro e reverse engineering: keyframes, transizioni, curve, `clip-path`, scroll-driven CSS. Porta 19 reference e 3 script |

Extra:
- `llms.txt` — l'indice ufficiale GreenSock delle skill GSAP.
- `esempio-vanilla/` — esempio GSAP in HTML statico con tag `<script>`, lo stesso
  stack di questi siti.

## Quanto serve ognuna, misurato

Contato sui 269 componenti del catalogo da cui vengono le due regie di questo sito:

| Skill | Componenti che la richiedono |
|---|---|
| `ui-animation` (CSS) | 239 su 269 — e **78 girano solo in CSS, senza GSAP** |
| `gsap-performance` | 224 |
| `gsap-core` | 208 |
| `gsap-timeline` | 172 |
| `gsap-scrolltrigger` | 109 |
| `gsap-plugins` | 92 — Observer 41, Flip 30, ScrollSmoother 25, SplitText 13 |
| `gsap-utils` | 66 |

Se il componente che ti e' toccato e' uno dei 78 in CSS puro, il tuo documento
principale e' `ui-animation/`, non il primo.

## Due avvertenze, non filtri

Le cartelle sono complete: niente e' stato tolto. Ma due cose vanno lette col
contesto giusto, perche' questi siti sono **HTML statico con tag `<script>`**:

- Alcuni reference di `ui-animation/` (`component-patterns`, `contextual-animations`,
  `code-output`, `gesture-drag`, `svg-animation`) mostrano gli esempi in
  framer-motion / React. **La matematica e le curve valgono lo stesso**; l'API no.
  Prendi il timing, non il `<motion.div>`.
- `references/spring-animations.md` insegna le molle, ma
  `cinematic-gsap-lenis-motion-system` dice esplicitamente di evitare rimbalzi ed
  elastici su questo tipo di sito. Se i due si contraddicono, **comanda
  cinematic-gsap-lenis**: il tono e' alta cucina, non giocattolo.

## Limite di autorita'

Le skill danno il **come**: l'API corretta, il cleanup, le prestazioni, il gusto.
Non danno la firma di questo sito ne' i suoi numeri: quelli vengono dai due
componenti in `MOTION_COMPONENTE/`. Se una skill suggerisce un valore e il
componente ne usa un altro, **comanda il componente**.
