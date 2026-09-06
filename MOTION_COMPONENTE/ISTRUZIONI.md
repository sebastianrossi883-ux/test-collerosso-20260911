# Il componente di questo sito

In questa cartella c'e' il **codice sorgente** di due componenti veri. Non
sono esempi da guardare: sono la matematica da cui prendere il movimento di
questo sito. Leggi il codice, capisci come funziona, e integralo.

## 1. La regia delle FOTOGRAFIE — Rotated Revealer — variante index5.html

Cartella: `1_regia_immagini_RotatedRevealers-master/`
**La variante scelta e' `index5.html`** — il suo codice sta in `js/demo5.js`
Cosa fa: Demos of the tutorial on how to create and animate a rotated overlay, or "reveal" element for interesting page transition effects.


Nella cartella ci sono anche le altre 4 varianti dello stesso componente: guarda quella indicata, non le altre. Sono effetti diversi, ognuna con il suo codice.

Questa e' la coreografia che governa le immagini della pagina. Leggi il suo
JavaScript e il suo CSS, prendine la matematica - le curve, i tempi, i
rapporti, il modo in cui calcola le posizioni - e falla lavorare sulle
fotografie del sito.

**Nessuna fotografia resta ferma.** Contale prima di consegnare: se la pagina
ha dieci immagini, dieci devono muoversi.

## 2. La regia di CONTORNO — Animations for Sticky Sections — variante index13.html

Cartella: `2_regia_contorno_StickySections-main/`
**La variante scelta e' `index13.html`**
Cosa fa: Some ideas of how sticky sections can be animated while exiting the viewport.

Questa vale per tutto quello che non e' una fotografia: titoli, testi,
passaggi fra le sezioni, elementi di interfaccia. Dove sta meglio lo decidi
tu leggendo il codice e guardando la pagina - se il meccanismo non ha senso
su un titolo, portalo sulle sezioni o sui passaggi. L'unico vincolo e' che
non deve prendersi le fotografie: quelle hanno gia' la loro regia.

## Se i due litigano, comanda il primo

I due componenti nascono da demo diverse e possono avere temperamenti
diversi: uno lento e ampio, l'altro secco e nervoso. Il carattere del sito lo
detta **la regia delle fotografie**: velocita', curve, respiro sono i suoi.

La regia di contorno e' subordinata. Prendine quello che ci sta. Se il suo
modo di muoversi va contro il primo, usane solo la parte che regge - una
curva, un rapporto, un modo di calcolare - oppure **lasciala perdere del
tutto** e scrivilo nel messaggio di consegna. Un sito con una regia sola
fatta bene vale piu' di due che si pestano i piedi.

Questa e' una tua decisione, non una mia: la prendi dopo aver letto tutti e
due i sorgenti e guardato la pagina.

## Cosa prendere e cosa NON prendere

Del componente prendi **la matematica**: le curve, i tempi, gli sfalsamenti,
i ritagli, il modo in cui calcola le posizioni e i rapporti fra gli elementi.
Quella e' la cosa che vale, ed e' scritta da chi il mestiere lo sa fare.

**Non prendere niente di quello che il componente MOSTRA.** Le sue fotografie,
i suoi testi, i suoi caratteri, i suoi colori e le sue spaziature sono
materiale da dimostrazione: non c'entrano niente con questo sito e non devono
comparirci. Il sito ha gia' le proprie fotografie, i propri testi, il proprio
carattere e la propria palette, e restano quelli.

Quindi il lavoro e' un ADATTAMENTO, non un trapianto: la coreografia del
componente deve girare sul contenuto del sito. Se il componente muove sei
riquadri e il sito ha quattro fotografie, la matematica si adatta a quattro.
Se il componente vuole un contenitore che il sito non ha, lo crei attorno a
quello che c'e' senza cambiare quello che si vede da fermi.

## Il tono: e' un ristorante da guida Michelin

Questo non e' un sito qualunque. La categoria e' alta cucina, e il movimento
deve essere all'altezza: lento dove serve, preciso, mai appariscente. Niente
rimbalzi, niente elastici, niente effetti che si fanno notare al posto della
fotografia. Il movimento accompagna, non si esibisce.

Se una parte del componente, adattata, risultasse volgare o chiassosa su un
sito di questo tono, lasciala fuori e tieni il resto.

## Tutto si attiva con lo SCORRIMENTO

Il sito e' una pagina che si scorre, e il movimento deve nascere da li'.
Nessuna animazione parte da un clic, da un pulsante o da una freccia: chi
guarda scorre e le cose accadono.

**Quasi tutte queste demo, nella loro pagina originale, partono da un clic**:
sono nate come passaggi fra pagine. Non e' un problema e non e' un motivo per
scartarle. La matematica e l'innesco sono due cose separate: prendi le curve,
i ritagli, i tempi e i rapporti del componente, e legali allo scorrimento con
ScrollTrigger o con un IntersectionObserver.

