<iframe id="iframe-03" frameborder="0" sandbox="allow-scripts allow-same-origin allow-forms allow-popups allow-presentation allow-top-navigation" src="javascript: window.frameElement.getAttribute(&quot;srcdoc&quot;);" srcdoc="&lt;script&gt;window.onmessage = function(event) {event.source.postMessage({iframeId: event.data, scrollHeight: document.body.getBoundingClientRect().height || document.body.scrollHeight}, event.origin);};&lt;/script&gt;&lt;body style='margin: 0'&gt;&lt;!doctype html&gt;
&lt;html lang=&quot;en&quot;&gt;
&lt;head&gt;
&lt;meta charset=&quot;utf-8&quot; /&gt;
&lt;meta name=&quot;viewport&quot; content=&quot;width=device-width,initial-scale=1&quot; /&gt;
&lt;title&gt;AP Gov — Constitution Flashcards&lt;/title&gt;





&lt;style&gt;
/* ===== Modern, mobile-first theme — UI-only (no JS changes) ===== */
:root {
  --bg: radial-gradient(900px 600px at 15% -10%, #0b1220 0%, #0a0f1c 35%, #090d17 70%, #070a12 100%);
  --panel: rgba(18, 22, 35, 0.72);
  --ink: #e9eef7;
  --muted: #9fb0c8;
  --accent: #8b5cf6;    /* violet */
  --accent-2: #22d3ee;  /* cyan */
  --ok: #a7f3d0;        /* answer text */
  --exp: #f5d0fe;       /* explanation text */
  --rule: rgba(255,255,255,.10);
}

html, body {
  height: 100%;
  margin: 0;
  background: var(--bg);
  color: var(--ink);
  font-family: Inter, ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, &quot;Helvetica Neue&quot;, Arial;
  -webkit-font-smoothing: antialiased;
  text-rendering: optimizeLegibility;
}

.wrap { max-width: 980px; margin: 0 auto; padding: 18px; }

.card {
  background: var(--panel);
  border-radius: 20px;
  padding: 22px 20px 28px;
  box-shadow: 0 14px 44px rgba(0,0,0,.35), inset 0 1px 0 rgba(255,255,255,.05);
  backdrop-filter: blur(14px) saturate(140%);
  -webkit-backdrop-filter: blur(14px) saturate(140%);
  border: 1px solid var(--rule);
  min-height: 58vh;
}

h1 {
  margin: 0 0 10px;
  font-size: clamp(22px, 4.2vw, 38px);
  font-weight: 800;
  letter-spacing: .2px;
  line-height: 1.15;
  background: linear-gradient(90deg, var(--accent), var(--accent-2));
  -webkit-background-clip: text; background-clip: text; color: transparent;
}

.muted { color: var(--muted); }

/* Controls: responsive grid for cleaner layout on mobile */
.controls { display: grid; grid-template-columns: repeat(12, 1fr); gap: 10px; align-items: center; margin: 12px 0 16px; }
#start .controls &gt; * { grid-column: span 3; }
#start .controls .btn { grid-column: span 2; }
#start .controls #showAllBtn { grid-column: span 3; }
#start .controls label { grid-column: span 3; }

@media (max-width: 720px) {
  .wrap { padding: 12px; }
  .card { padding: 18px 14px 22px; border-radius: 16px; }
  .controls { grid-template-columns: 1fr; }
  #start .controls &gt; * { grid-column: auto; width: 100%; }
  .btn { width: 100%; }
}


/* --- START OF Fix overlap for Jump To (desktop + mobile) --- */
#jumpSelect {
  width: 100%;
  max-width: 360px;   /* keep the dropdown from sprawling */
}

#jumpGoBtn {
  margin-left: 8px;   /* give it breathing room on the same row */
}

/* On phones/tablets: stack the select and the button */
@media (max-width: 720px) {
  #jumpSelect {
    max-width: none;
    width: 100%;
  }
  #jumpGoBtn {
    width: 100%;
    margin-left: 0;
  }
}

/* --- END OF Fix overlap for Jump To (desktop + mobile) --- */


.btn {
  background: linear-gradient(135deg, var(--accent), var(--accent-2));
  color: #0b132b;
  border: 0;
  padding: 12px 18px;
  border-radius: 14px;
  font-weight: 800;
  cursor: pointer;
  white-space: nowrap;
  box-shadow: 0 10px 22px rgba(34,211,238,.20);
  transition: transform .12s ease, box-shadow .2s ease, filter .2s ease;
  touch-action: manipulation;
}
.btn:hover { transform: translateY(-1px); box-shadow: 0 14px 26px rgba(139,92,246,.26); }
.btn:active { transform: translateY(0); filter: brightness(.96); }
.btn.secondary { background: transparent; color: var(--ink); border: 1px solid var(--rule); box-shadow: none; }

.select, .wpm { appearance: none; background: rgba(11,18,32,.6); border: 1px solid var(--rule); color: var(--ink); border-radius: 12px; padding: 10px 12px; }
select.select { background-image: linear-gradient(180deg, transparent 0, transparent 100%), url('data:image/svg+xml;utf8,&lt;svg xmlns=&quot;https://www.w3.org/2000/svg&quot; width=&quot;20&quot; height=&quot;20&quot; viewBox=&quot;0 0 24 24&quot; fill=&quot;none&quot; stroke=&quot;%239fb0c8&quot; stroke-width=&quot;2&quot; stroke-linecap=&quot;round&quot; stroke-linejoin=&quot;round&quot;&gt;&lt;polyline points=&quot;6 9 12 15 18 9&quot;/&gt;&lt;/svg&gt;'); background-repeat: no-repeat; background-position: right 10px center; padding-right: 36px; }

