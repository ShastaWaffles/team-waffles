<style>
  .version-table {
    width: 100%;
    border-collapse: collapse;
    margin: 24px 0;
    font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
    font-size: 14px;
  }
  .version-table th, .version-table td {
    padding: 12px 16px;
    text-align: left;
    border-bottom: 1px solid #2f3136;
  }
  .version-table th {
    background: #1f2227;
    color: #fff;
    font-weight: 700;
  }
  .version-table tr:nth-child(even) {
    background: #2c2f33;
  }
  .version-table tr:nth-child(odd) {
    background: #23272a;
  }
  .version-badge {
    display: inline-block;
    padding: 4px 8px;
    border-radius: 999px;
    font-size: 12px;
    font-weight: 600;
    color: #fff;
  }
  .badge-beta   { background: linear-gradient(135deg, #5865F2, #4752C4); }
  .badge-stable { background: linear-gradient(135deg, #43B581, #2E8B57); }
  .badge-upcoming { background: linear-gradient(135deg, #FAA61A, #E67E22); }
  .badge-release { background: linear-gradient(135deg, #9B59B6, #6D3C91); }

    .latest-version {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: #1f2227;
    border: 1px solid #2f3136;
    border-radius: 14px;
    padding: 16px 20px;
    margin: 20px 0;
    box-shadow: 0 6px 18px rgba(0,0,0,.25);
    font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
  }
  .latest-info {
    display: flex;
    flex-direction: column;
    gap: 6px;
  }
  .latest-title {
    font-size: 16px;
    font-weight: 700;
    color: #fff;
    margin: 0;
  }
  .latest-desc {
    font-size: 14px;
    color: #c9d1d9;
    margin: 0;
  }
</style>

<div class="latest-version">
  <div class="latest-info">
    <p class="latest-title">🚀 Latest Version: <span class="version-badge badge-beta">0.4.0-beta.1</span></p>
    <p class="latest-desc">First public beta — leaderboards and core scramble gameplay are live.</p>
  </div>
  <div>
    <p class="latest-desc">Released: 2025-08-27</p>
  </div>
</div>

<h2>📜 Cranagram Version History</h2>
<table class="version-table">
  <thead>
    <tr>
      <th>Version</th>
      <th>Date</th>
      <th>Changes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><span class="version-badge badge-beta">0.4.0-beta.1</span></td>
      <td>2025-08-27</td>
      <td>First public beta. Added leaderboards, core scramble gameplay is stable.</td>
    </tr>
    <tr>
      <td><span class="version-badge badge-beta">0.4.0-beta.2</span></td>
      <td>2025-09-??</td>
      <td>Bug fixes and small balance tweaks to the scoring system.</td>
    </tr>
    <tr>
      <td><span class="version-badge badge-beta">0.4.0-beta.3</span></td>
      <td>upcoming</td>
      <td>UI polish (better banners, icons, smoother activity start flow).</td>
    </tr>
    <tr>
      <td><span class="version-badge badge-beta">0.4.0-beta.4</span></td>
      <td>upcoming</td>
      <td>Stability updates + improved leaderboard storage backend.</td>
    </tr>
  </tbody>
</table>
