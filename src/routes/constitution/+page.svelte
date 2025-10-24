<script>
  // +page.svelte style single-file Svelte component
  export let data;

  const constitution = {
    title: "The Stone Toad Steve Austin Memorial Dynasty League Constitution",
    lastUpdated: "September 3, 2025",
  };
</script>

<style>
  /* Page layout approximating the format of a typical +page.svelte
     - centered title
     - narrow content column with side margins
     - modest header sizes for better proportion
  */
  :global(body) {
    margin: 0;
    font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    background: #fff;
    color: #111;
  }

  .page {
    max-width: 900px;
    margin: 2.5rem auto;
    padding: 1.5rem;
  }

  .title {
    text-align: center;
    margin-bottom: 1rem;
    font-size: 1.25rem; /* smaller title for better proportion */
    font-weight: 700;
  }

  .meta {
    text-align: center;
    font-size: 0.9rem;
    color: #444;
    margin-bottom: 1.75rem;
  }

  h2 {
    font-size: 1rem; /* smaller headers */
    margin-top: 1.25rem;
    margin-bottom: 0.5rem;
  }

  p, li {
    font-size: 0.95rem;
    line-height: 1.5;
  }

  ul, ol {
    margin-left: 1.15rem;
  }

  .section {
    margin-bottom: 1.25rem;
  }

  .muted {
    color: #666;
    font-size: 0.9rem;
  }

  .note {
    margin-top: 1rem;
    padding: 0.75rem;
    border-left: 3px solid #eee;
    background: #fafafa;
  }

  .danger {
    color: #8b0000;
    font-weight: 700;
  }

  /* Ensure page has side margins on narrow screens */
  @media (max-width: 640px) {
    .page { padding: 1rem; margin: 1rem; }
    .title { font-size: 1.1rem; }
    h2 { font-size: 0.98rem; }
  }
</style>

