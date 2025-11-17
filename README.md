<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Happy Birthday, My Special One</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet" />
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: "Poppins", sans-serif;
      background: #050816;
      color: #f9fafb;
      line-height: 1.6;
      scroll-behavior: smooth;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* Layout */
    .container {
      width: 90%;
      max-width: 1100px;
      margin: 0 auto;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 50;
      background: rgba(5, 8, 22, 0.92);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid rgba(148, 163, 184, 0.3);
    }

    .navbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.8rem 0;
    }

    .logo {
      font-weight: 700;
      letter-spacing: 1px;
      font-size: 1.1rem;
      color: #38bdf8;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1.5rem;
      font-size: 0.9rem;
    }

    nav a {
      color: #e5e7eb;
      opacity: 0.9;
      transition: opacity 0.2s, color 0.2s;
    }

    nav a:hover {
      opacity: 1;
      color: #38bdf8;
    }

    /* Hero */
    .hero {
      min-height: 90vh;
      display: flex;
      align-items: center;
      padding: 3rem 0;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: minmax(0, 2fr) minmax(0, 1.2fr);
      gap: 2rem;
      align-items: center;
    }

    @media (max-width: 768px) {
      .hero-grid {
        grid-template-columns: 1fr;
        text-align: center;
      }
    }

    .hero-tag {
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 3px;
      color: #a5b4fc;
      margin-bottom: 0.8rem;
    }

    .hero-title {
      font-size: 2.4rem;
      line-height: 1.2;
      margin-bottom: 0.8rem;
    }

    .hero-title span {
      color: #38bdf8;
    }

    .hero-subtitle {
      margin-bottom: 1.2rem;
      color: #cbd5f5;
      font-size: 0.98rem;
    }

    .hero-quote {
      font-size: 0.95rem;
      font-style: italic;
      color: #9ca3af;
      margin-bottom: 1.5rem;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
      justify-content: flex-start;
    }

    @media (max-width: 768px) {
      .hero-actions {
        justify-content: center;
      }
    }

    .btn {
      padding: 0.7rem 1.6rem;
      border-radius: 999px;
      border: 1px solid transparent;
      font-size: 0.9rem;
      cursor: pointer;
      transition: transform 0.15s ease, box-shadow 0.15s ease, background 0.15s ease, border-color 0.15s ease;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
    }

    .btn-primary {
      background: linear-gradient(135deg, #38bdf8, #a855f7);
      color: white;
      box-shadow: 0 8px 30px rgba(56, 189, 248, 0.35);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 10px 40px rgba(56, 189, 248, 0.45);
    }

    .btn-ghost {
      background: transparent;
      border-color: #4b5563;
      color: #e5e7eb;
    }

    .btn-ghost:hover {
      border-color: #38bdf8;
      background: rgba(15, 23, 42, 0.7);
    }

    .hero-side {
      background: radial-gradient(circle at top, rgba(56, 189, 248, 0.3), transparent 55%),
                  radial-gradient(circle at bottom, rgba(168, 85, 247, 0.3), transparent 60%);
      border-radius: 24px;
      padding: 1.8rem;
      border: 1px solid rgba(148, 163, 184, 0.4);
      box-shadow: 0 18px 50px rgba(15, 23, 42, 0.8);
    }

    .hero-side-title {
      font-size: 1rem;
      font-weight: 600;
      margin-bottom: 0.6rem;
    }

    .hero-side-text {
      font-size: 0.9rem;
      color: #e5e7eb;
      margin-bottom: 0.6rem;
    }

    .tag-chip {
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
      padding: 0.25rem 0.7rem;
      border-radius: 999px;
      font-size: 0.75rem;
      background: rgba(15, 23, 42, 0.7);
      border: 1px solid rgba(148, 163, 184, 0.7);
      margin-right: 0.25rem;
      margin-bottom: 0.25rem;
    }

    /* Sections */
    section {
      padding: 3.5rem 0;
    }

    section h2 {
      font-size: 1.6rem;
      margin-bottom: 0.5rem;
    }

    section p.section-subtitle {
      font-size: 0.95rem;
      color: #9ca3af;
      margin-bottom: 1.8rem;
    }

    /* Timeline / “Stress-Strain Love Curve” */
    .timeline {
      display: grid;
      grid-template-columns: 1.3fr 1fr;
      gap: 2.5rem;
      align-items: center;
    }

    @media (max-width: 900px) {
      .timeline {
        grid-template-columns: 1fr;
      }
    }

    .timeline-curve {
      position: relative;
      background: radial-gradient(circle at top left, rgba(56, 189, 248, 0.25), transparent 60%);
      border-radius: 18px;
      padding: 1.8rem 1.6rem;
      border: 1px solid rgba(148, 163, 184, 0.4);
      min-height: 260px;
      overflow: hidden;
    }

    .curve-svg {
      width: 100%;
      height: 220px;
    }

    .timeline-curve small {
      font-size: 0.8rem;
      color: #9ca3af;
    }

    .timeline-events {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .event-card {
      background: rgba(15, 23, 42, 0.9);
      border-radius: 16px;
      padding: 1rem 1.1rem;
      border: 1px solid rgba(148, 163, 184, 0.4);
    }

    .event-meta {
      font-size: 0.78rem;
      color: #9ca3af;
      margin-bottom: 0.3rem;
    }

    .event-title {
      font-size: 0.95rem;
      font-weight: 600;
      margin-bottom: 0.2rem;
    }

    .event-text {
      font-size: 0.9rem;
      color: #e5e7eb;
    }

    /* Properties */
    .cards-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.4rem;
    }

    @media (max-width: 900px) {
      .cards-grid {
        grid-template-columns: 1fr;
      }
    }

    .card {
      background: radial-gradient(circle at top, rgba(56, 189, 248, 0.18), transparent 60%);
      border-radius: 18px;
      padding: 1.4rem 1.3rem;
      border: 1px solid rgba(148, 163, 184, 0.4);
      height: 100%;
    }

    .card-label {
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 2px;
      color: #a5b4fc;
      margin-bottom: 0.4rem;
    }

    .card-title {
      font-size: 1rem;
      font-weight: 600;
      margin-bottom: 0.4rem;
    }

    .card-text {
      font-size: 0.9rem;
      color: #e5e7eb;
      margin-bottom: 0.4rem;
    }

    .card-meta {
      font-size: 0.8rem;
      color: #9ca3af;
    }

    /* Gallery */
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.2rem;
    }

    @media (max-width: 900px) {
      .gallery-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }

    @media (max-width: 640px) {
      .gallery-grid {
        grid-template-columns: 1fr;
      }
    }

    .gallery-item {
      background: rgba(15, 23, 42, 0.9);
      border-radius: 16px;
      border: 1px solid rgba(148, 163, 184, 0.4);
      overflow: hidden;
      display: flex;
      flex-direction: column;
    }

    .gallery-img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      background: #020617;
    }

    .gallery-caption {
      padding: 0.7rem 0.9rem 0.9rem;
      font-size: 0.85rem;
      color: #e5e7eb;
    }

    /* Secret audio / voice note */
    .secret-box {
      margin-top: 1.2rem;
      background: rgba(15, 23, 42, 0.9);
      border-radius: 16px;
      border: 1px dashed rgba(148, 163, 184, 0.7);
      padding: 1rem 1.2rem;
      font-size: 0.9rem;
      color: #e5e7eb;
    }

    .secret-label {
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 3px;
      color: #fbbf24;
      margin-bottom: 0.2rem;
    }

    audio {
      width: 100%;
      margin-top: 0.6rem;
    }

    /* Final message */
    .final-box {
      background: radial-gradient(circle at center, rgba(56, 189, 248, 0.18), transparent 65%);
      border-radius: 24px;
      padding: 2rem 1.5rem;
      border: 1px solid rgba(148, 163, 184, 0.4);
      text-align: center;
      max-width: 720px;
      margin: 0 auto;
    }

    .final-main {
      font-size: 1.15rem;
      margin-bottom: 0.7rem;
    }

    .final-sub {
      font-size: 0.95rem;
      color: #cbd5f5;
      margin-bottom: 1.1rem;
    }

    .signature {
      font-size: 0.9rem;
      color: #9ca3af;
    }

    footer {
      padding: 1.5rem 0 2.5rem;
      font-size: 0.75rem;
      color: #6b7280;
      text-align: center;
    }
  </style>
