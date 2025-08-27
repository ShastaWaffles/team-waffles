<style>
.projects {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
  margin-top: 16px;

  /* expand wider */
  max-width: 1000px;   /* choose your width */
  margin-left: auto;
  margin-right: auto;
}
  @media (min-width: 700px) {
    .projects { grid-template-columns: 1fr 1fr; }
  }

  .project-card {
    position: relative;
    display: flex;
    align-items: center;
    gap: 14px;
    padding: 14px 16px;
    border-radius: 14px;
    text-decoration: none;
    border: 1px solid #2f3136;
    background: #1f2227;
    transition: transform .12s ease, box-shadow .12s ease, border-color .12s ease;
  }
  .project-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 18px rgba(0,0,0,.25);
    border-color: #3b3f47;
  }

  .project-icon {
    width: 56px;
    height: 56px;
    border-radius: 12px;
    flex: 0 0 56px;
    object-fit: cover;
    background: #2c2f33;
  }

  .project-text {
    display: grid;
    gap: 4px;
    min-width: 0;
  }
  .project-title {
    font: 700 16px/1.2 system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
    color: #ffffff;
    margin: 0;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .project-desc {
    font: 400 14px/1.5 system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
    color: #c9d1d9;
    margin: 0;
  }

  /* 🔹 Badges */
  .project-badges {
    position: absolute;
    top: 10px;
    right: 14px;
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
  }
  .project-badge {
    font: 600 11px/1 system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
    padding: 4px 8px;
    border-radius: 999px;
    background: #5865F2;
    color: white;
    white-space: nowrap;
  }
  .badge-green { background:#43B581; }
  .badge-red   { background:#F04747; }
  .badge-gray  { background:#747F8D; }

  /* Light mode */
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

  <a href="index.html" style="color:white; text-decoration:none; font-weight:bold; font-family:Arial, sans-serif;">🏠 Team Home</a>
  <a href="" style="color:white; text-decoration:none; font-weight:bold; font-family:Arial, sans-serif;">📜 Contact</a>

</div>

# About
- Team Waffles is currently a solo development team that is operated by @ShastaWaffles (Github) / @wafflesaresomething (Discord)

# Projects
<div class="projects">

  <a class="project-card" href="cranagram.html" aria-label="Open Cranagram project">
    <img class="project-icon" src="cranagram-squared.png" alt="Cranagram icon">
    <div class="project-text">
      <h3 class="project-title">Cranagram - The Discord Activity</h3>
      <p class="project-desc">Unscramble the words! New words to unscramble every 12 hours for fresh fun. This is the Discord activity that has Cranagram.com integrated within, with some extra fun features such as leaderboards, so you can show your friends how much of a nerd you are! Show your friends how fast you can unscramble these words! </p>
    </div>
    <div class="project-badges">
      <span class="project-badge">Discord</span>
      <span class="project-badge badge-gray">Development</span>
    </div>
  </a>

</div>
