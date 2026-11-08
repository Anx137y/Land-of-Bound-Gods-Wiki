---
title: Factions
---

<style>
  .faction-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
    gap: 1rem;
    margin: 2rem 0;
    width: 70vw;
    position: relative;
    left: 50%;
    transform: translateX(-50%);
  }

  .faction {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    aspect-ratio: 1 / 1;
    padding: 0.9rem 0.6rem;
    background: var(--color);
    color: #000;
    text-decoration: none;
    text-align: center;
    border-radius: 12px;
    border: 2px solid rgba(0, 0, 0, 0.25);
    transition: transform 0.15s, box-shadow 0.15s;
  }

  .faction:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
  }

  /* Space for the faction's symbol */
  .symbol {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    font-size: 2.4rem;
  }

  .symbol img {
    max-width: 70%;
    max-height: 100%;
  }

  .faction-name {
    font-size: 1rem;
    line-height: 1.2;
  }

  .former-tag {
    display: block;
    font-size: 0.7rem;
    opacity: 0.8;
    letter-spacing: 0.08em;
  }

  /* Former factions appear slightly faded */
  .faction.former { filter: saturate(0.5) brightness(0.9); }
</style>

# Factions and Nations

The many unique factions and nations of Phanelar

<div class="faction-grid">
<a class="faction" style="--color:#986795" href="factions/sal-jotna"><div class="symbol"><img width="50" height="50" alt="image" src="https://github.com/user-attachments/assets/51c251ec-3eb1-4c47-a539-82e3ca2dcc13"/></div><div class="faction-name">The Kingdom of Sal Jotna</div></a>
  
<a class="faction" style="--color:#986795" href="factions/valhalk"><div class="symbol"><img width="50" height="50" alt="image" src="https://github.com/user-attachments/assets/63f2a22d-9a68-4d62-9d22-228e50daf5b7"/></div><div class="faction-name">The Kingdom of Valhalk</div></a>

<a class="faction" style="--color:#986795" href="factions/dverganland"><div class="symbol"><img width="50" height="50" alt="image" src="https://github.com/user-attachments/assets/a62d2b68-99a4-4c52-b361-c618e0a34ae5"/></div>
<div class="faction-name">Konungsriki of Dvergenland</div></a>

<a class="faction" style="--color:#986795" href="factions/frorbia"><div class="symbol"><img width="50" height="50" alt="image" src="https://github.com/user-attachments/assets/83630f5b-2b46-445a-b154-099abc471c1d" />
</div><div class="faction-name">Rānae of Frorbia</div></a>

<a class="faction" style="--color:#986795" href="factions/orovar"><div class="symbol"><img width="50" height="50" alt="image" src="https://github.com/user-attachments/assets/a74d07cd-1860-4875-8167-9d106a01e720" />
</div><div class="faction-name">Bibliarchy of Orovar</div></a>

  
</div>
