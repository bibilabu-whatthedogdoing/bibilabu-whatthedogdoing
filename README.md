<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#070b18" />
  <title>bibilabu-whatthedogdoing</title>

  <style>
    :root {
      --bg-0: #070b18;
      --bg-1: #0b1326;
      --ink: #ffffff;
      --ink-soft: rgba(244, 247, 255, 0.78);
      --ink-muted: rgba(226, 232, 240, 0.58);
      --line: rgba(255, 255, 255, 0.18);
      --line-strong: rgba(255, 255, 255, 0.30);
      --glass: rgba(255, 255, 255, 0.085);
      --glass-strong: rgba(255, 255, 255, 0.14);
      --glass-dark: rgba(8, 13, 28, 0.34);
      --radius-xl: 28px;
      --radius-lg: 22px;
      --radius-md: 16px;
      --font-sans: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      --font-mono: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace;
    }

    * {
      box-sizing: border-box;
    }

    html {
      min-height: 100%;
      background: var(--bg-0);
    }

    body {
      min-height: 100vh;
      margin: 0;
      color: var(--ink);
      font-family: var(--font-sans);
      overflow-x: hidden;
      background:
        radial-gradient(circle at 12% 22%, rgba(99, 179, 237, 0.34), transparent 26%),
        radial-gradient(circle at 84% 18%, rgba(219, 39, 119, 0.40), transparent 30%),
        radial-gradient(circle at 72% 78%, rgba(126, 34, 206, 0.44), transparent 34%),
        linear-gradient(135deg, #060e20 0%, #0b1326 42%, #24134d 76%, #4c123c 100%);
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      background:
        linear-gradient(115deg, transparent 0%, rgba(255, 255, 255, 0.08) 38%, transparent 54%),
        radial-gradient(circle at 50% 0%, rgba(255, 255, 255, 0.12), transparent 36%);
      opacity: 0.65;
    }

    body::after {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      opacity: 0.13;
      mix-blend-mode: soft-light;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='180' height='180' filter='url(%23n)' opacity='0.45'/%3E%3C/svg%3E");
    }

    .page {
      position: relative;
      z-index: 1;
      width: min(1120px, calc(100vw - 40px));
      min-height: 100vh;
      margin: 0 auto;
      padding: 42px 0;
      display: grid;
      align-items: center;
    }

    .orb {
      position: fixed;
      border-radius: 999px;
      filter: blur(46px);
      opacity: 0.45;
      pointer-events: none;
      transform: translateZ(0);
    }

    .orb.one {
      width: 360px;
      height: 360px;
      left: -120px;
      top: 18%;
      background: #6cb6ff;
    }

    .orb.two {
      width: 420px;
      height: 420px;
      right: -140px;
      bottom: 2%;
      background: #db2777;
    }

    .orb.three {
      width: 300px;
      height: 300px;
      right: 18%;
      top: -120px;
      background: #c084fc;
      opacity: 0.30;
    }

    .hero {
      position: relative;
      min-height: 650px;
      overflow: hidden;
      border: 1px solid var(--line-strong);
      border-radius: 40px;
      background:
        linear-gradient(135deg, rgba(255, 255, 255, 0.16), rgba(255, 255, 255, 0.055) 52%, rgba(255, 255, 255, 0.10)),
        rgba(255, 255, 255, 0.08);
      box-shadow:
        0 34px 120px rgba(0, 0, 0, 0.34),
        inset 0 1px 0 rgba(255, 255, 255, 0.34),
        inset 1px 0 0 rgba(255, 255, 255, 0.12);
      backdrop-filter: blur(34px) saturate(140%);
      -webkit-backdrop-filter: blur(34px) saturate(140%);
    }

    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      pointer-events: none;
      background:
        radial-gradient(circle at 12% 0%, rgba(255, 255, 255, 0.20), transparent 30%),
        linear-gradient(90deg, rgba(255, 255, 255, 0.10), transparent 42%);
      opacity: 0.85;
    }

    .hero::after {
      content: "";
      position: absolute;
      inset: 20px;
      pointer-events: none;
      border: 1px solid rgba(255, 255, 255, 0.13);
      border-radius: 30px;
    }

    .hero-inner {
      position: relative;
      z-index: 1;
      min-height: 650px;
      display: grid;
      grid-template-columns: minmax(0, 1fr) 360px;
      gap: 34px;
      padding: 56px;
    }

    .copy {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      min-width: 0;
    }

    .topline {
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 62px;
    }

    .chip {
      height: 34px;
      display: inline-flex;
      align-items: center;
      padding: 0 14px;
      border: 1px solid rgba(255, 255, 255, 0.20);
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.075);
      color: rgba(255, 255, 255, 0.84);
      font-size: 11px;
      font-weight: 760;
      line-height: 1;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      text-shadow: 0 2px 8px rgba(0, 0, 0, 0.22);
    }

    h1 {
      max-width: 720px;
      margin: 0;
      color: var(--ink);
      font-size: clamp(46px, 7vw, 82px);
      font-weight: 760;
      line-height: 0.96;
      letter-spacing: -0.075em;
      text-wrap: balance;
      text-shadow: 0 20px 58px rgba(0, 0, 0, 0.34);
    }

    .handle-break {
      display: block;
    }

    .lead {
      max-width: 600px;
      margin: 26px 0 0;
      color: var(--ink-soft);
      font-size: clamp(18px, 2vw, 24px);
      font-weight: 520;
      line-height: 1.45;
      letter-spacing: -0.025em;
      text-shadow: 0 2px 14px rgba(0, 0, 0, 0.18);
    }

    .manifesto {
      max-width: 650px;
      margin-top: 84px;
      padding-left: 22px;
      border-left: 1px solid rgba(255, 255, 255, 0.22);
      color: rgba(255, 255, 255, 0.66);
      font-size: 15px;
      font-weight: 500;
      line-height: 1.85;
    }

    .dock {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 12px;
      margin-top: 42px;
    }

    .mini {
      min-height: 108px;
      padding: 18px;
      border: 1px solid var(--line);
      border-radius: 22px;
      background: rgba(255, 255, 255, 0.075);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
      box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.18);
    }

    .mini strong {
      display: block;
      color: var(--ink);
      font-size: 15px;
      font-weight: 720;
      line-height: 1.2;
      letter-spacing: -0.02em;
    }

    .mini span {
      display: block;
      margin-top: 11px;
      color: rgba(226, 232, 240, 0.62);
      font-size: 12px;
      font-weight: 540;
      line-height: 1.55;
    }

    .side {
      display: grid;
      grid-template-rows: 1fr auto;
      gap: 16px;
      min-width: 0;
    }

    .code-card,
    .license-card {
      border: 1px solid rgba(255, 255, 255, 0.17);
      border-radius: 28px;
      background: rgba(7, 11, 24, 0.28);
      box-shadow:
        0 20px 60px rgba(0, 0, 0, 0.18),
        inset 0 1px 0 rgba(255, 255, 255, 0.16);
      backdrop-filter: blur(28px) saturate(130%);
      -webkit-backdrop-filter: blur(28px) saturate(130%);
    }

    .code-card {
      padding: 24px;
    }

    .window {
      display: flex;
      gap: 7px;
      margin-bottom: 30px;
    }

    .dot {
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.42);
    }

    .dot:nth-child(1) { background: rgba(255, 180, 171, 0.92); }
    .dot:nth-child(2) { background: rgba(255, 216, 231, 0.90); }
    .dot:nth-child(3) { background: rgba(173, 201, 235, 0.90); }

    pre {
      margin: 0;
      color: rgba(246, 249, 255, 0.88);
      font-family: var(--font-mono);
      font-size: 13px;
      font-weight: 650;
      line-height: 1.92;
      white-space: pre-wrap;
      text-shadow: 0 2px 12px rgba(0, 0, 0, 0.20);
    }

    .muted { color: rgba(226, 232, 240, 0.42); }
    .kw { color: #ffffff; }
    .fn { color: #dbeafe; }
    .str { color: #ffd8e7; }

    .license-card {
      padding: 24px;
      background:
        linear-gradient(135deg, rgba(255, 255, 255, 0.13), rgba(255, 255, 255, 0.065)),
        rgba(255, 255, 255, 0.05);
    }

    .label {
      display: block;
      color: rgba(255, 255, 255, 0.54);
      font-size: 11px;
      font-weight: 800;
      line-height: 1;
      letter-spacing: 0.15em;
      text-transform: uppercase;
    }

    .license-card b {
      display: block;
      margin-top: 18px;
      color: var(--ink);
      font-size: 32px;
      font-weight: 760;
      line-height: 1;
      letter-spacing: -0.045em;
    }

    .license-card p {
      margin: 18px 0 0;
      color: rgba(244, 247, 255, 0.66);
      font-size: 13px;
      font-weight: 520;
      line-height: 1.7;
    }

    .bottom {
      position: relative;
      z-index: 1;
      display: flex;
      justify-content: space-between;
      gap: 18px;
      margin-top: 18px;
      color: rgba(255, 255, 255, 0.52);
      font-family: var(--font-mono);
      font-size: 12px;
      font-weight: 650;
      letter-spacing: -0.02em;
    }

    .bottom span:last-child {
      color: rgba(255, 255, 255, 0.78);
    }

    @media (max-width: 980px) {
      .page {
        align-items: start;
        padding: 28px 0;
      }

      .hero,
      .hero-inner {
        min-height: auto;
      }

      .hero-inner {
        grid-template-columns: 1fr;
        padding: 32px;
      }

      .topline {
        margin-bottom: 44px;
      }

      .manifesto {
        margin-top: 52px;
      }

      .side {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 680px) {
      .page {
        width: min(100vw - 18px, 1120px);
        padding: 9px 0;
      }

      .hero {
        border-radius: 28px;
      }

      .hero::after {
        inset: 12px;
        border-radius: 20px;
      }

      .hero-inner {
        padding: 24px;
      }

      .dock {
        grid-template-columns: 1fr;
      }

      h1 {
        font-size: clamp(42px, 14vw, 62px);
      }

      .bottom {
        display: grid;
      }
    }

    @media (prefers-reduced-motion: no-preference) {
      .hero {
        animation: enter 760ms cubic-bezier(.2, .8, .2, 1) both;
      }

      .orb.one {
        animation: drift-one 12s ease-in-out infinite alternate;
      }

      .orb.two {
        animation: drift-two 14s ease-in-out infinite alternate;
      }

      @keyframes enter {
        from {
          opacity: 0;
          transform: translateY(18px) scale(0.985);
        }
        to {
          opacity: 1;
          transform: translateY(0) scale(1);
        }
      }

      @keyframes drift-one {
        to { transform: translate3d(42px, 24px, 0) scale(1.04); }
      }

      @keyframes drift-two {
        to { transform: translate3d(-34px, -26px, 0) scale(1.06); }
      }
    }
  </style>
</head>

<body>
  <div class="orb one" aria-hidden="true"></div>
  <div class="orb two" aria-hidden="true"></div>
  <div class="orb three" aria-hidden="true"></div>

  <main class="page">
    <section class="hero" aria-label="Profile landing page">
      <div class="hero-inner">
        <div class="copy">
          <div>
            <div class="topline" aria-label="profile signals">
              <span class="chip">new account</span>
              <span class="chip">no lore</span>
              <span class="chip">observe carefully</span>
            </div>

            <h1>
              bibilabu-<span class="handle-break">whatthedogdoing</span>
            </h1>

            <p class="lead">
              fresh account. not fresh hands.
            </p>

            <p class="manifesto">
              I build software close to the machine, where timing matters, ownership matters,
              and vague abstractions eventually become bugs. No old links. No borrowed reputation.
              Just constraints, interfaces, memory, latency, failure paths, and code that survives reality.
            </p>
          </div>

          <div class="dock" aria-label="engineering taste">
            <article class="mini">
              <strong>deterministic</strong>
              <span>State should not require faith.</span>
            </article>

            <article class="mini">
              <strong>explicit</strong>
              <span>Ownership should be visible.</span>
            </article>

            <article class="mini">
              <strong>low-level</strong>
              <span>The machine always has receipts.</span>
            </article>
          </div>
        </div>

        <aside class="side" aria-label="side information">
          <div class="code-card">
            <div class="window" aria-hidden="true">
              <span class="dot"></span>
              <span class="dot"></span>
              <span class="dot"></span>
            </div>

            <pre><span class="muted">// operating mode</span>
<span class="kw">while</span> (unknown) {
    <span class="fn">inspect</span>();
    <span class="fn">simplify</span>();
    <span class="fn">remove_noise</span>();

    <span class="kw">if</span> (<span class="str">"reality"</span> != target) {
        <span class="kw">continue</span>;
    }

    <span class="fn">ship_less</span>();
}</pre>
          </div>

          <div class="license-card">
            <span class="label">license mood</span>
            <b>WTFPL</b>
            <p>Not because chaos is the goal. Because sometimes the cleanest interface is the one with no ceremony.</p>
          </div>
        </aside>
      </div>
    </section>

    <div class="bottom" aria-label="footer">
      <span>single static page · atmospheric glass · zero legacy trail</span>
      <span>observe carefully</span>
    </div>
  </main>
</body>
</html>

[---](./index_atmospheric_glass_profile.html)