/* Range track/thumb polish */
input.wpm[type=range] { height: 36px; background: transparent; }
input.wpm[type=range]::-webkit-slider-runnable-track { height: 6px; background: linear-gradient(90deg, var(--accent), var(--accent-2)); border-radius: 999px; }
input.wpm[type=range]::-webkit-slider-thumb { -webkit-appearance: none; appearance: none; width: 22px; height: 22px; border-radius: 50%; background: #fff; border: 2px solid rgba(0,0,0,.25); margin-top: -8px; box-shadow: 0 3px 8px rgba(0,0,0,.35); }
input.wpm[type=range]::-moz-range-track { height: 6px; background: linear-gradient(90deg, var(--accent), var(--accent-2)); border-radius: 999px; }
input.wpm[type=range]::-moz-range-thumb { width: 22px; height: 22px; border-radius: 50%; background: #fff; border: 2px solid rgba(0,0,0,.25); box-shadow: 0 3px 8px rgba(0,0,0,.35); }

.stage { margin-top: 8px; }
.q, .a { font-size: clamp(22px, 5.4vw, 36px); line-height: 1.35; margin: clamp(18px, 5vw, 32px) 0; word-wrap: break-word; letter-spacing: .1px; }
.a { color: var(--ok); }
.exp { font-size: clamp(18px, 3.8vw, 24px); line-height: 1.55; margin: clamp(22px, 6vw, 40px) 0; color: var(--exp); word-wrap: break-word; }

.keyhint { font-size: 13px; color: var(--muted); }
.sep { height: 1px; background: var(--rule); margin: 16px 0; }
.progress { margin-top: 6px; font-size: 13px; color: var(--muted); }
.hidden { display: none; }

.allitem { padding: 16px 0 24px; border-bottom: 1px solid var(--rule); }
.allitem .index { font-weight: 700; color: var(--muted); margin-bottom: 6px; }
.row { display: flex; gap: 10px; align-items: center; flex-wrap: wrap; }
.spacer { flex: 1 1 auto; }
.mini { font-size: 12px; color: var(--muted); margin-left: 6px; }

/* Focus styles for a11y */
:focus-visible { outline: 3px solid rgba(34,211,238,.55); outline-offset: 2px; border-radius: 10px; }

@media print {
  body { background: white; color: black; }
  .card { box-shadow: none; background: white; }
  .btn, .controls, .keyhint { display: none !important; }
  .q, .a, .exp { color: black; }
}

/* Light mode tweaks */
@media (prefers-color-scheme: light) {
  :root { --bg: linear-gradient(180deg, #f8fafc 0%, #eef2ff 100%); --panel: rgba(255,255,255,.9); --ink: #0b1220; --muted:#5b6b86; --rule: rgba(11,18,32,.12); }
  .a { color: #065f46; }
  .exp { color: #6b21a8; }
  .btn { color:#0b132b; }
}
/* --- Global mobile nav bar (fixed at bottom; shown only on small screens) --- */
.global-navpad {
  position: fixed;
  left: 0; right: 0; bottom: 0;
  padding: 10px 16px calc(10px + env(safe-area-inset-bottom));
  gap: 12px;
  background: linear-gradient(180deg, rgba(0,0,0,0) 0%, rgba(0,0,0,.35) 40%, rgba(0,0,0,.65) 100%);
  backdrop-filter: blur(6px);
  -webkit-backdrop-filter: blur(6px);
  z-index: 50;
  display: none; /* hidden by default, enabled via media query */
}
.global-navpad .bigbtn {
  font-size: clamp(18px, 4.8vw, 22px);
  padding: 16px 18px;
  min-height: 56px;
  border-radius: 14px;
  width: 100%;
}
/* Only show on narrower screens, and reserve space so content isn't covered */
@media (max-width: 900px) {
  .global-navpad { display: grid; grid-template-columns: 1fr 1fr; }
  body.has-nav #quiz { padding-bottom: 110px; }
}
@media print { .global-navpad { display: none !important; } }
&lt;/style&gt;





&lt;/head&gt;
&lt;body&gt;
  &lt;div class=&quot;wrap&quot;&gt;
    &lt;!-- START SCREEN --&gt;
    &lt;div id=&quot;start&quot; class=&quot;card&quot;&gt;
      &lt;h1&gt;AP Gov — U.S. Constitution Flashcards&lt;/h1&gt;
      &lt;p class=&quot;muted&quot;&gt;
        Press &lt;strong&gt;Start&lt;/strong&gt; for flashcard mode (Question → Answer → Explanation with word-by-word reveal).
        Use &lt;strong&gt;Space/Enter/→&lt;/strong&gt; to advance, &lt;strong&gt;←/Backspace&lt;/strong&gt; to go back.
      &lt;/p&gt;
      &lt;div class=&quot;controls&quot;&gt;
        &lt;label&gt;&lt;input type=&quot;checkbox&quot; id=&quot;randomize&quot;&gt; Randomize&lt;/label&gt;
        &lt;label&gt;Reading speed:
          &lt;input type=&quot;range&quot; id=&quot;wpm&quot; class=&quot;wpm&quot; min=&quot;300&quot; max=&quot;500&quot; step=&quot;10&quot; value=&quot;400&quot;&gt;
          &lt;span id=&quot;wpmLabel&quot; class=&quot;mini&quot;&gt;400 wpm&lt;/span&gt;
        &lt;/label&gt;
        &lt;button class=&quot;btn&quot; id=&quot;startBtn&quot;&gt;Start&lt;/button&gt;

        &lt;span class=&quot;spacer&quot;&gt;&lt;/span&gt;

        &lt;button class=&quot;btn secondary&quot; id=&quot;showAllBtn&quot;&gt;Show All (Printable)&lt;/button&gt;

        &lt;!-- Jump To controls --&gt;
        &lt;label&gt;Jump to:
          &lt;select id=&quot;jumpSelect&quot; class=&quot;select&quot;&gt;&lt;/select&gt;
        &lt;/label&gt;
        &lt;button class=&quot;btn secondary&quot; id=&quot;jumpGoBtn&quot;&gt;Go&lt;/button&gt;
      &lt;/div&gt;
      &lt;div class=&quot;keyhint&quot;&gt;Tip: Click inside the card once you start so keyboard shortcuts work.&lt;/div&gt;
    &lt;/div&gt;

    &lt;!-- QUIZ SCREEN --&gt;
    &lt;div id=&quot;quiz&quot; class=&quot;card hidden&quot; tabindex=&quot;0&quot; aria-live=&quot;polite&quot;&gt;
      &lt;div class=&quot;row&quot; style=&quot;justify-content: space-between;&quot;&gt;
        &lt;div id=&quot;progress&quot; class=&quot;progress&quot;&gt;&lt;/div&gt;
        &lt;div class=&quot;controls&quot;&gt;
          &lt;button class=&quot;btn secondary&quot; id=&quot;backToStart1&quot;&gt;Back to Start&lt;/button&gt;
        &lt;/div&gt;
      &lt;/div&gt;
      &lt;div id=&quot;stage&quot; class=&quot;stage&quot;&gt;&lt;/div&gt;
      &lt;div class=&quot;sep&quot;&gt;&lt;/div&gt;
      &lt;div class=&quot;keyhint&quot;&gt;Space/Enter/→: advance • ←/Backspace: back • Click inside this card to ensure keys work.&lt;/div&gt;
    &lt;/div&gt;

    &lt;!-- ALL CARDS (PRINTABLE) --&gt;
    &lt;div id=&quot;all&quot; class=&quot;card hidden&quot;&gt;
      &lt;div class=&quot;row&quot; style=&quot;justify-content: space-between;&quot;&gt;
        &lt;h1&gt;All Cards — Typed Out&lt;/h1&gt;
        &lt;div class=&quot;controls&quot;&gt;
          &lt;button class=&quot;btn&quot; id=&quot;printBtn&quot;&gt;Print&lt;/button&gt;
          &lt;button class=&quot;btn secondary&quot; id=&quot;backToStart2&quot;&gt;Back to Start&lt;/button&gt;
        &lt;/div&gt;
      &lt;/div&gt;
      &lt;div class=&quot;muted&quot; style=&quot;margin-bottom: 12px;&quot;&gt;
        Order: &lt;span id=&quot;allOrderLabel&quot;&gt;Original&lt;/span&gt; • Reading speed (flashcards): &lt;span id=&quot;wpmEcho&quot;&gt;220&lt;/span&gt; wpm
      &lt;/div&gt;
      &lt;div id=&quot;allList&quot;&gt;&lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;

&lt;!-- Global mobile nav (outside the card) --&gt;
&lt;div id=&quot;navpadGlobal&quot; class=&quot;global-navpad hidden&quot;&gt;
  &lt;button class=&quot;btn secondary bigbtn&quot; id=&quot;globalBack&quot; aria-label=&quot;Back&quot;&gt;← Back&lt;/button&gt;
  &lt;button class=&quot;btn bigbtn&quot; id=&quot;globalNext&quot; aria-label=&quot;Next&quot;&gt;Next →&lt;/button&gt;
&lt;/div&gt;

&lt;script&gt;

const CARDS = [
  /* ===================== Foundations (1–15) ===================== */
  { q: &quot;What taxation flaw doomed the Articles of Confederation?&quot;,
    a: &quot;Congress had no power to levy taxes; it could only request money from the states.&quot;,
    exp: &quot;Without an independent revenue stream the national government could not pay debts, fund defense, or run basic operations, which exposed the system's weakness and pushed leaders toward a new constitution.&quot; },
  { q: &quot;Why did the Articles’ lack of an executive branch matter?&quot;,
    a: &quot;There was no national officer to enforce laws or lead during crises.&quot;,
    exp: &quot;Even when Congress made decisions, states could ignore them because no single executive had authority to implement or coordinate action across the union.&quot; },
  { q: &quot;What problem flowed from the Articles’ lack of a national judiciary?&quot;,
    a: &quot;There was no uniform court system to resolve disputes among states or interpret national laws.&quot;,
    exp: &quot;Conflicting state rulings and unanswered questions about interstate issues made the union unstable and undermined the rule of law across state lines.&quot; },
  { q: &quot;Why did large states resist the Articles’ one‑state, one‑vote rule?&quot;,
    a: &quot;Representation ignored population size, giving small states equal power in Congress.&quot;,
    exp: &quot;Citizens in bigger states had proportionally less influence, which felt undemocratic and fueled calls for representation that reflected the people as well as the states.&quot; },
  { q: &quot;Why were amendments under the Articles nearly impossible to pass?&quot;,
    a: &quot;They required unanimous approval by all thirteen states.&quot;,
    exp: &quot;Any single state could veto needed reforms, freezing the system even when most agreed change was necessary.&quot; },
  { q: &quot;What defense weakness did the Articles create?&quot;,
    a: &quot;The national government lacked a reliable standing military force.&quot;,
    exp: &quot;With no assured funding or command structure, the union was slow and inconsistent in responding to threats or rebellions.&quot; },
  { q: &quot;What did Shays’ Rebellion reveal about the Articles of Confederation?&quot;,
    a: &quot;It exposed the national government’s inability to maintain order and support state stability.&quot;,
    exp: &quot;Massachusetts struggled to respond to the uprising, highlighting the need for a stronger central government that could help preserve domestic tranquility.&quot; },
  { q: &quot;Who were two leading Federalists, and what did they argue?&quot;,
    a: &quot;James Madison and Alexander Hamilton argued for a stronger national government constrained by structural checks.&quot;,
    exp: &quot;They believed that careful design—separation of powers, checks and balances, and federalism—could create energy in government without inviting tyranny.&quot; },
  { q: &quot;Who were two notable Anti‑Federalists, and what did they demand?&quot;,
    a: &quot;Patrick Henry and George Mason demanded explicit protections for individual rights.&quot;,
    exp: &quot;They feared consolidated power and insisted that a bill of rights be added so basic liberties would be beyond government reach.&quot; },
  { q: &quot;According to Federalists, what solved the problem of disorder in the states?&quot;,
    a: &quot;A stronger national government balanced by checks and balances would provide stability without sacrificing liberty.&quot;,
    exp: &quot;Institutional design—not mere trust in leaders—was Madison’s answer to faction and conflict.&quot; },
  { q: &quot;What did Anti‑Federalists insist on to safeguard liberty?&quot;,
    a: &quot;They insisted on a Bill of Rights as a condition for broad support of the Constitution.&quot;,
    exp: &quot;Clear, textual guarantees for speech, religion, due process, and more would reassure citizens that the new government had limits.&quot; },
  { q: &quot;What is the core claim of Federalist No. 10?&quot;,
    a: &quot;A large republic is the best way to control factions and protect minority rights.&quot;,
    exp: &quot;With many diverse interests, it becomes harder for any single faction to dominate, which protects liberty better than small, uniform polities.&quot; },
  { q: &quot;What is the core claim of Federalist No. 51?&quot;,
    a: &quot;Separation of powers and checks and balances allow ambition to counteract ambition.&quot;,
    exp: &quot;Because each branch has motives to defend its turf, no branch can easily accumulate all power, keeping government limited and accountable.&quot; },
  { q: &quot;What did Brutus No. 1 fear about federal power under the new Constitution?&quot;,
    a: &quot;That the Necessary and Proper Clause and the Supremacy Clause would overpower the states.&quot;,
    exp: &quot;Brutus warned that broad federal means and legal supremacy could gradually erase meaningful state authority and local self‑government.&quot; },
  { q: &quot;Why did Brutus argue that a large republic would be impractical?&quot;,
    a: &quot;Representatives would be too distant from the people to understand and reflect local interests.&quot;,
    exp: &quot;He believed only small republics can keep officials close to citizens and responsive to their needs.&quot; },

  /* ===================== Articles I–VII (16–40) ===================== */
  { q: &quot;What does Article I establish?&quot;,
    a: &quot;Article I creates the legislative branch—a bicameral Congress composed of the House and the Senate.&quot;,
    exp: &quot;The House represents the people by population with short two‑year terms; the Senate represents states equally with six‑year terms to promote stability.&quot; },
  { q: &quot;What unique role does the House of Representatives have in lawmaking?&quot;,
    a: &quot;All revenue (tax) bills must originate in the House.&quot;,
    exp: &quot;Because House members are closest to the voters, the Constitution gives them the first word on raising public money.&quot; },
  { q: &quot;Name two distinctive roles of the Senate.&quot;,
    a: &quot;The Senate ratifies treaties and confirms major executive and judicial appointments.&quot;,
    exp: &quot;The Senate also tries impeachments; when the president is tried, the Chief Justice presides to reinforce impartiality.&quot; },
  { q: &quot;Give three important enumerated powers of Congress.&quot;,
    a: &quot;Congress can levy taxes, regulate interstate and foreign commerce, and declare war.&quot;,
    exp: &quot;Other listed powers include coining money, establishing federal courts, raising and supporting armies, and maintaining a navy.&quot; },
  { q: &quot;What does the Necessary and Proper (Elastic) Clause authorize?&quot;,
    a: &quot;It allows Congress to pass laws needed to carry out its enumerated powers.&quot;,
    exp: &quot;This clause creates implied powers—flexibility to choose reasonable means to achieve constitutionally assigned ends.&quot; },
  { q: &quot;What does the Commerce Clause empower Congress to do?&quot;,
    a: &quot;It authorizes Congress to regulate trade among the states and with foreign nations.&quot;,
    exp: &quot;Over time it became a central basis for federal economic policy and many civil‑rights protections affecting interstate activities.&quot; },
  { q: &quot;Give two limits Article I places on Congress.&quot;,
    a: &quot;Congress may not pass bills of attainder or ex post facto laws.&quot;,
    exp: &quot;Other limits include no taxes on exports, no titles of nobility, protection of habeas corpus except in emergencies, and spending only by appropriation.&quot; },
  { q: &quot;How is impeachment divided between the House and the Senate?&quot;,
    a: &quot;The House impeaches (brings charges); the Senate conducts the trial and may convict and remove.&quot;,
    exp: &quot;For presidential trials the Chief Justice presides; conviction requires a two‑thirds Senate vote, underscoring its seriousness.&quot; },
  { q: &quot;What does Article II establish?&quot;,
    a: &quot;Article II establishes the executive branch headed by the President of the United States.&quot;,
    exp: &quot;The President executes the laws, serves as Commander in Chief, negotiates treaties, and appoints key officials—subject to checks by the other branches.&quot; },
  { q: &quot;Name three core presidential powers in Article II.&quot;,
    a: &quot;Serving as Commander in Chief, appointing officers and judges (with Senate consent), and negotiating treaties (subject to Senate ratification).&quot;,
    exp: &quot;These powers give the executive energy in foreign affairs and administration while the Senate’s role provides democratic oversight.&quot; },
  { q: &quot;What is the Take Care Clause in Article II?&quot;,
    a: &quot;It requires the President to ‘take care that the laws be faithfully executed.’&quot;,
    exp: &quot;This clause grounds executive enforcement authority and limits broad non‑enforcement; the President must implement duly enacted laws.&quot; },
  { q: &quot;How are presidential powers checked by the other branches?&quot;,
    a: &quot;The Senate must confirm many appointments and ratify treaties, Congress can override vetoes, and both branches share impeachment powers.&quot;,
    exp: &quot;These checks ensure cooperation across branches and prevent unilateral executive control.&quot; },
  { q: &quot;What is the impeachment standard for civil officers in Article II?&quot;,
    a: &quot;Officers may be impeached and removed for treason, bribery, or other high crimes and misdemeanors.&quot;,
    exp: &quot;The phrase captures serious abuses of public trust, leaving room for Congress to judge misconduct that threatens constitutional governance.&quot; },
  { q: &quot;What does Article III establish?&quot;,
    a: &quot;Article III creates the judicial branch and vests the judicial power in one Supreme Court and any inferior courts Congress creates.&quot;,
    exp: &quot;It outlines jurisdiction and protects judicial independence so courts can interpret the law without political pressure.&quot; },
  { q: &quot;How does Article III protect judicial independence?&quot;,
    a: &quot;Federal judges hold office during good behavior and cannot have their salaries reduced while in office.&quot;,
    exp: &quot;Security of tenure and pay helps judges decide cases based on law rather than politics or fear of retaliation.&quot; },
  { q: &quot;How does the Constitution define treason against the United States?&quot;,
    a: &quot;Treason consists only of levying war against the U.S. or adhering to its enemies, giving them aid and comfort.&quot;,
    exp: &quot;A conviction requires either a confession in open court or testimony of two witnesses to the same overt act, setting a high bar to protect dissent.&quot; },
  { q: &quot;What does the Full Faith and Credit Clause require of states?&quot;,
    a: &quot;States must recognize the public acts, records, and judicial proceedings of other states.&quot;,
    exp: &quot;This rule promotes legal continuity so judgments, adoptions, and other civil acts remain valid when people move across state lines.&quot; },
  { q: &quot;What is the Privileges and Immunities Clause in Article IV?&quot;,
    a: &quot;States may not discriminate against citizens of other states in fundamental matters like earning a livelihood.&quot;,
    exp: &quot;It helps maintain national unity by protecting core civil and economic rights for visitors and new residents.&quot; },
  { q: &quot;What does Article IV say about extradition?&quot;,
    a: &quot;A person charged with a crime who flees to another state must be returned to the state with jurisdiction on request.&quot;,
    exp: &quot;Extradition prevents defendants from evading justice simply by crossing state borders.&quot; },
  { q: &quot;How are new states admitted under Article IV?&quot;,
    a: &quot;Congress admits new states, and a new state cannot be formed within an existing one without consent of the state legislature and Congress.&quot;,
    exp: &quot;This process balances national growth with respect for existing state boundaries and consent.&quot; },
  { q: &quot;What does the Guarantee Clause promise to every state?&quot;,
    a: &quot;The United States shall guarantee to every state a republican form of government and protection against invasion and, on request, domestic violence.&quot;,
    exp: &quot;The clause commits the nation to representative government in the states and to mutual security in emergencies.&quot; },
  { q: &quot;What does Article V outline?&quot;,
    a: &quot;Article V provides the process to amend the Constitution.&quot;,
    exp: &quot;Amendments are proposed by two‑thirds of Congress or a convention called by two‑thirds of the states and are ratified by three‑fourths of the states.&quot; },
  { q: &quot;What does the Supremacy Clause in Article VI declare?&quot;,
    a: &quot;The Constitution, federal laws made pursuant to it, and treaties are the supreme law of the land.&quot;,
    exp: &quot;When valid federal law conflicts with state law, federal law prevails within its constitutional sphere.&quot; },
  { q: &quot;What oaths or tests does Article VI address?&quot;,
    a: &quot;All federal and state officers must swear to support the Constitution, and no religious test may ever be required for office.&quot;,
    exp: &quot;The oath binds officials to the constitutional system, while the ban on religious tests protects freedom of conscience.&quot; },
  { q: &quot;What does Article VII do?&quot;,
    a: &quot;Article VII sets the ratification process for the Constitution, providing that it would take effect after approval by nine states.&quot;,
    exp: &quot;This clause allowed the new frame of government to begin functioning without unanimity, avoiding the Articles’ paralysis.&quot; },

  /* ===================== Key Principles (41–55) ===================== */
  { q: &quot;What is popular sovereignty?&quot;,
    a: &quot;Popular sovereignty means that all governmental power ultimately comes from the people.&quot;,
    exp: &quot;The Constitution opens with ‘We the People,’ signaling that authority is delegated upward from citizens, not granted downward by rulers.&quot; },
  { q: &quot;What is republicanism?&quot;,
    a: &quot;Republicanism is rule through elected representatives who are accountable to the voters.&quot;,
    exp: &quot;This design balances responsiveness with stability, filtering public views through deliberation rather than instant, direct votes on every issue.&quot; },
  { q: &quot;What is meant by limited government and the rule of law?&quot;,
    a: &quot;Government officials are bound by the Constitution and laws; their powers are granted and constrained.&quot;,
    exp: &quot;No one is above the law, and officials may act only where the Constitution authorizes, protecting liberty from arbitrary power.&quot; },
  { q: &quot;What is separation of powers?&quot;,
    a: &quot;Separation of powers divides governmental functions among legislative, executive, and judicial branches.&quot;,
    exp: &quot;Each branch specializes and has distinct tools, making it harder for power to concentrate in any one set of hands.&quot; },
  { q: &quot;What are checks and balances?&quot;,
    a: &quot;Checks and balances are mechanisms by which each branch can restrain the others.&quot;,
    exp: &quot;Examples include the presidential veto and congressional override, the Senate’s confirmation power, judicial review, and impeachment.&quot; },
  { q: &quot;What is judicial review?&quot;,
    a: &quot;Judicial review is the power of the courts to invalidate laws or executive actions that violate the Constitution.&quot;,
    exp: &quot;Established in Marbury v. Madison, it ensures that the Constitution remains the supreme rule that binds all branches.&quot; },
  { q: &quot;What is federalism?&quot;,
    a: &quot;Federalism divides power between a national government and the states.&quot;,
    exp: &quot;The national government handles truly national problems, while states retain authority over local matters, allowing diversity with unity.&quot; },
  { q: &quot;How do enumerated powers differ from implied powers?&quot;,
    a: &quot;Enumerated powers are explicitly listed; implied powers are reasonably inferred from the Necessary and Proper Clause.&quot;,
    exp: &quot;Implied powers let Congress choose effective means—like creating a bank—to carry out its listed ends, such as taxing and spending.&quot; },
  { q: &quot;What are concurrent powers?&quot;,
    a: &quot;Concurrent powers are powers shared by both the federal government and the states.&quot;,
    exp: &quot;Typical examples include taxing, operating courts, and enforcing laws, areas where cooperation is routine.&quot; },
  { q: &quot;What are reserved powers?&quot;,
    a: &quot;Reserved powers are those not delegated to the federal government and kept by the states or the people, as the Tenth Amendment states.&quot;,
    exp: &quot;They include core ‘police powers’ like public health, safety, education, and running elections—functions closest to daily life.&quot; },
  { q: &quot;Why did the Framers make the amendment process difficult?&quot;,
    a: &quot;They required supermajorities to ensure stability while still allowing genuine consensus to change the charter.&quot;,
    exp: &quot;Hard—but not impossible—rules prevent frequent, faction‑driven rewrites and protect minority rights from sudden swings.&quot; },
  { q: &quot;What is selective incorporation?&quot;,
    a: &quot;Selective incorporation applies most of the Bill of Rights to the states through the Fourteenth Amendment’s Due Process Clause.&quot;,
    exp: &quot;Case by case, the Supreme Court recognized rights as fundamental and therefore binding on state and local governments, not just the federal government.&quot; },
  { q: &quot;Which case cemented judicial review at the federal level?&quot;,
    a: &quot;Marbury v. Madison established that the Supreme Court can strike down unconstitutional laws.&quot;,
    exp: &quot;The decision positioned the Court as the final interpreter of the Constitution, preventing Congress or the President from being judges in their own causes.&quot; },
  { q: &quot;Give an example of an executive check on the legislature.&quot;,
    a: &quot;The President can veto bills passed by Congress.&quot;,
    exp: &quot;The veto forces Congress to reconsider and build a two‑thirds supermajority if it wants to enact the law anyway.&quot; },
  { q: &quot;Give an example of a legislative check on the executive.&quot;,
    a: &quot;The Senate must confirm many presidential nominees and may refuse to ratify treaties.&quot;,
    exp: &quot;Congress also controls appropriations and may impeach and remove executive officers when necessary.&quot; },

  /* ========== Bill of Rights & Civil Liberties (56–80) ========== */
  { q: &quot;What freedoms does the First Amendment protect?&quot;,
    a: &quot;It protects freedom of religion, speech, press, assembly, and the right to petition the government.&quot;,
    exp: &quot;These core liberties enable democratic debate, conscience, and collective action; the government generally cannot punish expression just because it is unpopular.&quot; },
  { q: &quot;What does the Free Exercise Clause protect?&quot;,
    a: &quot;It shields individuals’ right to practice their religion without undue government interference.&quot;,
    exp: &quot;Government may enforce neutral, generally applicable laws, but it cannot target religious practices for special burdens.&quot; },
  { q: &quot;What does the Establishment Clause prohibit?&quot;,
    a: &quot;It prohibits the government from establishing an official religion or coercing religious participation.&quot;,
    exp: &quot;Schools and agencies must remain neutral toward religion, neither promoting nor disparaging faith.&quot; },
  { q: &quot;What does the Second Amendment secure?&quot;,
    a: &quot;It protects an individual right to keep and bear arms, subject to reasonable regulation.&quot;,
    exp: &quot;The Supreme Court has recognized a personal right for lawful purposes like self‑defense while allowing governments to set safety rules.&quot; },
  { q: &quot;What protection does the Third Amendment provide?&quot;,
    a: &quot;It bars the quartering of soldiers in private homes without the owner’s consent in peacetime.&quot;,
    exp: &quot;This reflects the Founders’ reaction to British abuses and their commitment to the privacy and sanctity of the home.&quot; },
  { q: &quot;What does the Fourth Amendment guard against?&quot;,
    a: &quot;It protects people from unreasonable searches and seizures and requires warrants based on probable cause.&quot;,
    exp: &quot;The amendment balances public safety with privacy by demanding specific justification before officers intrude on persons, houses, papers, or effects.&quot; },
  { q: &quot;Name two key rights in the Fifth Amendment.&quot;,
    a: &quot;The Fifth protects against self‑incrimination and double jeopardy and guarantees due process of law.&quot;,
    exp: &quot;It also includes the Takings Clause, requiring just compensation when government takes private property for public use.&quot; },
  { q: &quot;What criminal‑procedure rights does the Sixth Amendment ensure?&quot;,
    a: &quot;It guarantees a speedy, public trial by an impartial jury, the right to counsel, and the rights to confront witnesses and compel testimony.&quot;,
    exp: &quot;These safeguards make trials fair and transparent and help prevent wrongful convictions.&quot; },
  { q: &quot;What protections does the Seventh Amendment provide?&quot;,
    a: &quot;It preserves the right to a jury trial in certain civil cases.&quot;,
    exp: &quot;Civil juries allow citizens to decide factual disputes between private parties, not just criminal accusations by the state.&quot; },
  { q: &quot;What limits does the Eighth Amendment place on punishment?&quot;,
    a: &quot;It prohibits excessive bail and fines and bars cruel and unusual punishments.&quot;,
    exp: &quot;Punishments must be proportional and humane; this provision shapes debates over conditions of confinement and methods of punishment.&quot; },
  { q: &quot;What does the Ninth Amendment say about rights not listed in the Constitution?&quot;,
    a: &quot;It says that the listing of certain rights does not deny or disparage others retained by the people.&quot;,
    exp: &quot;The Ninth keeps the Bill of Rights from being read as an exhaustive catalog; liberty extends beyond expressly named guarantees.&quot; },
  { q: &quot;What principle does the Tenth Amendment affirm?&quot;,
    a: &quot;Powers not delegated to the United States nor prohibited to the states are reserved to the states or to the people.&quot;,
    exp: &quot;This amendment anchors federalism by confirming that the national government is one of limited, enumerated powers.&quot; },
  { q: &quot;How does the Fourteenth Amendment protect individual rights against states?&quot;,
    a: &quot;It forbids states from denying due process and equal protection of the laws.&quot;,
    exp: &quot;The amendment became the vehicle for selective incorporation of most Bill of Rights protections and for dismantling state‑sponsored discrimination.&quot; },
  { q: &quot;What is due process of law?&quot;,
    a: &quot;Due process means government must follow fair procedures and, in some contexts, respect fundamental rights before taking life, liberty, or property.&quot;,
    exp: &quot;Procedural due process concerns fair steps; substantive due process guards certain core liberties from arbitrary infringement.&quot; },
  { q: &quot;What does equal protection require?&quot;,
    a: &quot;States must treat similarly situated people alike unless the government has a sufficient reason to classify.&quot;,
    exp: &quot;Courts apply different levels of scrutiny to prevent invidious discrimination while allowing reasonable regulations.&quot; },
  { q: &quot;What is the exclusionary rule in Fourth Amendment law?&quot;,
    a: &quot;It bars the use of evidence obtained through unconstitutional searches or seizures.&quot;,
    exp: &quot;By excluding tainted evidence, courts deter police from violating rights and reinforce the warrant and probable‑cause requirements.&quot; },
  { q: &quot;What is the Miranda rule under the Fifth Amendment?&quot;,
    a: &quot;Before custodial interrogation, police must inform suspects of their rights, including the right to remain silent and to an attorney.&quot;,
    exp: &quot;Warnings help ensure that confessions are voluntary and that people understand they do not have to incriminate themselves.&quot; },
  { q: &quot;How does the Free Speech Clause apply to symbolic expression?&quot;,
    a: &quot;Protective coverage often extends to symbolic acts intended to communicate a message, subject to narrow limits.&quot;,
    exp: &quot;Examples include wearing armbands or burning symbols; government may regulate time, place, and manner but not suppress a viewpoint simply because it is offensive.&quot; },
  { q: &quot;What does the Establishment Clause require in public schools?&quot;,
    a: &quot;Public schools must remain religiously neutral; they may not sponsor prayer or endorse religious doctrine.&quot;,
    exp: &quot;Students retain personal religious freedom, but school officials cannot organize or pressure participation in religious activities.&quot; },
  { q: &quot;How does the Second Amendment interact with public‑safety regulations?&quot;,
    a: &quot;Courts recognize an individual right to keep and bear arms while allowing governments to enact reasonable safety rules.&quot;,
    exp: &quot;Measures like barring possession by felons or regulating dangerous places can coexist with the core right of lawful self‑defense.&quot; },
  {q:&quot;Heller’s core holding?&quot;,
   a:&quot;2A protects an individual right to own a handgun for self-defense.&quot;,
   exp:&quot;Subject to certain long-standing limits; later applied to states.&quot;},
  {q:&quot;Time, place, manner limits?&quot;,
   a:&quot;Content-neutral, narrowly tailored, leave open alternatives.&quot;,
   exp:&quot;Allows order without targeting ideas or speakers.&quot;},
  {q:&quot;What is incorporation to states?&quot;,
   a:&quot;Applying BoR protections via 14th Due Process.&quot;,
   exp:&quot;Most—but not all—rights incorporated selectively.&quot;},
  {q:&quot;Rights of the accused protect what value?&quot;,
   a:&quot;Fair process before loss of liberty or property.&quot;,
   exp:&quot;Due Process balances enforcement with individual dignity.&quot;},
  {q:&quot;Why protect unpopular speech?&quot;,
   a:&quot;To safeguard debate and minority viewpoints.&quot;,
   exp:&quot;Majority-approved speech needs no protection; dissents do.&quot;},
   
  /* ============== Federalism & Constitutional Change (81–100) ============== */
  { q: &quot;What is dual federalism?&quot;,
    a: &quot;Dual federalism envisions national and state governments operating in separate, distinct spheres.&quot;,
    exp: &quot;Think of a ‘layer‑cake’: each level has its own responsibilities with minimal overlap, a model more common in the early Republic.&quot; },
  { q: &quot;What is cooperative federalism?&quot;,
    a: &quot;Cooperative federalism features shared responsibilities and joint action by national and state governments.&quot;,
    exp: &quot;This ‘marble‑cake’ model grew with national programs that use state partners to implement federal policy.&quot; },
  { q: &quot;What is fiscal federalism?&quot;,
    a: &quot;Fiscal federalism is the use of federal funds and grants to influence state and local policy.&quot;,
    exp: &quot;Congress can encourage state priorities by attaching conditions to money, shaping policy while respecting state administration.&quot; },
  { q: &quot;How do categorical grants differ from block grants?&quot;,
    a: &quot;Categorical grants fund specific programs with detailed conditions; block grants provide broader funding with more state flexibility.&quot;,
    exp: &quot;Categorical grants steer outcomes tightly; block grants let states tailor solutions to local needs.&quot; },
  { q: &quot;What is an unfunded mandate?&quot;,
    a: &quot;It is a federal requirement that states take certain actions without providing full funding.&quot;,
    exp: &quot;Mandates can advance national goals but strain state budgets, sparking debates about fairness and federal overreach.&quot; },
  { q: &quot;Why is McCulloch v. Maryland a landmark for federal power?&quot;,
    a: &quot;It upheld implied powers under the Necessary and Proper Clause and barred states from taxing valid federal operations.&quot;,
    exp: &quot;The decision affirmed a broad reading of national authority and the supremacy of federal law when acting within constitutional bounds.&quot; },
  { q: &quot;What principle did Gibbons v. Ogden establish about commerce?&quot;,
    a: &quot;It held that Congress controls interstate commerce and may override conflicting state laws.&quot;,
    exp: &quot;The ruling expanded the national reach over economic activity that crosses state lines, promoting a unified market.&quot; },
  { q: &quot;How did the New Deal era reshape federalism?&quot;,
    a: &quot;It expanded national involvement in economic and social policy, ushering in cooperative federalism.&quot;,
    exp: &quot;Federal programs used grants and partnerships to address widespread problems the states could not solve alone.&quot; },
  { q: &quot;What is the doctrine of nullification, and is it valid?&quot;,
    a: &quot;Nullification claimed a state could invalidate federal laws it deemed unconstitutional; the doctrine is not legally valid.&quot;,
    exp: &quot;The Supremacy Clause and Civil War era developments confirmed that states may not unilaterally void federal law—courts decide constitutionality.&quot; },
  { q: &quot;How does the Supremacy Clause shape federal‑state conflicts today?&quot;,
    a: &quot;When valid federal law conflicts with state law, federal law prevails within its proper scope.&quot;,
    exp: &quot;Preemption ensures national rules govern national problems while still leaving room for states to regulate in areas not occupied by federal law.&quot; },
  { q: &quot;What is preemption in federal law?&quot;,
    a: &quot;Preemption occurs when federal law displaces or overrides state law in the same field or in direct conflict.&quot;,
    exp: &quot;Congress can expressly preempt, or courts can find implied preemption where federal regulation is pervasive or inconsistent with state rules.&quot; },
  { q: &quot;What is the significance of the Spending Clause for federalism?&quot;,
    a: &quot;It lets Congress tax and spend for the general welfare, often using grants to steer state policy.&quot;,
    exp: &quot;Funding conditions can encourage nationwide standards while leaving states to implement them.&quot; },
  { q: &quot;How does incorporation change citizens’ protections against state action?&quot;,
    a: &quot;Through the Fourteenth Amendment, most federal rights now also restrict states, not just the federal government.&quot;,
    exp: &quot;Selective incorporation nationalized core civil liberties so people enjoy the same baseline protections across states.&quot; },
  { q: &quot;What is the Twenty‑Seventh Amendment’s federalism angle?&quot;,
    a: &quot;It is not about federalism; it delays congressional pay changes until after an election.&quot;,
    exp: &quot;By making salary changes take effect only after voters have their say, it promotes accountability rather than altering state–federal balance.&quot; },
  { q: &quot;What is the difference between civil liberties and civil rights?&quot;,
    a: &quot;Civil liberties are freedoms from government interference; civil rights are protections against unfair treatment by government or private actors in certain contexts.&quot;,
    exp: &quot;Liberties like speech limit what government may do; rights like equal access to voting ensure fair inclusion and opportunity.&quot; },
  { q: &quot;How did the Fifteenth and Nineteenth Amendments expand democracy?&quot;,
    a: &quot;They barred voting discrimination based on race and secured women’s suffrage, respectively.&quot;,
    exp: &quot;Together with later reforms, these amendments enlarged the electorate and made representation more reflective of the people.&quot; },
  { q: &quot;What problem does the Seventeenth Amendment address?&quot;,
    a: &quot;It established the direct election of U.S. senators by the people rather than by state legislatures.&quot;,
    exp: &quot;Direct elections increased accountability to voters and reduced deadlocks and corruption in senatorial selection.&quot; },
  { q: &quot;What does the Twenty‑Fourth Amendment prohibit?&quot;,
    a: &quot;It bans poll taxes in federal elections.&quot;,
    exp: &quot;Poll taxes were used to suppress poor and minority voters; removing them advanced the promise of equal political participation.&quot; },
  { q: &quot;Why is the Nineteenth Amendment a turning point?&quot;,
    a: &quot;It guarantees women the right to vote nationwide.&quot;,
    exp: &quot;By doubling the potential electorate, it transformed American politics and policy agendas.&quot; },
  { q: &quot;How did the Twenty‑Sixth Amendment change voting?&quot;,
    a: &quot;It lowered the voting age to eighteen for all elections.&quot;,
    exp: &quot;If young adults can be drafted and taxed, the amendment recognizes they should also have a voice in government decisions.&quot; },

  /* ===================== 27 Amendments (101–127) ===================== */
  { q: &quot;What does the First Amendment protect?&quot;,
    a: &quot;It protects freedom of religion, speech, press, assembly, and petition.&quot;,
    exp: &quot;These freedoms enable citizens to think, speak, gather, and seek change without fear of government punishment for their viewpoints.&quot; },
  { q: &quot;What does the Second Amendment protect?&quot;,
    a: &quot;It secures an individual right to keep and bear arms, subject to reasonable regulations.&quot;,
    exp: &quot;While the core right includes lawful self‑defense, governments may set safety rules consistent with constitutional limits.&quot; },
  { q: &quot;What does the Third Amendment protect?&quot;,
    a: &quot;It prohibits quartering soldiers in private homes without consent in peacetime.&quot;,
    exp: &quot;The amendment reflects the Founders’ desire to protect household privacy against military intrusion.&quot; },
  { q: &quot;What does the Fourth Amendment protect?&quot;,
    a: &quot;It guards against unreasonable searches and seizures and requires warrants based on probable cause.&quot;,
    exp: &quot;Police need specific, justified reasons before intruding on personal privacy and property.&quot; },
  { q: &quot;What does the Fifth Amendment protect?&quot;,
    a: &quot;It protects against self‑incrimination and double jeopardy and guarantees due process and just compensation for takings.&quot;,
    exp: &quot;Government must play fair in investigations, trials, and property acquisition for public use.&quot; },
  { q: &quot;What does the Sixth Amendment protect?&quot;,
    a: &quot;It guarantees a speedy, public jury trial, assistance of counsel, and confrontation and compulsory process rights.&quot;,
    exp: &quot;These ensure that criminal defendants can challenge the case against them and present a defense.&quot; },
  { q: &quot;What does the Seventh Amendment protect?&quot;,
    a: &quot;It preserves jury trials in certain civil cases.&quot;,
    exp: &quot;Civil juries bring community judgment to private disputes about money or property.&quot; },
  { q: &quot;What does the Eighth Amendment protect?&quot;,
    a: &quot;It prohibits excessive bail and fines and forbids cruel and unusual punishments.&quot;,
    exp: &quot;Punishment must be humane and proportionate to the offense.&quot; },
  { q: &quot;What does the Ninth Amendment affirm?&quot;,
    a: &quot;It affirms that people retain rights beyond those specifically listed in the Constitution.&quot;,
    exp: &quot;Liberty is wider than any list; unenumerated rights still matter.&quot; },
  { q: &quot;What does the Tenth Amendment affirm?&quot;,
    a: &quot;It reserves undelegated powers to the states or the people.&quot;,
    exp: &quot;The amendment anchors the principle of limited, enumerated federal power.&quot; },
  { q: &quot;What does the Eleventh Amendment address?&quot;,
    a: &quot;It limits certain lawsuits against states in federal court.&quot;,
    exp: &quot;The amendment strengthens state sovereign immunity from some types of suits.&quot; },
  { q: &quot;What does the Twelfth Amendment change?&quot;,
    a: &quot;It revises presidential elections so electors cast separate ballots for President and Vice President.&quot;,
    exp: &quot;The change reduced electoral deadlocks and clarified how tickets are chosen.&quot; },
  { q: &quot;What does the Thirteenth Amendment do?&quot;,
    a: &quot;It abolishes slavery and involuntary servitude, except as punishment for a crime.&quot;,
    exp: &quot;This formally ended slavery in the United States and empowered Congress to enforce that freedom.&quot; },
  { q: &quot;What does the Fourteenth Amendment do?&quot;,
    a: &quot;It grants birthright citizenship and forbids states from denying due process and equal protection.&quot;,
    exp: &quot;It nationalized civil liberties protections and became the foundation for modern civil rights law.&quot; },
  { q: &quot;What does the Fifteenth Amendment do?&quot;,
    a: &quot;It prohibits denying the right to vote on account of race, color, or previous condition of servitude.&quot;,
    exp: &quot;The amendment aimed to secure political equality for formerly enslaved people and their descendants.&quot; },
  { q: &quot;What does the Sixteenth Amendment allow?&quot;,
    a: &quot;It authorizes a federal income tax without apportionment among the states.&quot;,
    exp: &quot;This gave the national government a reliable revenue source for modern programs.&quot; },
  { q: &quot;What does the Seventeenth Amendment change?&quot;,
    a: &quot;It provides for the direct election of U.S. senators by voters in each state.&quot;,
    exp: &quot;Direct election increased democratic accountability and reduced legislative deadlocks.&quot; },
  { q: &quot;What does the Eighteenth Amendment do?&quot;,
    a: &quot;It established national prohibition of the manufacture, sale, and transportation of intoxicating liquors (later repealed).&quot;,
    exp: &quot;The policy sought to curb social harms from alcohol but proved difficult to enforce and was later reversed by the Twenty‑First Amendment.&quot; },
  { q: &quot;What does the Nineteenth Amendment do?&quot;,
    a: &quot;It guarantees women the right to vote.&quot;,
    exp: &quot;The amendment expanded the electorate and advanced political equality.&quot; },
  { q: &quot;What does the Twentieth Amendment address?&quot;,
    a: &quot;It changes the start dates of presidential and congressional terms and provides procedures if a President‑elect dies before taking office.&quot;,
    exp: &quot;By shortening the ‘lame‑duck’ period, it improves government continuity and readiness.&quot; },
  { q: &quot;What does the Twenty‑First Amendment do?&quot;,
    a: &quot;It repeals national Prohibition and allows regulation of alcohol by states.&quot;,
    exp: &quot;The amendment recognized Prohibition’s failure and returned significant control to the states.&quot; },
  { q: &quot;What does the Twenty‑Second Amendment do?&quot;,
    a: &quot;It limits the President to two elected terms (or a maximum of ten years if finishing another’s term).&quot;,
    exp: &quot;Term limits guard against concentration of executive power and encourage leadership turnover.&quot; },
  { q: &quot;What does the Twenty‑Third Amendment do?&quot;,
    a: &quot;It grants presidential electors to the District of Columbia.&quot;,
    exp: &quot;Residents of the nation’s capital gained a voice in choosing the President and Vice President.&quot; },
  { q: &quot;What does the Twenty‑Fourth Amendment do?&quot;,
    a: &quot;It bans poll taxes in federal elections.&quot;,
    exp: &quot;Poll taxes were barriers to poor and minority voters; eliminating them advanced equal access to the ballot.&quot; },
  { q: &quot;What does the Twenty‑Fifth Amendment provide?&quot;,
    a: &quot;It clarifies presidential succession and procedures for filling a vice‑presidential vacancy and for dealing with presidential disability.&quot;,
    exp: &quot;These rules ensure continuity of government when presidents die, resign, or become unable to serve.&quot; },
  { q: &quot;What does the Twenty‑Sixth Amendment do?&quot;,
    a: &quot;It lowers the voting age to eighteen for all elections.&quot;,
    exp: &quot;Young adults gained full political voice, aligning civic responsibility with representation.&quot; },
  { q: &quot;What does the Twenty‑Seventh Amendment do?&quot;,
    a: &quot;It delays congressional pay changes from taking effect until after the next election of representatives.&quot;,
    exp: &quot;The delay lets voters weigh in before members benefit from salary adjustments, promoting accountability.&quot; }
];

/* End of DATA ONLY file */


const SECTIONS = [
  { label: 'Foundations (Q1–15)', start: 0 },
  { label: 'Articles I–VII (Q16–40)', start: 15 },
  { label: 'Key Principles (Q41–55)', start: 40 },
  { label: 'Bill of Rights & Civil Liberties (Q56–80)', start: 55 },
  { label: 'Federalism & Change (Q81–100)', start: 80 },
  { label: '27 Amendments (Q101–127)', start: 100 }
];

/* ----------------------- App State ----------------------- */
let order = [...CARDS.keys()];
let idx = 0;            // which card in 'order'
let step = 0;           // 0=Q, 1=Q+A, 2=Q+A+EXP
let randomized = false; // randomized order?
let animTimer = null;   // current animation timer
let animAbort = null;   // abort fn for current animation
let wpm = 220;          // default words per minute
let renderedIndex = -1;  // which original card index has been rendered
let renderedStep = -1;   // last rendered step for that card (0,1,2)
/* ----------------------- Utilities ----------------------- */
function shuffle(arr){
  for (let i = arr.length - 1; i &gt; 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [arr[i], arr[j]] = [arr[j], arr[i]];
  }
}
function clearAnim() {
  if (animTimer) { clearInterval(animTimer); animTimer = null; }
  if (animAbort) { animAbort(); animAbort = null; }
}
function typeWords(el, text, wpmVal) {
  const words = (text || &quot;&quot;).split(/\s+/);
  el.textContent = &quot;&quot;;
  let i = 0;
  const delay = Math.max(30, Math.round(60000 / Math.max(60, wpmVal)));
  return new Promise((resolve) =&gt; {
    const tick = () =&gt; {
      if (i &gt;= words.length) { clearInterval(animTimer); animTimer = null; resolve(); return; }
      el.textContent += (i === 0 ? &quot;&quot; : &quot; &quot;) + words[i++];
    };
    tick();
    animTimer = setInterval(tick, delay);
    animAbort = () =&gt; { clearInterval(animTimer); animTimer = null; el.textContent = words.join(&quot; &quot;); resolve(); };
  });
}
function hasExplanation(card) {
  return card &amp;&amp; typeof card.exp === &quot;string&quot; &amp;&amp; card.exp.trim().length &gt; 0;
}

/* ----------------------- Start / Quiz Flow ----------------------- */
function startSession(jumpToOriginalIndex = null) {
  randomized = document.getElementById('randomize').checked;
  // sync WPM from slider
  wpm = parseInt(document.getElementById('wpm').value, 10) || 220;
  order = [...CARDS.keys()];
  if (randomized) shuffle(order);

  if (jumpToOriginalIndex !== null) {
    const pos = order.findIndex(k =&gt; k === jumpToOriginalIndex);
    idx = pos &gt;= 0 ? pos : 0;
  } else {
    idx = 0;
  }
  step = 0;
  renderedIndex = -1;
  renderedStep  = -1;

  document.getElementById('start').classList.add('hidden');
  document.getElementById('all').classList.add('hidden');
  const quiz = document.getElementById('quiz');
  quiz.classList.remove('hidden');
  quiz.focus();
  // show global mobile nav on quiz screen
  document.getElementById('navpadGlobal').classList.remove('hidden');
  document.body.classList.add('has-nav');
  renderQuiz();
}

async function renderQuiz() {
  const stage = document.getElementById('stage');
  const card = CARDS[order[idx]];

  // If we switched cards, rebuild fresh and type sequentially up to current step
  if (renderedIndex !== idx) {
    clearAnim();
    stage.innerHTML = &quot;&quot;;

    // Question (always type)
    const q = document.createElement('div');
    q.className = 'q';
    stage.appendChild(q);
    await typeWords(q, card.q, wpm);
    renderedIndex = idx; renderedStep = 0;

    // If we land with step &gt;=1 (e.g., via Back), add Answer/Explanation sequentially
    if (step &gt;= 1) {
      const a = document.createElement('div');
      a.className = 'a';
      stage.appendChild(a);
      await typeWords(a, &quot;      &quot; + card.a, wpm);
      renderedStep = 1;
    }
    if (step &gt;= 2 &amp;&amp; hasExplanation(card)) {
      const exp = document.createElement('div');
      exp.className = 'exp';
      stage.appendChild(exp);
      await typeWords(exp, &quot;Explanation: &quot; + card.exp, wpm);
      renderedStep = 2;
    }
  } else {
    // Same card: extend without replaying prior parts
    if (step &gt; renderedStep) {
      if (renderedStep === 0 &amp;&amp; step &gt;= 1) {
        // Append only the Answer
        const a = document.createElement('div');
        a.className = 'a';
        stage.appendChild(a);
        await typeWords(a, &quot;      &quot; + card.a, wpm);
        renderedStep = 1;
      }
      if (renderedStep &lt;= 1 &amp;&amp; step &gt;= 2 &amp;&amp; hasExplanation(card)) {
        // Append only the Explanation
        const exp = document.createElement('div');
        exp.className = 'exp';
        stage.appendChild(exp);
        await typeWords(exp, &quot;Explanation: &quot; + card.exp, wpm);
        renderedStep = 2;
      }
    } else if (step &lt; renderedStep) {
      // Going backwards: rebuild static up to the requested step (no typing replay)
      clearAnim();
      stage.innerHTML = '';
      const q = document.createElement('div');
      q.className = 'q';
      q.textContent = card.q;
      stage.appendChild(q);
      if (step &gt;= 1) {
        const a = document.createElement('div');
        a.className = 'a';
        a.textContent = &quot;      &quot; + card.a;
        stage.appendChild(a);
      }
      if (step &gt;= 2 &amp;&amp; hasExplanation(card)) {
        const exp = document.createElement('div');
        exp.className = 'exp';
        exp.textContent = &quot;Explanation: &quot; + card.exp;
        stage.appendChild(exp);
      }
      renderedStep = step;
    }
  }

  document.getElementById('progress').textContent =
    `Question ${idx + 1} of ${CARDS.length}${randomized ? &quot; • Randomized&quot; : &quot;&quot;}`;
}

function next() {
  // Do not fast-forward while typing; keep the typing effect consistent
  if (animTimer) { return; }

  const card = CARDS[order[idx]];

  if (step &lt; 2) {
    // Skip explanation step if it doesn't exist
    if (step === 1 &amp;&amp; !hasExplanation(card)) {
      step = 0;
      if (idx &lt; order.length - 1) idx++; else idx = 0;
      renderedIndex = -1; renderedStep = -1;
      renderQuiz();
      return;
    }
    step++;
    renderQuiz();
    return;
  }

  // Move to next card
  step = 0;
  if (idx &lt; order.length - 1) idx++; else idx = 0;
  renderedIndex = -1; renderedStep = -1;
  renderQuiz();
}

function back() {
  // Do not fast-forward while typing
  if (animTimer) { return; }

  if (step &gt; 0) {
    step--;
    renderQuiz();
    return;
  }
  // Move to previous card at full reveal
  if (idx &gt; 0) idx--; else idx = order.length - 1;
  step = 2;
  renderedIndex = -1; renderedStep = -1;
  renderQuiz();
}

/* ----------------------- Show All (Typed Out) ----------------------- */
function showAll() {
  randomized = document.getElementById('randomize').checked;
  order = [...CARDS.keys()];
  if (randomized) shuffle(order);

  document.getElementById('start').classList.add('hidden');
  document.getElementById('quiz').classList.add('hidden');
  const all = document.getElementById('all');
  all.classList.remove('hidden');
  // hide global nav on All view
  document.getElementById('navpadGlobal').classList.add('hidden');
  document.body.classList.remove('has-nav');

  document.getElementById('allOrderLabel').textContent = randomized ? &quot;Randomized&quot; : &quot;Original&quot;;
  document.getElementById('wpmEcho').textContent = wpm;

  const list = document.getElementById('allList');
  list.innerHTML = &quot;&quot;;

  order.forEach((k, i) =&gt; {
    const c = CARDS[k];
    const wrap = document.createElement('div');
    wrap.className = 'allitem';

    const idxDiv = document.createElement('div');
    idxDiv.className = 'index';
    idxDiv.textContent = `Q${i+1}`;
    wrap.appendChild(idxDiv);

    const q = document.createElement('div');
    q.className = 'q';
    q.textContent = c.q;
    wrap.appendChild(q);

    const a = document.createElement('div');
    a.className = 'a';
    a.textContent = &quot;      &quot; + c.a;
    wrap.appendChild(a);

    if (hasExplanation(c)) {
      const e = document.createElement('div');
      e.className = 'exp';
      e.textContent = &quot;Explanation: &quot; + c.exp;
      wrap.appendChild(e);
    }

    list.appendChild(wrap);
  });
}

function backToStart() {
  clearAnim();
  document.getElementById('quiz').classList.add('hidden');
  document.getElementById('all').classList.add('hidden');
  document.getElementById('start').classList.remove('hidden');
  // hide global nav on Start view
  document.getElementById('navpadGlobal').classList.add('hidden');
  document.body.classList.remove('has-nav');
}

/* ----------------------- Jump To (Start Screen) ----------------------- */
function populateJumpSelect() {
  const sel = document.getElementById('jumpSelect');
  sel.innerHTML = '';
  SECTIONS.forEach(sec =&gt; {
    const opt = document.createElement('option');
    opt.value = String(sec.start); // original start index for that section
    opt.textContent = sec.label;
    sel.appendChild(opt);
  });
}
function jumpGo() {
  const originalIndex = parseInt(document.getElementById('jumpSelect').value, 10);
  startSession(originalIndex);
}
/* ----------------------- Events ----------------------- */
document.getElementById('startBtn').addEventListener('click', () =&gt; startSession(null));
document.getElementById('showAllBtn').addEventListener('click', showAll);
document.getElementById('backToStart1').addEventListener('click', backToStart);
document.getElementById('backToStart2').addEventListener('click', backToStart);
document.getElementById('printBtn').addEventListener('click', () =&gt; window.print());
document.getElementById('jumpGoBtn').addEventListener('click', jumpGo);
// Touch-friendly global nav buttons
document.getElementById('globalBack').addEventListener('click', back);
document.getElementById('globalNext').addEventListener('click', next);

const quizEl = document.getElementById('quiz');
quizEl.addEventListener('keydown', (e) =&gt; {
  // Prevent double-handling on auto-repeat and stop bubbling to document
  if (e.repeat) { e.preventDefault(); return; }
  if (e.code === 'Space' || e.key === 'Enter' || e.key === 'ArrowRight') { e.preventDefault(); e.stopPropagation(); next(); }
  else if (e.key === 'ArrowLeft' || e.code === 'Backspace') { e.preventDefault(); e.stopPropagation(); back(); }
});
document.addEventListener('keydown', (e) =&gt; {
  const quizVisible = !quizEl.classList.contains('hidden');
  if (!quizVisible) return;
  // If focus is already inside #quiz, let that handler manage it to avoid duplicates
  if (quizEl.contains(e.target)) return;
  if (e.repeat) { e.preventDefault(); return; }
  if (e.code === 'Space' || e.key === 'Enter' || e.key === 'ArrowRight') { e.preventDefault(); next(); }
  else if (e.key === 'ArrowLeft' || e.code === 'Backspace') { e.preventDefault(); back(); }
});
quizEl.addEventListener('click', () =&gt; quizEl.focus());

document.getElementById('wpm').addEventListener('input', (e) =&gt; {
  wpm = parseInt(e.target.value, 10);
  document.getElementById('wpmLabel').textContent = `${wpm} wpm`;
});

// Initialize start UI
wpm = parseInt(document.getElementById('wpm').value, 10) || 220;
document.getElementById('wpmLabel').textContent = `${wpm} wpm`;
populateJumpSelect();

// --- Lightweight self-tests (console only, do not affect UI) ---
(function selfTest(){
  try {
    console.assert(Array.isArray(CARDS), 'CARDS should be an array');
    console.assert(CARDS.length &gt;= 5, 'CARDS should have entries');
    console.assert(typeof CARDS[0].q === 'string' &amp;&amp; typeof CARDS[0].a === 'string', 'Each card needs q and a');
    // Missing explanation guard test
    const fakeNoExp = {q:'Q', a:'A', exp:''};
    console.assert(!hasExplanation(fakeNoExp), 'hasExplanation should be false when exp is empty');
    // Ensure start helpers exist
    console.assert(typeof startSession === 'function' &amp;&amp; typeof showAll === 'function', 'Core functions should exist');
    console.debug('[Flashcards] Self-test passed. Total cards:', CARDS.length);
  } catch (e) {
    console.error('[Flashcards] Self-test error:', e);
  }
})();
&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;

&lt;/body&gt;" style="width: 100%; display: block; height: 600px; overflow: visible; transition: height 1.5s;"></iframe>
