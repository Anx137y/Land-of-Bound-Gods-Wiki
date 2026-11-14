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
  .era-myth      { --era-color: #bc43b6; } 
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

<div class="era era-lost">
  <div class="era-title">The Lost Millenia<span class="era-dates">10448 BE to 4000 BE</span></div>
  <div class="entry">
    <div class="details">The traitorous gods are punished, and the Seraphim are sealed beneath the earth in the far corners of the world</div>
  </div>

  <div class="entry">
    <div class="details">The dragon army is hunted to near extinction</div>
  </div>
  
  <div class="entry">
    <div class="details">Humans across Phanelar emerge from hiding and establish new primitive hunter-gatherer civilizations</div>
  </div>
  </div>

<div class="era era-man-2">
  <div class="era-title">Second Era of Man<span class="era-dates">4000 BE to 2650 BE</span></div>
  <div class="entry">
    <div class="label">4000 BE</div>
    <div class="details">The city-state of Othrys is established in the foothills of Mt. Othrys</div>
  </div>
  
  <div class="entry">
    <div class="label">3765 BE</div>
    <div class="details">The city of Ranshal is founded on the coast of the Settan Desert</div>
  </div>
  
  <div class="entry">
    <div class="label">3560 BE</div>
    <div class="details">Othryan explorers discover Hades' Maw in northwest Koktos</div>
  </div>
  
  <div class="entry">
    <div class="label">3498 BE</div>
    <div class="details">The Greman culture group in Phanehold establish early worship practices of various deities</div>
  </div>
  
  <div class="entry">
    <div class="label">3460 BE</div>
    <div class="details">The Gith civil war begins</div>
  </div>
  
  <div class="entry">
    <div class="label">3333 BE</div>
    <div class="details">The city of Babalonica is established on worship practices of Babalon. The city implements a government based on sexual competition</div>
  </div>
  
  <div class="entry">
    <div class="label">3320 BE</div>
    <div class="details">Greman tribes in the Orani forest region form a multi-clan alliance to face Ranshal invaders from the east</div>
  </div>
  
  <div class="entry">
    <div class="label">3316 BE</div>
    <div class="details">Followers of Wodan establish the Kingdom of Valhalk</div>
  </div>
  
  <div class="entry">
    <div class="label">3300 BE</div>
    <div class="details">Greman tribes in the Heim Basin found the Kingdom of the Heim</div>
  </div>
  
  <div class="entry">
    <div class="label">3260 BE</div>
    <div class="details">The Kenku warlord Odanaga begins the process of uniting Irihin's disparate tribes and cultures</div>
  </div>
  
  <div class="entry">
    <div class="label">3255 BE</div>
    <div class="details">An internal civil conflict leads to the fall of Othrys, with the polis itself reduced to little more than rubble</div>
    <div class="details">The Othryan people emigrate from their homeland</div>
  </div>
  
  <div class="entry">
    <div class="label">3250 BE</div>
    <div class="details">The two factions from Othrys found the city-states of Aria and Parthenos respectively</div>
  </div>
  
  <div class="entry">
    <div class="label">3210 BE</div>
    <div class="details">The Paxon culture group in Ourean found the twin kingdoms of Estcher and Brital</div>
  </div>
  
  <div class="entry">
    <div class="label">3200 BE</div>
    <div class="details">The Tepa culture group in Ourean founds the Kingdome of Espatcha on the slopes of Mt. Tepantli</div>
  </div>
  
  <div class="entry">
    <div class="label">3150 BE</div>
    <div class="details">Parthenos begins spreading its influence across the many small polis in the Mycea Archipelago</div>
  </div>
  
  <div class="entry">
    <div class="label">3120 BE</div>
    <div class="details">The Odanaga period ends in Irihin with the murder of the Emperor during a large scale slave revolt</div>
  </div>
  
  <div class="entry">
    <div class="label">3115 BE</div>
    <div class="details">The two hundred year long conflict between the Orani tribes and Ranshal ends with a mutual alliance and the establishment of the Kingdom of Orani</div>
  </div>

  <div class="entry">
    <div class="label">3100 BE</div>
    <div class="details">The elven villages surrounding the World Tree combine to form the great elven city of Sulgarde</div>
  </div>

  <div class="entry">
    <div class="label">3097 BE</div>
    <div class="details">The Kingdom of the Heim's expanded influence leads to a two-front conflict against kingdoms situated near Lake Fritz and Agnes respectively</div>
  </div>

  <div class="entry">
    <div class="label">3090 BE</div>
    <div class="details">Multiple tribes in the Red Forest flee south across the Sea of Phanes to avoid conquest by the Kingdome of the Heim</div>
    <div class="details">The refugee tribes from the Red Forest establish the Kingdom of Patrie on the southern shore of the Sea of Phanes</div>
  </div>

  <div class="entry">
    <div class="label">3000 BE</div>
    <div class="details">The Kingdom of the Hiem overextends its reach past Fjell Oglagnyr</div>
    <div class="details">The Kingdom of the Heim collapses from internal rebellions</div>
    <div class="details">The fractured states that had constituted the Kingdom of the Heim begin a long period of regular land wars, with territory trading hands frequently</div>
  </div>
  
  <div class="entry">
    <div class="label">2780 BE</div>
    <div class="details">Parthenos's expanded borders reach Babalonica, and the two states begin warring</div>
  </div>

  <div class="entry">
    <div class="label">2760 BE</div>
    <div class="details">The Golden Land's slow expansion reaches the borders of the polis of Aria</div>
    <div class="details">Intitial fighting between Aria and the Golden Land lasts two months, before Aria joins the Golden Land as a vassal state</div>
  </div>
  
  <div class="entry">
    <div class="label">2757 BE</div>
    <div class="details">Babalonica pushes Parthenos off their island, and proceed to liberate Parthenos' holdings in the Mycea Archipelago</div>
  </div>

  <div class="entry">
    <div class="label">2740 BE</div>
    <div class="details">The island of Optila establishes the Empire of Optila</div>
    <div class="details">The Empire of Optila conquer the Nine Isles in the Central Sea</div>
  </div>
  
  <div class="entry">
    <div class="label">2690 BE</div>
    <div class="details">Irihin unites under the Bugbear Emperor Hiro, who enacts an isolationist policy and cuts the island off from the outside world with a powerful spell</div>
  </div>

  <div class="entry">
    <div class="label">2650 BE</div>
    <div class="details">A wing of dragons resurfaces in the Great Desert</div>
    <div class="details">The dragon wing decimates the Kingdom of Espatcha, alongside every other established community in the Great Desert</div>
  </div>
  
  </div>


<div class="era era-fear">
  <div class="era-title">The Age of Fear<span class="era-dates">2650 BE to 1080 BE</span></div>
  <div class="entry">
    <div class="label">2600 BE</div>
    <div class="details">A dragon wing some 3000 dragons strong crosses the Kuitlapanomitl Mountains</div>
  </div>
  
  <div class="entry">
    <div class="label">2550 BE</div>
    <div class="details">Brital and Estcher unite to fend off the dragons</div>
    <div class="details">The cities and fields of Brital and Estcher are razed to the ground, but the peoples and governments survive</div>
  </div>
  
  <div class="entry">
    <div class="label">2548 BE</div>
    <div class="details">The dragons circumvent the Eye of The World, leaving the Empire of Optila unharmed</div>
  </div>

  <div class="entry">
    <div class="label">2542 BE</div>
    <div class="details">Parthenos is able to avoid being destroyed, as the forewarning of the slow-moving dragons let them evacuate into the expansive cave networks beneath the Othrys mountain range</div>
  </div>
  
  <div class="entry">
    <div class="label">2500 BE</div>
    <div class="details">A culture of fear pervades Phanelar, with nations hesitant to expand, rebuild, or even trade as fears of dragons claim the public mind</div>
    <div class="details">The Church of Phanes is founded, who quickly spread across Phanelar. Their teachings exacerbate and validate the fears of the public</div>
  </div>
  
  <div class="entry">
    <div class="label">1100 BE</div>
    <div class="details">Over a thousand years of peace has left governments disillusioned to the Church's fearmongering, and nations across Phanelar begin to trade and interact once more </div>
  </div>
  
  </div>

  
<div class="era era-seraphim-war">
  <div class="era-title">The Seraphim's Wars<span class="era-dates">1080 BE to 760 BE</span></div>
  <div class="entry">
    <div class="label">1080 BE</div>
    <div class="details">The nation of Valhalk pushes into the ancestral lands of the Goliaths</div>
    <div class="details">The Goliaths call on their guardian deity, the Seraphim Raphael, to protect them</div>
    <div class="details">Raphael dispatches an army of giants from Sal Jotna</div>
  </div>

  <div class="entry">
    <div class="label">1070 BE</div>
    <div class="details">The army of giants begins pushing Valhalk out of the Goliath's homeland. This causes Valhalk to evacuate north as the giants continue into the city of Eingenvar</div>
  </div>
  
  <div class="entry">
    <div class="label">1060 BE</div>
    <div class="details">Valhalk conquers Fjell Ensom and Fjell Oglagynr, relocating their capital to the valley between the two mountain ranged</div>
  </div>

  <div class="entry">
    <div class="label">1032 BE</div>
    <div class="details">The giant army crosses the Phanehold Tundra and reaches the borders of Patrie</div>
    <div class="details">The giant army dissolves into stone and clay at the border of Patrie</div>
  </div>
  
  <div class="entry">
    <div class="label">1030 BE</div>
    <div class="details">The Kingdom of Patrie, frightened by the unexpected approach, decided to commit to action to retake their ancestral homeland in the Red Forest and Red River delta</div>
  </div>

  <div class="entry">
    <div class="label">1028 BE</div>
    <div class="details">The Patrie Royal Navy lays seige to a city at the mouth of the Red River. The fall of that city triggered a system of alliances that pressured kingdoms and dukedoms across the Greman region to combat Patrie</div>
  </div>

  <div class="entry">
    <div class="label">1000 BE</div>
    <div class="details">The Kingdom of Orangi devolves into civil war over disagreements in the upper government about participation in the campaign against Patrie</div>
  </div>

  <div class="entry">
    <div class="label">990 BE</div>
    <div class="details">Ranshal invades Orangi's easter border, taking advantage of the continuing civil war</div>
  </div>

  <div class="entry">
    <div class="label">975 BE</div>
    <div class="details">The Empire of Optila backs the interventionist faction in Orangi</div>
    <div class="details">The Empire of Optila conquers the Svalhalli Peninsula</div>
    <div class="details">The Empire of Optila enters combat alongside the interventionist faction in the Orangi civil war</div>
  </div>

  <div class="entry">
    <div class="label">970 BE</div>
    <div class="details">The Empire of Optila and the interventionist faction prevail, reclaiming control of the Orangi forest, as well as gaining control of Aponshal and the Wildi archipelago</div>
  </div>

  <div class="entry">
    <div class="label">960 BE</div>
    <div class="details">The Empire of Optila and Orangi join in the campaign to push Patrie out of the Red Forest region</div>
    <div class="details">The Empire of Optila sets up battles in a way to ensure the weakening of the Greman kingdoms and dukedoms</div>
  </div>

  <div class="entry">
    <div class="label">950 BE</div>
    <div class="details">Patrie is pushed out of the Red Forest region</div>
  </div>

  <div class="entry">
    <div class="label">945 BE</div>
    <div class="details">The Empire of Optila launches a campaign to invade the Heim Basin and the rest of the Gremen region</div>
  </div>

  <div class="entry">
    <div class="label">920 BE</div>
    <div class="details">The Empire of Optila successfully conquers the Heim Basin and the Gremen Region</div>
  </div>

  <div class="entry">
    <div class="label">910 BE</div>
    <div class="details">The Empire of Optila conquers the island of Vinnestar and continues west into Koktos</div>
    <div class="details">The Empire of Optila's scouts encounter the border of the Golden Land, who had quietly expanded to control the eastern coast of Koktos north of Mt. Othrys</div>
  </div>

  <div class="entry">
    <div class="label">900 BE</div>
    <div class="details">The Optilan Imperial Army pushed the Golden Army back to the Gulf of Hanektos</div>
    <div class="details">The Imperial Army occupies the city-state of Aria</div>
  </div>

  <div class="entry">
    <div class="label">880 BE</div>
    <div class="details">The city-state of Aria joins the Empire of Optila as a vassal state</div>
  </div>

  <div class="entry">
    <div class="label">860 BE</div>
    <div class="details">The Kingdom of Orangi joins the Empire of Optila as a vassal state</div>
  </div>

  <div class="entry">
    <div class="label">850 BE</div>
    <div class="details">Githzerai refugees from the continuing conflict in the Gith Peninsula construct a community around ancient ruins on the Jerana Peninsula</div>
  </div>

  <div class="entry">
    <div class="label">840 BE</div>
    <div class="details">The Githzerai refugees reactivates The Cradle, an ancient facility that produces Warforged</div>
  </div>

  <div class="entry">
    <div class="label">820 BE</div>
    <div class="details">The Empire of Optila learns of the Cradle, and sens a naval group to conquer the area</div>
  </div>

  <div class="entry">
    <div class="label">790 BE</div>
    <div class="details">The Empire of Optila deploys its newly acquired Warforged army onto Koktos, conquering Parthenos and sweeping across the entire island. The only spared area is the island of Babalonica</div>
  </div>

  <div class="entry">
    <div class="label">760 BE</div>
    <div class="details">The city-state of Aria revolts, and is crushed beneath the heel of the Empire of Optila in the Massacre of Yellow Square</div>
  </div>
  
  </div>

  
<div class="era era-grand-empire">
  <div class="era-title">The Age of The Grand Empire<span class="era-dates">760 BE to 400 BE</span></div>
  <div class="entry">
    <div class="label">  </div>
    <div class="details">  </div>
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
