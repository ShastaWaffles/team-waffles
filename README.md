<style>
  /* Section wrapper: wider than the theme’s default content width */
.projects-wrap {
  max-width: 100%;     /* never exceed parent width */
  margin: 0 auto;      /* keep centered */
}

  .projects-grid {
    display: grid;
    grid-template-columns: 1fr; /* 1 column on mobile */
    gap: 18px;
  }
  @media (min-width: 880px) {
    .projects-grid { grid-template-columns: 1fr 1fr; } /* 2 columns on desktop */
  }

  .project-card {
    box-sizing: border-box;
    position: relative;
    display: flex;
    align-items: center;
    gap: 14px;
    padding: 16px 18px;
    border-radius: 14px;
    text-decoration: none;
    border: 1px solid #2f3136;
    background: #1f2227;
    transition: transform .12s ease, box-shadow .12s ease, border-color .12s ease;
    width: 100%;                 /* make each card span its grid cell */
  }
  .project-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 18px rgba(0,0,0,.25);
    border-color: #3b3f47;
  }

  .project-icon {
    width: 64px; height: 64px;
    border-radius: 12px;
    flex: 0 0 64px;
    object-fit: cover;
    background: #2c2f33;
  }

  .project-text { display: grid; gap: 6px; min-width: 0; }
  .project-title {
    font: 700 17px/1.25 system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
    color: #fff; margin: 0;
    white-space: nowrap; overflow: hidden; text-overflow: ellipsis;
  }
  .project-desc {
    max-width: 80ch; /* keeps text readable */
    font: 400 14px/1.55 system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
    color: #c9d1d9; margin: 0;
  }

  /* Corner badges */
  .project-badges {
    position: absolute;
    top: 10px; right: 14px;
    display: flex; gap: 6px; flex-wrap: wrap;
  }
 /* Base badge */
.project-badge { 
  font: 600 11px/1 system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
  padding: 4px 8px;
  border-radius: 999px;
  color: #fff;
  white-space: nowrap;
  background: #5865F2; /* fallback */
  background-size: 200% 200%;
  transition: background-position 0.3s ease;
}
.project-badge:hover {
  background-position: right center; /* animate gradient on hover */
}

/* Gradient variants */
.badge-blue {
  background: linear-gradient(135deg, #5865F2, #4752C4);
}
.badge-green {
  background: linear-gradient(135deg, #43B581, #2E8B57);
}
.badge-red {
  background: linear-gradient(135deg, #F04747, #C0392B);
}
.badge-gray {
  background: linear-gradient(135deg, #747F8D, #4F545C);
}
.badge-yellow {
  background: linear-gradient(135deg, #FAA61A, #E67E22);
}
.badge-orange {
  background: linear-gradient(135deg, #F26522, #D35400);
}
.badge-purple {
  background: linear-gradient(135deg, #9B59B6, #6D3C91);
}
.badge-pink {
  background: linear-gradient(135deg, #E91E63, #C2185B);
}
.badge-teal {
  background: linear-gradient(135deg, #1ABC9C, #148F77);
}
.badge-black {
  background: linear-gradient(135deg, #23272A, #0D0D0D);
  color: #fff;
}
.badge-white {
  background: linear-gradient(135deg, #ffffff, #f3f4f6);
  color: #111827;
  border: 1px solid #ddd;
}

/* External link icon — always visible */
.project-link-icon {
  position: absolute;
  bottom: 10px;
  right: 14px;
  width: 14px;
  height: 14px;
  opacity: 1;                 /* <- always visible */
  fill: currentColor;
  color: #c9d1d9;             /* dark theme */
  transition: transform 0.2s ease;
}
.project-card:hover .project-link-icon {
  transform: translateY(-1px);
}

/* Light mode color */
@media (prefers-color-scheme: light) {
  .project-link-icon { color: #6b7280; } /* slate-500 */
}


  /* Light mode adjustments */
  @media (prefers-color-scheme: light) {
    .project-card { background:#fff; border-color:#e5e7eb; }
    .project-card:hover { border-color:#d1d5db; box-shadow:0 6px 18px rgba(0,0,0,.08); }
    .project-title { color:#111827; }
    .project-desc { color:#374151; }
    .project-icon { background:#f3f4f6; }
  }
</style>


<div style="
  background-color:#2c2f33;
  padding: 12px;
  display:flex;
  justify-content:center;
  gap: 30px;
  border-radius: 8px;
  margin-bottom: 20px;
">

  <a href="" style="color:white; text-decoration:none; font-weight:bold; font-family:Arial, sans-serif;">📜 Contact</a>

</div>

# About
- Team Waffles is currently a solo development team that is operated by @ShastaWaffles (Github) / @wafflesaresomething (Discord)

# Projects
<div class="projects-wrap">

  <a class="project-card" href="cranagram.html" aria-label="Open Cranagram project">
    <img class="project-icon" src="cranagram-squared.png" alt="Cranagram icon">
    <div class="project-text">
      <h3 class="project-title">Cranagram - The Discord Activity</h3>
      <p class="project-desc">Unscramble the words! New words to unscramble every 12 hours for fresh fun. This is the Discord activity that has Cranagram.com integrated within, with some extra fun features such as leaderboards, so you can show your friends how much of a nerd you are! Show your friends how fast you can unscramble these words! </p>
    </div>
    <div class="project-badges">
      <span class="project-badge badge-blue">Discord App</span>
      <span class="project-badge badge-gray">In Development</span>
      <span class="project-badge badge-yellow">v0.5.2-BETA</span>
    </div>
      <svg class="project-link-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
    <path d="M14 3h7v7h-2V6.41l-9.29 9.3-1.42-1.42 9.3-9.29H14V3zM5 5h5V3H5c-1.1 
    0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 
    2-2v-5h-2v5H5V5z"/>
  </svg>
  </a>

</div>

# Discord
<iframe src="https://discord.com/widget?id=734547551931596961&theme=dark" width="350" height="500" allowtransparency="true" frameborder="0" sandbox="allow-popups allow-popups-to-escape-sandbox allow-same-origin allow-scripts"></iframe>

