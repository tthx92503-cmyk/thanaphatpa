<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Helion-Style Sample Website</title>
  <style>
    :root {
      --color-primary: #00f2fe;
      --color-secondary: #4facfe;
      --color-dark: #222;
      --color-light: #f5f7fa;
      --color-white: #fff;
      --font-sans: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    }
    body {
      margin: 0;
      padding: 0;
      font-family: var(--font-sans);
      background-color: var(--color-light);
      color: #333;
      line-height: 1.6;
    }
    header {
      background: linear-gradient(135deg, var(--color-secondary), var(--color-primary));
      color: var(--color-white);
      padding: 60px 20px;
      text-align: center;
    }
    header h1 {
      margin: 0;
      font-size: 3rem;
    }
    header p {
      font-size: 1.2rem;
      margin-top: 15px;
    }
    nav {
      background-color: var(--color-dark);
      color: var(--color-white);
      display: flex;
      justify-content: center;
      padding: 15px 0;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    nav a {
      color: var(--color-white);
      text-decoration: none;
      margin: 0 20px;
      font-weight: 500;
      font-size: 1rem;
    }
    nav a:hover {
      color: var(--color-primary);
    }
    section {
      max-width: 1000px;
      margin: 40px auto;
      padding: 0 20px;
    }
    .tech-cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      margin-top: 30px;
    }
    .tech-card {
      background: var(--color-white);
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      padding: 20px;
      text-align: center;
    }
    .tech-card h3 {
      color: var(--color-secondary);
      margin-bottom: 15px;
    }
    .faq {
      margin-top: 30px;
    }
    .faq-item {
      margin-bottom: 15px;
    }
    .faq-question {
      font-weight: bold;
      cursor: pointer;
    }
    .faq-answer {
      max-height: 0;
      overflow: hidden;
      transition: max-height 0.3s ease;
      margin-top: 5px;
    }
    .faq-item.open .faq-answer {
      max-height: 200px; /* ประมาณนี้ ถ้าตัวตอบเยอะอาจต้องปรับ */
    }
    footer {
      background-color: var(--color-dark);
      color: var(--color-white);
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
  </style>
</head>
<body>

  <header>
    <h1>We’re Building the World’s First Fusion Power Plant</h1>
    <p>Enabling a future with unlimited clean electricity</p>
  </header>

  <nav>
    <a href="#technology">Technology</a>
    <a href="#team">Team</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
  </nav>

  <section id="technology">
    <h2>Technology</h2>
    <div class="tech-cards">
      <div class="tech-card">
        <h3>How it Works</h3>
        <p>Understand the basic process behind our fusion technology, from plasma ignition to energy output.</p>
      </div>
      <div class="tech-card">
        <h3>Trenta</h3>
        <p>Our prototype machinery that shows the initial steps toward commercial fusion.</p>
      </div>
      <div class="tech-card">
        <h3>Polaris</h3>
        <p>The next-gen reactor aiming for higher efficiency and more frequent pulses.</p>
      </div>
    </div>
  </section>

  <section id="team">
    <h2>Team</h2>
    <p>Meet the people behind the vision — science, engineering, leadership — all working together for a clean energy future.</p>
    <!-- ถ้าอยาก ใส่รูป, รายละเอียดเพิ่มเติม -->
  </section>

  <section id="faq">
    <h2>FAQ</h2>
    <div class="faq">
      <div class="faq-item">
        <div class="faq-question">What is fusion power?</div>
        <div class="faq-answer">
          <p>Fusion is the process ... (อธิบายสั้นๆ ว่าอะไรเป็นอะไร) </p>
        </div>
      </div>
      <div class="faq-item">
        <div class="faq-question">How safe is it?</div>
        <div class="faq-answer">
          <p>เราทำงานภายใต้การควบคุมมาตรฐานสูงสุด …</p>
        </div>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <p>General Inquiries: <a href="mailto:inquiries@helionenergy.com">inquiries@helionenergy.com</a></p>
    <p>Media & Press: <a href="mailto:press@helionenergy.com">press@helionenergy.com</a></p>
  </section>

  <footer>
    <p>© 2025 Helion | Privacy Policy · Terms of Use</p>
  </footer>

  <script>
    // JS สำหรับเปิด/ปิด FAQ
    document.querySelectorAll('.faq-item .faq-question').forEach(q => {
      q.addEventListener('click', () => {
        const item = q.parentElement;
        item.classList.toggle('open');
      });
    });
  </script>

</body>
</html>