Vale anche per i componenti che nella demo si attivano al passaggio del mouse:
sul telefono quel gesto non esiste, quindi l'ingresso resta comunque lo
scorrimento. Un effetto al passaggio del mouse puo' restare in piu', mai da
solo.

## Come integrarli

- Il sorgente e' **eseguibile, non illustrativo**: niente riassunti, niente
  versioni semplificate, niente segnaposto.
- Il componente porta il suo DOM: adattalo alla struttura del sito, non il
  contrario.
- Librerie: la regia delle fotografie gira su **css**, quella di
  contorno su **css**. Quelle che il sito non ha gia', caricale
  da CDN.
- **Non cambiare il disegno del sito**: colori, caratteri, spaziature e
  posizioni restano quelli. Qui si aggiunge il movimento, non un altro sito.
- Questa cartella `MOTION_COMPONENTE/` e' materiale di lavoro - componenti e
  `SAPERE/` compresi: quando hai finito **cancellala tutta**, non deve restare
  nel sito consegnato.

## Il sapere: la cartella `SAPERE/`

Accanto ai componenti c'e' `SAPERE/`: otto skill di motion design intere, filtrate
per HTML statico. Parti da `SAPERE/00_INDEX.md`.

Servono per il **come** - l'API giusta, il cleanup, le prestazioni. La firma di
questo sito non e' li' dentro: e' nei due componenti qui sopra. Se una skill
suggerisce un valore e il componente ne usa un altro, **comanda il componente**.

Quando hai finito, `SAPERE/` si cancella col resto di `MOTION_COMPONENTE/`.

## Prima di consegnare: nove controlli

Non sono indicazioni di gusto: sono i modi in cui una pagina animata si rompe.

1. **Il sito ha GIA' un motore.** Arriva con Lenis istanziato, GSAP, ScrollTrigger,
   SplitText e CustomEase da CDN, e circa sei firme `mk-*` al lavoro. Il tuo lavoro
   si aggiunge, non duplica. **Non istanziare mai un secondo smooth scroll:** 113
   componenti su 269 ne portano uno proprio, 58 dei quali scritto a mano con un
   `lerp` dentro un `requestAnimationFrame`, che non ha un nome da cercare.
   Toglilo e aggancia la sua matematica al Lenis che c'e' gia'.
   **Gli elementi con una classe `mk-*` sono OCCUPATI. Non toccarli.**
   Ne' la classe (toglierla non spegne il motore: lo lascia acceso senza niente
   da leggere, e quella sezione smette di muoversi), ne' l'elemento stesso con
   una tua animazione. Due timeline che scrivono sulla stessa proprieta' dello
   stesso nodo a ogni frame producono uno sfarfallio visibile: e' successo
   davvero, su un `<h1 class="mk-hero">` animato da tutti e due.
   Lavora **su altri elementi**: un contenitore che non ha firme, un fratello,
   un figlio che il motore non tocca. In ogni sezione c'e' spazio libero.
   Se davvero non ce n'e', lascia stare quella sezione e dillo nel resoconto.
2. Niente ScrollTrigger sulla prima schermata: entra al caricamento.
   **E mai uno `scrub` sulla hero.** Uno scrub ha bisogno di corsa fra `start` e
   `end` per completarsi; sulla prima schermata quella corsa non esiste e
   l'animazione resta ferma a meta'. E' successo: un `clip-path` bloccato a
   `inset(17.8% 31.6% round 238px)` che ha lasciato la hero ritagliata a
   pastiglia. Sulla hero si usa una timeline al `load`, senza scrub.
3. Mai animare `height`, `width`, `margin`, `padding`, `display`. Solo `transform`,
   `opacity`, `filter`, `clip-path`. E' la prima causa dei testi accavallati.
4. `prefers-reduced-motion`: pagina ferma e completa.
5. Testo spezzato: `aria-label` con la frase intera sull'elemento, maschere `aria-hidden`.
6. Se il JavaScript non parte, il contenuto resta visibile. Mai pagina bianca.
7. `ScrollTrigger.refresh()` dopo font e immagini, o le righe restano misurate male.
8. Gli elementi in fondo pagina: se l'innesco cade oltre lo scorrimento massimo non
   scatta mai. Scorri fino in fondo, niente deve restare a opacita' zero.
9. Sotto i 768px pin e scorrimento orizzontale si disattivano, e si riattivano se
   la finestra torna larga.

## Nel messaggio di consegna, dichiara due cose

Una riga per **ciascuno** dei due componenti: che cosa gli hai preso e su quali
elementi del sito l'hai messo. Se da uno dei due non hai preso niente, scrivilo -
e' una decisione legittima (vedi "se i due litigano"), ma va detta, non nascosta
dietro una funzione che porta il suo nome e dentro fa un'altra cosa.

E l'elenco degli elementi su cui hai messo le tue animazioni. Se fra questi
compare un elemento che porta gia' una classe `mk-*`, e' un errore: correggilo
prima di consegnare, non dopo.

---
Accoppiata `RotatedRevealers-master#index5.html+StickySections-main#index13.html` — pescata fra 31122 ancora libere.
