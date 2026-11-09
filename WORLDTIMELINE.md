---
title: World Timeline
---

<style>

  html { overflow-x: hidden; }
  
  .timeline {
    --line: #444;
    --line-x: 30%;
    position: relative;
    max-width: 960px;
    margin: 2rem auto;
    padding: 0;
  }

  /* The single line down the middle */
  .timeline::before {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: var(--line-x);
    width: 4px;
    margin-left: -2px;
    background: var(--line);
    z-index: 1;
  }

  .era::before {                 /* NEW: the full-width colored box */
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: 50%;
    width: 100vw;
    margin-left: -50vw;
    background: var(--era-color);
    border-top: 2px solid rgba(0, 0, 0, 0.15);
    border-bottom: 2px solid rgba(0, 0, 0, 0.15);
    z-index: 0;
  }
  
  /* Large colored era boxes */
  .era {
    position: relative;
    margin: 0 0 2.5rem;
    padding: 1.5rem 0 1rem;
  }

  .era-title {
    position: relative;
    z-index: 3;
    width: calc(var(--line-x) * 2);   /* centers the text on the line */
    margin: 0rem 0 1.5rem;         /* position relative to the rest of the era box */
    padding: 0.8rem 0;
    background: #000;
    color: #fff;
    font-size: 1.25rem;
    font-weight: 700;
    text-align: center;
    box-shadow: 0 0 0 100vmax #000;   /* stretches the black out to the edges of the page */
    clip-path: inset(0 -100vmax);     /* keeps the stretch horizontal only */
  }

  .era-dates {
    display: block;
    font-size: 0.8rem;
    font-weight: 400;
    opacity: 0.8;
  }

  /* One row = label (left) | line | details (right) */
  .entry {
    position: relative;
    z-index: 2;
    display: grid;
    grid-template-columns: calc(var(--line-x) - 1.25rem) 1fr;
    column-gap: 2.5rem;
    row-gap: 0.7rem;
    margin-bottom: 1.5rem;
  }

  .entry .label {
    grid-column: 1;
    text-align: right;
    font-weight: 700;
    font-size: 1.1rem;
    color: #1a1a1a;
  }

  .entry .label   { padding-left: 1rem; }   /* NEW: add to your existing label rule */
  .entry .details { padding-right: 1rem; }  /* NEW: add to your existing details rule */

  .entry .label small {
    display: block;
    font-weight: 400;
    font-style: italic;
  }

  .entry .details::before {
  content: "–";
  position: absolute;
  left: 0;
  top: 0;
  }
  
  .entry .details {
    grid-column: 2;
    position: relative;
    padding-left: 1.2em;
    text-align: left;
    color: #1a1a1a;
    line-height: 1.45;
  }

  /* Dot on the line for each entry */
  .entry::after {
    content: "";
    position: absolute;
    top: 0.45rem;
    left: var(--line-x);
    width: 14px;
    height: 14px;
    margin-left: -7px;
    background: #fff;
    border: 3px solid var(--line);
    border-radius: 50%;
  }

  /* Era colors – change these freely */
  .era-creation        { --era-color: #cc9f86; }
  .era-divinity         { --era-color: #f6f2c4; }
  .era-myth      { --era-color: #6a359a; } 
  .era-man-1             { --era-color: #c57573; }
  .era-succession      { --era-color: #00c7c5; }
  .era-lost          { --era-color: #6d6d6d; }
  .era-man-2             { --era-color: #b54e4c; }
  .era-fear             { --era-color: #5ba468; }
  .era-seraphim-war             { --era-color: #ce75aa; }
  .era-grand-empire             { --era-color: #ddcc22; }
  .era-man-3             { --era-color: #a92124; }

  @media (max-width: 600px) {
    .entry { column-gap: 1.6rem; font-size: 0.9rem; }
    .era-title { font-size: 1rem; }
  }
</style>

# Timeline
A summarized record of recorded history, compiled from countless sources and recorded in the Orotheca and other libaries. Dates are demarcated in the common Eruption centered calendar, suffixes BE and AE for Before and After Eruption.

<div class="timeline">

<div class="era era-creation">
<div class="era-title">Era of Creation<span class="era-dates"> Prehistory, known only from the brave few who have asked Phanes directly </span></div>
  
<div class="entry">
  <div class="label">The Beginning</div>
    <div class="details">Phanes began in the Center</div>
</div>

<div class="entry">
  <div class="label">The First Day</div>
    <div class="details">Phanes spoke light into existence. With the first light came space for light to travel in, and time for light to travel through</div>
    <div class="details">Phanes spoke the heavens into existence, in all their divine glory</div>
</div>

<div class="entry">
  <div class="label">The Second Day</div>
    <div class="details">Phanes journeyed the width and breadth of His heavens</div>
    <div class="details">Phanes returned to the Center, and there he spoke Phanelar into being</div>
</div>

<div class="entry">
  <div class="label">The Third Day</div>
    <div class="details">Phanes created Pontus and Ourea, the first gods</div>
    <div class="details">Ourea gifted Phanelar the land, and so space was ordered</div>
    <div class="details">Pontus gifted Phanelar the sea, and so time was ordered</div>
</div>

<div class="entry">
  <div class="label">The Fourth Day</div>
    <div class="details">Phanes called the Continent forth from the sea and land</div>
    <div class="details">Phanes created the Sky Forge in the center of the Continent</div>
    <div class="details">From the heavens, the land, and the sea, Phanes crafted bodies for himself, Ourea, and Pontus</div>
  <div class="details">Phanes created the Depths and the Clouds</div>
    <div class="details">Phanes created the First Divine Artefact in the Sky Forge, the Crown of Logos</div>
    <div class="details">Phanes distilled his authority into the Crown of Logos, and in doing so became able to inhabit his corporeal body, as well as exercise his authority, simultaneously </div>
</div>

<div class="entry">
  <div class="label">The Fifth Day</div>
    <div class="details">Phanes created Ilmola to govern the sky, and run the Sky Forge</div>
    <div class="details">Phanes created Ephialtes and Etzel to watch over life and order respectively</div>
    <div class="details">Phanes created Wodan, Nyxos, and Set-Hyst to oversee the three aspects of death</div>
    <div class="details">Phanes created Dietrich, Ebisu, and Babalon to rule heroism, fortune, and love</div>
    <div class="details">Phanes created Minerva to preside over magic and wisdom</div>
    <div class="details">Phanes created the World Flora to facilitate the circulation of magic through Phanelar</div>
</div>

<div class="entry">
  <div class="label">The Sixth Day</div>
    <div class="details">Phanes and Ephialtes together created the first life: the Unfired</div>
    <div class="details">Phanes placed the newborn gods and their authorities inside the Unfired, and so all the gods were anchored to Phanelar</div>
    <div class="details">Ephialtes was tasked with creating new life, and so flora and fauna were called forth, and they flowed over Phanelar in abundance</div>
</div>

</div>

<div class="era era-divinity">
  <div class="era-title">Era of Divinity<span class="era-dates">When the Gods walked freely</span></div>
  
  <div class="entry">
    <div class="label">The Age of The Divine</div>
    <div class="details">The newborn gods lived for a time in peace, each presiding over their domain</div>
    <div class="details">Ephialtes, Etzel, and Minerva combined their powers to create the first spirits</div>
    <div class="details">The three gods placed these spirits in bodies of stone and clay, creating the giants</div>
    <div class="details">Phanes disapproved of the actions of his Children, and renounced Minerva's authority, casting her into the bowels of the Depths. A cavernous maw was left in her wake</div>
    <div class="details">Phanes placed Minerva's authority into an owl. This owl would be given the name Koios</div>
  </div>
  <div class="entry">
    <div class="label">The Little Age of Creation</div>
    <div class="details">Phanes created the Seraphim to ensure the gods would not disobey further instructions</div>
    <div class="details">Phanes created humans, and allowed his children to create beings of similar stature</div>
    <div class="details">Phanes, wary of the power held by his children and the heavens through which he had long ago journeys, tasked Ilmola to create the Lintukoto, a barrier to separate the Center from the heavens </div>
  </div>
  
</div>

<div class="era era-myth">
  <div class="era-title">Era of Myth<span class="era-dates">The times of mythologies</span></div>
  
  <div class="entry">
  <div class="label">Human Mythology</div>
    <div class="details">Humans came into being as the first mortals on the island of Eden, it's steep cliffs overlooking a vast sea</div>
    <div class="details">The many gods vied for control over the humans, and though some would follow others, most chose to follow Phanes</div>
    <div class="details">One day, a human named Madave was gifted fire by Phanes</div>
    <div class="details">Madave used this fire to walk the caves beneath the island. He and his cohort followed the flame until they emerged into a pristine land, far from Eden</div>
  </div>

  <div class="entry">
  <div class="label">Firbolg Mythology</div>
    <div class="details">The third of three giants was Seppo Sampo. Seppo Sampo was a curious giant who found himself pulled to the both, while his brothers traveled south</div>
    <div class="details">Seppo Sampo found a bowl in the earth, Lehmien Koti. Inside the bowl was a herd of wild cattle. On the edges of the bowl was a pack of wolves</div>
    <div class="details">Unlike his brothers, Seppo Sampo was not strong, however he was cunning and wise</div>
    <div class="details">Seppo Sampo asked the wolves why they howled, to which the wolves replied "We hunger". Seppo Sampo then asked the wolves "Can you wait to eat", and they replied "No". Seppo Sampo then asked "Would you rather eat these cows now, and then starve, or would you follow me to a place where you will never starve?" The wolves conversed, before following Seppo Sampo</div>
    <div class="details">Seppo Sampo took the wolves to a nearby river. In the river, salmon leaped. He said, "Look here, all the meat you will need"</div>
    <div class="details">The wolves ate the salmon, and became the first bears</div>
    <div class="details">The god Ilmola looked down from on high, and saw Seppo Sampo's will and kindness. She granted Seppo Sampo a small portion of her authority, crowning him as an Ophanim</div>
    <div class="details">The cows Seppo Sampo had protected came to love him, and through their worship they became the Firbolg</div>
  </div>

  <div class="entry">
  <div class="label">Genasi Mythology</div>
    <div class="details">Pontus had long watched her siblings from her seas, and had decided that she would experience life on the land</div>
    <div class="details">Pontus surfaced at the mouth of a long river, and traveled north. Eventually she found herself on the edge of a rolling field, with a large plateau in the distance</div>
    <div class="details">She could not bring herself to step out of the waters, though she longed to see what lay across the horizon</div>
    <div class="details">In her sorrow, she shed four tears. These tears struck the land before her in succession, and birthed the first Water, Air, Fire, and Earth Genasi</div>
  </div>
  
</div>


<div class="era era-man-1">
  <div class="era-title">First Era of Man<span class="era-dates">15000 to 11000 BE</span></div>
  
  <div class="entry">
    <div class="label">15000 BE</div>
    <div class="details">Kingdoms of men began appearing across the Continent</div>
  </div>
  
  <div class="entry">
    <div class="label">13500 BE</div>
    <div class="details">Humans harnessed the power of magic and spread to the far corners of the Continent</div>
  </div>
  
  <div class="entry">
    <div class="label">11300 BE</div>
    <div class="details">The first Form Manifestation is discovered</div>
  </div>
</div>

<div class="era era-succession">
  <div class="era-title">The War of Succession<span class="era-dates">11000 BE to 10448 BE</span></div>
  <div class="entry">
    <div class="label">11000 BE</div>
    <div class="details">Ephialtes tricks Ilmola into creating three sets of Binding Chains</div>
  </div>

  <div class="entry">
    <div class="label">10950 BE</div>
    <div class="details">Ephialtes creates dragons. He then convinces the Seraphim to silently betray Phanes</div>
  </div>

  <div class="entry">
    <div class="label">10900 BE</div>
    <div class="details">Ephialtes ambushes Ourea and Pontus, shackling them with the Binding Chains</div>
    <div class="details">Ephialtes marches on Phanes' domain at the Eye of The World</div>
    <div class="details">Ephialtes demands fealty from the gods, and releases a massive army of dragons on the entire world</div>
  </div>

  <div class="entry">
    <div class="label">10899 BE</div>
    <div class="details">Ephialtes demands fealty from the gods</div>
    <div class="details">Ephialtes releases a massive army of dragons on Phanelar</div>
    <div class="details">Some gods yield to Ephialtes, while some side with Phanes.</div>
  </div>

  <div class="entry">
    <div class="label">10890 BE</div>
    <div class="details">The dragon armies pour down upon human civilization</div>
  </div>

  <div class="entry">
    <div class="label">10800 BE</div>
    <div class="details">The gods continue to battle each other, as Ephialtes uses Pontus and Ourea as shields to stop Phanes from destroying him</div>
  </div>

  <div class="entry">
    <div class="label">10700 BE</div>
    <div class="details">The dragons wipe the Continent clean of all human civilization, save for small pockets of survivors</div>
  </div>

  <div class="entry">
    <div class="label">10600 BE</div>
    <div class="details">Ephialtes forces Pontus to raise the sea levels, separating the Continent into three sections</div>
  </div>

  <div class="entry">
    <div class="label">10500 BE</div>
    <div class="details">Phanes faces Ephialtes personally, determined to end his son's rampage</div>
  </div>

  <div class="entry">
    <div class="label">10450 BE</div>
    <div class="details">Phanes and Ephialtes do battle, however the Seraphim ambush Phanes and rip the Crown of Logos from his head</div>
    <div class="details">Ephialtes dons the Crown of Logos and wills the creation of a perfect body for himself, which he then enters</div>
    <div class="details">Using the Crown, Ephialtes attempts to hijack the power of life and death from Phanes</div>
    <div class="details">Ilmola and Koios are able to steal the crown from Ephialtes and flee south</div>
  </div>
  
  <div class="entry">
    <div class="label">10448 BE</div>
    <div class="details">Ephialtes and Phanes clash as Ephialtes pursues Ilmola and Koios</div>
    <div class="details">Seeing no other option left, Phanes surges ahead of his son and dons the Crown for a final time</div>
    <div class="details">Phanes wills the Crown to shatter into pieces, and so it does. With the Crown's authority shattered, Phanes turns to deal with his rebellious son</div>
    <div class="details">Phanes then uses the final set of Binding Chains to seal Ephialtes to the ground</div>
    <div class="details">Ourea, even with his influence diminished, covers Ephialtes in a mountain range</div>
  </div>
  
</div>

<div class="era era-divinity">
  <div class="era-title">  <span class="era-dates">  </span></div>
  <div class="entry">
    <div class="label">  </div>
    <div class="details">  </div>
  </div>
  </div>

  
</div> 
