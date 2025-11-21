<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calendario dell'Avvento</title>
  <style>
    body {
      font-family: sans-serif;
      margin: 0;
      background: url('https://images.unsplash.com/photo-1543589077-47d81606c1bf') no-repeat center center fixed;
      background-size: cover;
      min-height: 100vh;
    }

    .overlay {
      background: rgba(0, 0, 0, 0.5);
      width: 100%;
      height: 100%;
      position: fixed;
      top: 0;
      left: 0;
      pointer-events: none;
      z-index: 0;
    }

    h1 {
      text-align: center;
      color: white;
      padding-top: 20px;
      text-shadow: 2px 2px 4px black;
      margin: 0;
      position: relative;
      z-index: 2;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      gap: 15px;
      padding: 40px;
      max-width: 1000px;
      margin: 20px auto 80px auto;
      position: relative;
      z-index: 2;
    }

    .day {
      background: rgba(200, 0, 0, 0.95);
      color: white;
      padding: 25px;
      font-size: 28px;
      text-align: center;
      cursor: pointer;
      border-radius: 12px;
      font-weight: bold;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.6);
      user-select: none;
      transition: transform 0.12s ease, opacity 0.12s ease;
      box-shadow: 0 6px 16px rgba(0,0,0,0.35);
    }

    .day:hover { transform: translateY(-4px); }

    .day.locked {
      background: rgba(120, 120, 120, 0.95);
      cursor: pointer; /* still clickable to show popup */
      opacity: 0.95;
    }

    #modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.85);
      justify-content: center;
      align-items: center;
      z-index: 20;
    }

    #modalContent {
      background: white;
      padding: 20px;
      border-radius: 10px;
      text-align: center;
      max-width: 90%;
      box-shadow: 0 10px 30px rgba(0,0,0,0.4);
    }

    #modalImg {
      max-width: 320px;
      border-radius: 10px;
      display: block;
      margin: 0 auto;
    }

    button {
      padding: 10px 20px;
      margin-top: 15px;
      border: none;
      background: #b30000;
      color: white;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
    }

    /* Effetto neve */
    .snowflake {
      position: fixed;
      top: -10px;
      color: white;
      font-size: 1em;
      animation-name: fall;
      animation-timing-function: linear;
      animation-iteration-count: infinite;
      pointer-events: none;
      z-index: 10;
      will-change: transform;
    }

    @keyframes fall {
      0% { transform: translateY(-10vh) rotate(0deg); opacity: 1; }
      100% { transform: translateY(110vh) rotate(360deg); opacity: 0; }
    }

    /* Responsive */
    @media (max-width: 900px) {
      .grid { grid-template-columns: repeat(5, 1fr); padding: 24px; }
    }
    @media (max-width: 600px) {
      .grid { grid-template-columns: repeat(4, 1fr); padding: 16px; }
      .day { padding: 14px; font-size: 18px; }
    }
  </style>
</head>
<body>
  <div class="overlay"></div>

  <h1>🎄 Calendario dell'Avvento 🎄</h1>

  <div class="grid" id="calendar" aria-label="Calendario dell'Avvento"></div>

  <div id="modal" role="dialog" aria-modal="true" aria-hidden="true">
    <div id="modalContent">
      <img id="modalImg" alt="Immagine del giorno"><br><br>
      <p id="modalText"></p>
      <button id="closeBtn">Chiudi</button>
    </div>
  </div>

  <script>
    // --- DATI ---
    // images: mappa giorno -> {img, text}
    const images = {};

    // --- ELEMENTI ---
    const now = new Date();
    const today = now.getDate(); // giorno corrente del mese
    const calendar = document.getElementById('calendar');
    const modal = document.getElementById('modal');
    const modalImg = document.getElementById('modalImg');
    const modalText = document.getElementById('modalText');
    const closeBtn = document.getElementById('closeBtn');

    // --- COSTRUZIONE CALENDARIO ---
    // Popoliamo images e creiamo le caselle CORRETTAMENTE dentro il ciclo
    for (let i = 1; i <= 24; i++) {
      images[i] = {
        img: `img/${i}.jpg`,
        text: `Frase del giorno ${i}`
      };

      const cell = document.createElement('div');
      cell.className = 'day' + (i > today ? ' locked' : '');
      cell.textContent = i;
      cell.setAttribute('role', 'button');
      cell.setAttribute('tabindex', '0');
      cell.setAttribute('aria-label', `Giorno ${i}`);

      if (i <= today) {
        cell.addEventListener('click', () => openModal(i));
        cell.addEventListener('keydown', (e) => { if (e.key === 'Enter' || e.key === ' ') openModal(i); });
      } else {
        cell.addEventListener('click', () => {
          // messaggio per i giorni futuri
          alert('Non essere frettolosa, la magia del Natale ha i suoi tempi!');
        });
        cell.addEventListener('keydown', (e) => { if (e.key === 'Enter' || e.key === ' ') alert('Non essere frettolosa, la magia del Natale ha i suoi tempi!'); });
      }

      calendar.appendChild(cell);
    }

    // --- FUNZIONI MODALE ---
    function openModal(day) {
      const data = images[day] || {};
      // fallback se immagine non esiste: non impostare src, o impostare una placeholder
      modalImg.src = '';
      modalImg.alt = `Immagine del giorno ${day}`;

      // prova a caricare l'immagine e mostrare il testo
      const imgUrl = data.img || '';
      if (imgUrl) {
        // carica immagine con gestione errori
        modalImg.src = imgUrl;
        modalImg.onerror = () => {
          modalImg.style.display = 'none';
        };
        modalImg.onload = () => {
          modalImg.style.display = 'block';
        };
      } else {
        modalImg.style.display = 'none';
      }

      modalText.textContent = data.text || '';
      modal.style.display = 'flex';
      modal.setAttribute('aria-hidden', 'false');
    }

    function closeModal() {
      modal.style.display = 'none';
      modal.setAttribute('aria-hidden', 'true');
      modalImg.src = '';
    }

    closeBtn.addEventListener('click', closeModal);
    modal.addEventListener('click', (e) => { if (e.target === modal) closeModal(); });
    document.addEventListener('keydown', (e) => { if (e.key === 'Escape') closeModal(); });

    // --- NEVE ---
    function createSnow() {
      const snowflake = document.createElement('div');
      snowflake.className = 'snowflake';
      snowflake.textContent = '❄';
      snowflake.style.left = Math.random() * 100 + 'vw';
      snowflake.style.fontSize = (Math.random() * 20 + 8) + 'px';
      snowflake.style.animationDuration = (Math.random() * 8 + 6) + 's';
      snowflake.style.opacity = (Math.random() * 0.6 + 0.4);

      document.body.appendChild(snowflake);

      // rimuovi dopo fine animazione (valore > durata animation)
      setTimeout(() => {
        if (snowflake && snowflake.parentNode) snowflake.parentNode.removeChild(snowflake);
      }, 16000);
    }

    // avvia la neve (frequenza moderata)
    const snowInterval = setInterval(createSnow, 300);

    // --- NOTE per l'utente su come sostituire immagini e testi ---
    // 1) crea una cartella "img" accanto a questo file
    // 2) inserisci le immagini nominate 1.jpg 2.jpg ... 24.jpg
    // 3) per testi personalizzati, modifica l'oggetto `images` qui sopra (es. images[1].text = "Ciao!")

  </script>
</body>
</html>