<main class="page">
  <h1 class="title">{constitution.title}</h1>
  <div class="meta">Official and current as of {constitution.lastUpdated}</div>

  <section class="section">
    <h2>Roster Format</h2>
    <ul>
      <li>1 QB</li>
      <li>2 RB</li>
      <li>2 WR</li>
      <li>1 TE</li>
      <li>1 FLEX</li>
      <li>1 SUPER FLEX</li>
      <li>1 Defense</li>
      <li>1 Kicker</li>
    </ul>
    <p class="muted">—--------------------------------------------------------</p>
    <ul>
      <li>10 starters</li>
      <li>14 Bench Slots</li>
      <li>2 IR Slots</li>
      <li>3 Taxi Squad slots (Taxi squad locks at Week 1 of regular season, players can be promoted from the taxi squad but cannot be moved back. Players can be on the taxi squad for a maximum of 3 years).</li>
    </ul>
  </section>

  <section class="section">
    <h2>Scoring</h2>
    <p>Standard ESPN Scoring with the following modifications:</p>
    <ul>
      <li>0.5 PPR</li>
      <li>Kicker scoring is re-balanced to lessen the position’s impact on team performance</li>
      <li>Made field goals are 3 points for any distance, 0-59 yards.</li>
      <li>60+ yard field goals are 5 points.</li>
      <li>-1 point for missed attempts</li>
      <li>A fumble is -1 point. A fumble lost is -1 point. (A fumble that is recovered by the player's team would therefore only be -1 point)</li>
    </ul>
  </section>

  <section class="section">
    <h2>Trades</h2>
    <ul>
      <li>Draft Pick Trades are enabled for starter draft</li>
      <li>Trade deadline is Week 12. The trade window re-opens upon the completion of the NFL post season.</li>
      <li>Trades are pushed through manually by the commissioner as soon as possible, as long as there are no concerns over quitting or collusion.</li>
      <li>If a trade is accepted after games for this week have started, the trade will not be processed until all players involved in the trade are unlocked.</li>
    </ul>
  </section>

  <section class="section">
    <h2>Waivers</h2>
    <ul>
      <li>FAAB waivers</li>
      <li>$1,000 yearly budget, which will renew after the rookie drafts.</li>
      <li>Players and free agents are locked at the time their individual game begins and will become unlocked on the following Wednesday at 3 a.m.</li>
      <li>After being dropped, players are on waivers for one day</li>
      <li>No waivers on Sundays</li>
    </ul>
  </section>

  <section class="section">
    <h2>Rookie Drafts</h2>
    <ul>
      <li>Rookie drafts will be 4 linear rounds</li>
      <li>Players must clear roster or taxi-squad space for drafted rookies prior to the draft date.</li>
      <li>The first six draft picks will be selected via a weighted lottery amongst the six teams that miss playoffs.</li>
      <li>Lottery weights are assigned first by team record, with a tiebreaker being total roster points (points scored throughout the year on both bench and starting lineups)</li>
      <li>Rosters become locked at the end of the NFL regular season and are re-opened after the rookie draft</li>
      <li>Rookie drafts will also include any free agent players locked at the end of the prior season</li>
    </ul>
  </section>

  <section class="section">
    <h2>League Divisions and Matchups</h2>
    <p>The league consists of three divisions of four teams.</p>
    <ul>
      <li>Teams within each division will play each other twice every year, with the remaining games being played against teams of the other division.</li>
      <li>Games can end in ties</li>
    </ul>
  </section>

  <section class="section">
    <h2>Playoffs and Toilet Bowl</h2>
    <ul>
      <li>The top two teams of each division make the playoffs</li>
      <li>The remaining teams then compete in a toilet bowl losers bracket to avoid being crowned last place.</li>
      <li>As teams within each division play each other twice, tiebreakers will be H2H records and then total points scored.</li>
      <li>Playoff matchups are 1 week long</li>
      <li>Playoff tiebreakers will be bench points</li>
      <li>The two division winners with the best record are given a week 1 bye.</li>
    </ul>
  </section>

  <section class="section">
    <h2>Rewards</h2>
    <p>To ensure long-term team investment, 3 years of league dues will be collected to start the league. (If the league votes on a $50 buy-in, $150 would be collected in year one, this covers the dues for the next two seasons).</p>
    <p>Yearly payout structure would go as follows:</p>
    <ul>
      <li>50% of the pot goes to first place</li>
      <li>25% of the pot goes to second place</li>
      <li>8.3% of the pot goes to third place (player gets their money back)</li>
      <li>16.7% of the pot goes into a BTC purchase.</li>
    </ul>
    <p>16.7% of the initial three year pay in will go to the purchase of Bitcoin. At the end of the three year cycle, the equivalent amount of Bitcoin is paid to the team with the highest win percentage in the league over that three year cycle (Points scored would be the tiebreaker).</p>
    <p class="muted">For example, a $200 BTC purchase 3 years ago in August 2022 would now be worth roughly $1,000 today</p>

    <p>Based on the $50 buy in we agreed upon for years 1-3 the yearly payout is:</p>
    <ul>
      <li>1st place = $350 ($300 plus the $50 payment from last place)</li>
      <li>2nd place = $150</li>
      <li>3rd place = $50</li>
      <li>BTC contribution = $100 (upfront purchase would be $300, taken from the entire 3 year pot)</li>
    </ul>
  </section>

  <section class="section">
    <h2>Punishments</h2>
    <p>As this is a dynasty league, rebuilds and youthful approaches to roster construction is a valid strategy. While every team should strive to win every year, a losing or poor season can be a part of any process towards building a competitive roster, and long-term strategies are encouraged.</p>
    <ul>
      <li>The last place team (team that loses the loser’s bracket, not the regular season last place team) will have to make an additional $50 buy in payment that will benefit that year’s champion</li>
    </ul>

    <div class="note">
      <p><strong>Note:</strong></p>
      <p>"I can tickle anyone in the league at any time with or without cause."</p>
      <p class="danger">"I am allowed to kill people"</p>
    </div>
  </section>

  <section class="section">
    <h2>Updates</h2>
    <p>This league constitution is official and current as of {constitution.lastUpdated}. Any updates to the constitution from this point forward will be documented below:</p>
    <pre class="muted">Updates

xxxxxx</pre>
  </section>
</main>