</head>
<body>
  <!-- HEADER -->
  <header>
    <div class="container navbar">
      <div class="logo">
        Material Love Lab
      </div>
      <nav>
        <ul>
          <li><a href="#hero">Home</a></li>
          <li><a href="#timeline">Us</a></li>
          <li><a href="#properties">Why You</a></li>
          <li><a href="#gallery">Moments</a></li>
          <li><a href="#message">Message</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- HERO -->
  <section class="hero" id="hero">
    <div class="container hero-grid">
      <div>
        <div class="hero-tag">Birthday Special • For You Only</div>
        <h1 class="hero-title">
          Happy Birthday, <span>[Her Name]</span> 💙
        </h1>
        <p class="hero-subtitle">
          From a materials science student who still can’t calculate how lucky he is to have you.
        </p>
        <p class="hero-quote">
          “If love had a tensile strength test, ours would break every machine in the lab.”
        </p>
        <div class="hero-actions">
          <a href="#timeline" class="btn btn-primary">
            Start the Journey →
          </a>
          <a href="#message" class="btn btn-ghost">
            Jump to the Birthday Wish
          </a>
        </div>
      </div>

      <div class="hero-side">
        <div class="hero-side-title">You are my favorite material</div>
        <p class="hero-side-text">
          In a world full of structures, phases and defects, you are the one thing that always makes perfect sense to me.
        </p>
        <p class="hero-side-text">
          This page is my tiny experiment: to show you, with a little science and a lot of heart, how special you are to me.
        </p>
        <div>
          <span class="tag-chip">Toughness ∞</span>
          <span class="tag-chip">Stability: Only with you</span>
          <span class="tag-chip">Phase: Happiest</span>
        </div>
      </div>
    </div>
  </section>

  <!-- TIMELINE / STRESS-STRAIN LOVE CURVE -->
  <section id="timeline">
    <div class="container">
      <h2>Our Stress–Strain Love Curve</h2>
      <p class="section-subtitle">
        Every strong material has a journey: elastic beginnings, plastic changes, and a point where it never returns to the old shape again. That’s what you did to my life.
      </p>

      <div class="timeline">
        <div class="timeline-curve">
          <svg class="curve-svg" viewBox="0 0 300 200">
            <!-- axes -->
            <line x1="30" y1="10" x2="30" y2="180" stroke="#64748b" stroke-width="1" />
            <line x1="30" y1="180" x2="280" y2="180" stroke="#64748b" stroke-width="1" />
            <!-- curve -->
            <path d="M30 175 
                     Q 90 120 150 90 
                     T 260 40" 
                  fill="none" stroke="#38bdf8" stroke-width="3" />
            <!-- points -->
            <circle cx="70" cy="145" r="4" fill="#a855f7" />
            <circle cx="140" cy="105" r="4" fill="#22c55e" />
            <circle cx="210" cy="70" r="4" fill="#fbbf24" />
            <circle cx="260" cy="40" r="4" fill="#f97316" />

            <!-- labels -->
            <text x="60" y="160" fill="#e5e7eb" font-size="9">First message</text>
            <text x="120" y="120" fill="#e5e7eb" font-size="9">First time we met</text>
            <text x="188" y="85" fill="#e5e7eb" font-size="9">The day I fell for you</text>
            <text x="230" y="55" fill="#e5e7eb" font-size="9">No going back</text>
          </svg>
          <small>Stress vs. Strain of my heart, tested only by you.</small>
        </div>

        <div class="timeline-events">
          <div class="event-card">
            <div class="event-meta">Elastic Region • [Edit the date]</div>
            <div class="event-title">The first “Hi”</div>
            <p class="event-text">
              That tiny message from you felt small, but it stretched my whole day into something brighter. I pretended to be normal. I failed.
            </p>
          </div>

          <div class="event-card">
            <div class="event-meta">Yield Point • [Edit the date]</div>
            <div class="event-title">When you became special</div>
            <p class="event-text">
              Somewhere between our random talks and shared jokes, you quietly crossed the yield point and permanently changed my life’s shape.
            </p>
          </div>

          <div class="event-card">
            <div class="event-meta">Ultimate Strength • [Edit the date]</div>
            <div class="event-title">Realizing I love you</div>
            <p class="event-text">
              That moment I realized it wasn’t just “liking” you anymore. It was deeper, stronger and impossible to ignore. No lab could measure it.
            </p>
          </div>

          <div class="event-card">
            <div class="event-meta">Safe Design • Today</div>
            <div class="event-title">Your birthday</div>
            <p class="event-text">
              Now you’re not just part of my story. You are the person I want to design every future around. One more year of your life, and I’m grateful I get a small place in it.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- PROPERTIES SECTION -->
  <section id="properties">
    <div class="container">
      <h2>Your Material Properties</h2>
      <p class="section-subtitle">
        If I had to write your description as a materials science report, it would look something like this.
      </p>

      <div class="cards-grid">
        <div class="card">
          <div class="card-label">Property 01</div>
          <div class="card-title">Strength</div>
          <p class="card-text">
            You handle stress, problems, and chaos with a quiet strength that I admire more than any “high strength alloy” in textbooks.
          </p>
          <p class="card-meta">
            Observation: Under pressure, she remains calm, kind and steady. No signs of failure.
          </p>
        </div>

        <div class="card">
          <div class="card-label">Property 02</div>
          <div class="card-title">Resilience</div>
          <p class="card-text">
            You bounce back from difficult days and still manage to care about others. That resilience inspires me to be better every single day.
          </p>
          <p class="card-meta">
            Conclusion: High impact resistance. Recovered from every shock with even more beauty.
          </p>
        </div>

        <div class="card">
          <div class="card-label">Property 03</div>
          <div class="card-title">Warmth</div>
          <p class="card-text">
            No matter how cold the world feels, you have a way of making everything softer, warmer and more alive just by being there.
          </p>
          <p class="card-meta">
            Result: Excellent thermal comfort. Ideal material to keep one heart safe for life.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- GALLERY -->
  <section id="gallery">
    <div class="container">
      <h2>Our Moments • Tiny Microstructures of Happiness</h2>
      <p class="section-subtitle">
        Every micrograph shows a structure. Every photo of us shows a memory I never want to lose.
      </p>

      <div class="gallery-grid">
        <!-- Replace src with your actual image paths -->
        <div class="gallery-item">
          <img src="images/photo1.jpg" alt="Memory 1" class="gallery-img" />
          <div class="gallery-caption">
            The day we [write something], when time felt strangely perfect and simple.
          </div>
        </div>
        <div class="gallery-item">
          <img src="images/photo2.jpg" alt="Memory 2" class="gallery-img" />
          <div class="gallery-caption">
            Your smile here is still one of my favorite “phases” you’ve ever been in.
          </div>
        </div>
        <div class="gallery-item">
          <img src="images/photo3.jpg" alt="Memory 3" class="gallery-img" />
          <div class="gallery-caption">
            Proof that the best experiments in life are unplanned and start with you.
          </div>
        </div>
      </div>

      <!-- Secret voice note box -->
      <div class="secret-box">
        <div class="secret-label">Secret Attachment</div>
        <p>
          I recorded a tiny message just for you. It’s not perfect, but it’s real, just like how I feel about you.
        </p>
        <!-- Replace "audio/voice-note.mp3" with your actual audio file path -->
        <audio controls>
          <source src="audio/voice-note.mp3" type="audio/mpeg" />
          Your browser does not support the audio element.
        </audio>
      </div>
    </div>
  </section>

  <!-- FINAL MESSAGE -->
  <section id="message">
    <div class="container">
      <div class="final-box">
        <h2>My Birthday Wish for You</h2>
        <p class="final-main">
          Happy Birthday, my favorite human material. You’re the one thing in my life that feels stronger, safer and more beautiful with time.
        </p>
        <p class="final-sub">
          I don’t know every equation, I don’t understand every theory, but I know this:<br />
          When I think about my future, you are there. Not as an extra, not as a side note, but as the main part of the design.
          <br /><br />
          I wish you a year full of peace in your mind, light in your heart and success in everything you dream of.  
          May you always feel loved, protected and proud of the person you are becoming.
        </p>
        <p class="signature">
          With all my love,<br />
          [Your Name]
        </p>
      </div>
    </div>
  </section>

  <footer>
    Crafted with too many feelings and a bit of materials science • For [Her Name] on her birthday ❤
  </footer>
</body>
</html>
