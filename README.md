# haynes-homestead
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Haynes Homestead | Colebrook, NH Farm</title>
  <meta name="description" content="Haynes Homestead is a family farm in Colebrook, New Hampshire offering farm-grown produce, eggs, berries, and North Country homestead goods." />
  <style>
    :root {
      --cream: #fbf5e9;
      --paper: #fffaf1;
      --sage: #6f7f4f;
      --deep: #26351f;
      --rust: #a85d2b;
      --gold: #d4a843;
      --berry: #7e2f45;
      --ink: #1e2419;
      --muted: #68705f;
      --shadow: 0 18px 50px rgba(38, 53, 31, 0.16);
      --radius: 28px;
    }

    * { box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      font-family: Georgia, 'Times New Roman', serif;
      background: var(--cream);
      color: var(--ink);
      line-height: 1.55;
    }

    img {
      display: block;
      max-width: 100%;
    }

    a { color: inherit; }

    .topbar {
      background: var(--deep);
      color: var(--cream);
      text-align: center;
      padding: 10px 16px;
      font-size: 0.95rem;
      letter-spacing: 0.02em;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 5;
      background: rgba(251, 245, 233, 0.94);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid rgba(38, 53, 31, 0.12);
    }

    nav {
      max-width: 1120px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 18px 20px;
      gap: 18px;
    }

    .brand {
      font-size: 1.3rem;
      font-weight: 700;
      letter-spacing: 0.03em;
      color: var(--deep);
      text-decoration: none;
      white-space: nowrap;
    }

    .nav-links {
      display: flex;
      gap: 18px;
      align-items: center;
      font-family: Arial, sans-serif;
      font-size: 0.9rem;
      color: var(--deep);
    }

    .nav-links a {
      text-decoration: none;
      opacity: 0.85;
    }

    .nav-links a:hover { opacity: 1; }

    .button {
      display: inline-block;
      background: var(--rust);
      color: white;
      padding: 13px 20px;
      border-radius: 999px;
      text-decoration: none;
      font-family: Arial, sans-serif;
      font-weight: 700;
      letter-spacing: 0.01em;
      box-shadow: 0 10px 25px rgba(168, 93, 43, 0.24);
    }

    .button.secondary {
      background: transparent;
      color: var(--deep);
      border: 1px solid rgba(38, 53, 31, 0.35);
      box-shadow: none;
    }

    .hero {
      max-width: 1120px;
      margin: 0 auto;
      padding: 76px 20px 46px;
      display: grid;
      grid-template-columns: 1.05fr 0.95fr;
      gap: 46px;
      align-items: center;
    }

    .eyebrow {
      font-family: Arial, sans-serif;
      color: var(--rust);
      font-weight: 800;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      font-size: 0.82rem;
    }

    h1 {
      font-size: clamp(3rem, 7vw, 6rem);
      line-height: 0.92;
      margin: 14px 0 22px;
      color: var(--deep);
      letter-spacing: -0.05em;
    }

    .hero p {
      font-size: 1.2rem;
      color: var(--muted);
      max-width: 620px;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 30px;
    }

    .farm-card {
      min-height: 560px;
      border-radius: var(--radius);
      overflow: hidden;
      box-shadow: var(--shadow);
      position: relative;
      background: var(--deep);
    }

    .farm-card img {
      width: 100%;
      height: 100%;
      min-height: 560px;
      object-fit: cover;
      object-position: center;
    }

    .farm-card::after {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(180deg, rgba(38,53,31,0.02), rgba(38,53,31,0.72));
    }

    .farm-card-content {
      position: absolute;
      bottom: 0;
      z-index: 2;
      padding: 30px;
      color: white;
    }

    .farm-card-content h2 {
      margin: 0 0 10px;
      font-size: 2rem;
      line-height: 1.05;
    }

    .farm-card-content p {
      margin: 0;
      color: rgba(255,255,255,0.84);
      font-size: 1rem;
    }

    .photo-strip {
      max-width: 1120px;
      margin: 0 auto;
      padding: 0 20px 24px;
      display: grid;
      grid-template-columns: 1.2fr 0.8fr 1fr;
      gap: 14px;
    }

    .photo-strip img,
    .gallery img,
    .story-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .photo-strip figure,
    .gallery figure {
      margin: 0;
      border-radius: 20px;
      overflow: hidden;
      box-shadow: 0 10px 28px rgba(38, 53, 31, 0.12);
      background: var(--paper);
      min-height: 220px;
    }

    .section {
      max-width: 1120px;
      margin: 0 auto;
      padding: 64px 20px;
    }

    .section-title {
      max-width: 720px;
      margin-bottom: 30px;
    }

    h2 {
      color: var(--deep);
      font-size: clamp(2.1rem, 4vw, 3.5rem);
      line-height: 1;
      margin: 0 0 16px;
      letter-spacing: -0.04em;
    }

    .section-title p, .card p, .story p, .contact p {
      color: var(--muted);
      font-size: 1.05rem;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .card {
      background: var(--paper);
      border: 1px solid rgba(38, 53, 31, 0.1);
      border-radius: 22px;
      padding: 24px;
      box-shadow: 0 12px 30px rgba(38, 53, 31, 0.08);
    }

    .card .icon {
      font-size: 2.1rem;
      margin-bottom: 12px;
    }

    .card h3 {
      margin: 0 0 8px;
      color: var(--deep);
      font-size: 1.35rem;
    }

    .story-wrap {
      display: grid;
      grid-template-columns: 0.9fr 1.1fr;
      gap: 24px;
      align-items: stretch;
    }

    .story-image {
      border-radius: var(--radius);
      min-height: 420px;
      box-shadow: var(--shadow);
      position: relative;
      overflow: hidden;
      background: var(--deep);
    }

    .story-image::after {
      content: "North Country grown";
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      color: white;
      font-size: 2.2rem;
      line-height: 1;
      font-weight: 700;
      padding: 80px 24px 24px;
      background: linear-gradient(180deg, transparent, rgba(38,53,31,0.75));
    }

    .story {
      background: var(--paper);
      border-radius: var(--radius);
      padding: 34px;
      border: 1px solid rgba(38, 53, 31, 0.1);
    }

    .produce-list {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 20px;
    }

    .tag {
      background: rgba(111, 127, 79, 0.14);
      color: var(--deep);
      border: 1px solid rgba(111, 127, 79, 0.22);
      padding: 8px 12px;
      border-radius: 999px;
      font-family: Arial, sans-serif;
      font-size: 0.88rem;
    }

    .banner {
      background: var(--deep);
      color: var(--cream);
      margin: 30px 0;
      padding: 54px 20px;
    }

    .banner-inner {
      max-width: 1120px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: 1fr auto;
      gap: 24px;
      align-items: center;
    }

    .banner h2 { color: var(--cream); }
    .banner p { color: rgba(251,245,233,0.78); max-width: 740px; }

    .gallery {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 18px;
    }

    .gallery figure:first-child {
      min-height: 460px;
    }

    .gallery-stack {
      display: grid;
      gap: 18px;
    }

    .gallery figcaption,
    .photo-strip figcaption {
      font-family: Arial, sans-serif;
      color: var(--muted);
      font-size: 0.92rem;
      padding: 12px 14px 14px;
      background: var(--paper);
    }

    .contact {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 18px;
    }

    .contact-card {
      background: var(--paper);
      border-radius: var(--radius);
      padding: 32px;
      border: 1px solid rgba(38, 53, 31, 0.1);
      box-shadow: 0 12px 30px rgba(38, 53, 31, 0.08);
    }

    .contact-card strong {
      display: block;
      color: var(--deep);
      margin-bottom: 6px;
      font-family: Arial, sans-serif;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      font-size: 0.78rem;
    }

    .contact-card a {
      color: var(--rust);
      font-weight: 700;
    }

    footer {
      text-align: center;
      padding: 32px 20px;
      color: var(--muted);
      font-family: Arial, sans-serif;
      font-size: 0.9rem;
    }

    @media (max-width: 820px) {
      .nav-links { display: none; }
      .hero, .story-wrap, .contact, .banner-inner, .gallery { grid-template-columns: 1fr; }
      .farm-card, .farm-card img { min-height: 420px; }
      .grid, .photo-strip { grid-template-columns: 1fr; }
      .section { padding: 48px 20px; }
      .photo-strip figure, .gallery figure:first-child { min-height: 300px; }
    }
  </style>
</head>
<body>
  <div class="topbar">Colebrook, New Hampshire • Farm grown produce, eggs, berries, and homestead goods</div>

  <header>
    <nav>
      <a class="brand" href="#top">Haynes Homestead</a>
      <div class="nav-links">
        <a href="#about">About</a>
        <a href="#offerings">What We Grow</a>
        <a href="#gallery">Photos</a>
        <a href="#visit">Visit</a>
        <a class="button" href="tel:16032374395">Call the Farm</a>
      </div>
    </nav>
  </header>

  <main id="top">
    <section class="hero">
      <div>
        <div class="eyebrow">A North Country farmstead</div>
        <h1>Grown with grit, care, and good soil.</h1>
        <p>Haynes Homestead is a family farm in Colebrook, New Hampshire rooted in practical homesteading, fresh seasonal food, and a deep respect for the land.</p>
        <div class="hero-actions">
          <a class="button" href="tel:16032374395">Call for availability</a>
          <a class="button secondary" href="#visit">Plan a visit</a>
        </div>
      </div>

      <div class="farm-card" aria-label="Haynes Homestead barn in winter">
        <img src="DSCF1203.jpg" alt="Haynes Homestead barn in the snow with mountain views in Colebrook New Hampshire" />
        <div class="farm-card-content">
          <h2>Seasonal. Local. North Country raised.</h2>
          <p>From eggs and garden vegetables to berries and farmstand favorites, availability changes with the season.</p>
        </div>
      </div>
    </section>

    <section class="photo-strip" aria-label="Haynes Homestead photo highlights">
      <figure>
        <img src="IMG_7221.jpg" alt="Haynes Homestead yellow tomato sign with fresh cucumbers" />
      </figure>
      <figure>
        <img src="516880470_10238381242373598_5665367009121722829_n.jpg" alt="Hand painted Haynes Homestead berries and vegetables sign" />
      </figure>
      <figure>
        <img src="DBP_9071.jpg" alt="Family planting together in a field at Haynes Homestead" />
      </figure>
    </section>

    <section class="section" id="offerings">
      <div class="section-title">
        <div class="eyebrow">What you may find</div>
        <h2>Fresh from the homestead</h2>
        <p>Because this is a working farm, products and picking dates may change based on weather, crop timing, and the season. Calling ahead is always the best move.</p>
      </div>

      <div class="grid">
        <article class="card">
          <div class="icon">🥚</div>
          <h3>Eggs & poultry</h3>
          <p>Farm-raised chickens have long been part of the homestead, including laying hens for eggs and meat birds.</p>
        </article>
        <article class="card">
          <div class="icon">🥬</div>
          <h3>Vegetables</h3>
          <p>Seasonal vegetables are grown with care, using compost, cover crops, and practical North Country growing methods.</p>
        </article>
        <article class="card">
          <div class="icon">🍓</div>
          <h3>Berries & u-pick</h3>
          <p>Haynes Homestead has been listed for red raspberries, strawberries, and other seasonal fruit. Call first to check what is ready.</p>
        </article>
      </div>
    </section>

    <section class="section" id="about">
      <div class="story-wrap">
        <div class="story-image" aria-label="Family at Haynes Homestead">
          <img src="517157576_10238603944261006_5762540005036087069_n.jpg" alt="Haynes Homestead family standing outside the farmhouse" />
        </div>
        <div class="story">
          <div class="eyebrow">The story</div>
          <h2>Rooted in family, grown through community</h2>
          <p>Haynes Homestead isn’t just land — it’s generations of people showing up for it. What began as a dairy farm carried forward through years of change, with the Haynes family adapting, rebuilding, and choosing to keep the farm alive rather than let it fade.</p>
          <p>Through every shift — from dairy to cattle to a self-sustaining homestead — one thing stayed constant: family at the center. Knowledge passed down, hands working side by side, and a belief that the land is something you care for together.</p>
          <p>This farm has never existed in isolation. It’s part of the Colebrook community — neighbors stopping by, families returning each season, and local connections that keep it going. Whether it’s picking berries, grabbing fresh produce, or just knowing where your food comes from, Haynes Homestead has always been about people as much as it is about farming.</p>
          <p>Today, that same spirit carries on — simple, honest, and deeply rooted in both family and community.</p>
          <div class="produce-list" aria-label="Products list">
            <span class="tag">Eggs</span>
            <span class="tag">Raspberries</span>
            <span class="tag">Strawberries</span>
            <span class="tag">Tomatoes</span>
            <span class="tag">Squash</span>
            <span class="tag">Greens</span>
            <span class="tag">Garlic</span>
            <span class="tag">Pumpkins</span>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="gallery">
      <div class="section-title">
        <div class="eyebrow">Photo gallery</div>
        <h2>Life on the farm</h2>
        <p>A small look at the land, the signs, the work, and the family behind Haynes Homestead.</p>
      </div>

      <div class="gallery">
        <figure>
          <img src="DSCF1203.jpg" alt="Winter view of the Haynes Homestead barn and mountains" />
          <figcaption>The barn in a North Country winter.</figcaption>
        </figure>
        <div class="gallery-stack">
          <figure>
            <img src="DBP_9071.jpg" alt="Three generations planting in the field" />
            <figcaption>Generations working the same soil.</figcaption>
          </figure>
          <figure>
            <img src="IMG_7221.jpg" alt="Fresh cucumbers and Haynes Homestead tomatoes sign" />
            <figcaption>Roadside produce when the season allows.</figcaption>
          </figure>
        </div>
      </div>
    </section>

    <section class="banner">
      <div class="banner-inner">
        <div>
          <div class="eyebrow">Before you drive out</div>
          <h2>Call ahead for what is fresh today.</h2>
          <p>Farm availability can change quickly. For berries, eggs, produce, directions, or current pick-your-own timing, please call the farm directly.</p>
        </div>
        <a class="button" href="tel:16032374395">603-237-4395</a>
      </div>
    </section>

    <section class="section" id="visit">
      <div class="section-title">
        <div class="eyebrow">Visit the farm</div>
        <h2>Find Haynes Homestead in Colebrook</h2>
        <p>A simple, no-fuss farm page built to help people call, visit, and know what to expect before they head over.</p>
      </div>

      <div class="contact">
        <div class="contact-card">
          <strong>Address</strong>
          <p>172 Harvey Swell Road<br />Colebrook, NH 03576</p>
          <a href="https://www.google.com/maps/search/?api=1&query=172+Harvey+Swell+Road+Colebrook+NH+03576" target="_blank" rel="noopener">Open in Google Maps</a>
        </div>
        <div class="contact-card">
          <strong>Phone</strong>
          <p><a href="tel:16032374395">603-237-4395</a></p>
          <p>Call for current produce, eggs, berry picking, hours, and directions.</p>
        </div>
      </div>
    </section>
  </main>

  <footer>
    © <span id="year"></span> Haynes Homestead • Colebrook, New Hampshire<br />
    Website template built as a free one-page starter site.
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
