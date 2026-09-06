---
title: "Envlo & Envlomet in Latin America"
layout: post
---

<style>
/* Scoped to this post. Uses the site's own palette idiom: hsl(230deg 18% L%)
   with light-dark(), PT Sans inherited from the theme, #46f accent. */
.envlo{
  --e-ink:      light-dark(hsl(230deg 18% 6%),  hsl(230deg 18% 100%));
  --e-ink-2:    light-dark(hsl(230deg 18% 30%), hsl(230deg 18% 78%));
  --e-ink-3:    light-dark(hsl(230deg 18% 46%), hsl(230deg 18% 62%));
  --e-rule:     rgba(131,134,149,.26);
  --e-rule-2:   rgba(131,134,149,.55);
  --e-fill:     rgba(131,134,149,.10);
  --e-fill-2:   rgba(131,134,149,.18);
  --e-accent:   light-dark(#46f, #38f);
  --e-pos:      light-dark(#1d6b40, #74c992);
  --e-pos-bg:   light-dark(rgba(29,107,64,.10), rgba(116,201,146,.14));
  --e-neg:      light-dark(#a02b2c, #f0918d);
  --e-neg-bg:   light-dark(rgba(160,43,44,.09), rgba(240,145,141,.13));
  --e-warn:     light-dark(#8a5900, #e6b45f);
  --e-warn-bg:  light-dark(rgba(138,89,0,.10), rgba(230,180,95,.13));
}

/* --- lede + fact strip --- */
.envlo .e-dek{font-size:1.1em;line-height:1.5;color:var(--e-ink-2);text-align:left;margin:0 0 1.6em}
.envlo .e-facts{display:flex;flex-wrap:wrap;gap:0;border-top:1px solid var(--e-rule);
  border-bottom:1px solid var(--e-rule);margin:0 0 2em;padding:0}
.envlo .e-facts div{padding:.7em 1.2em .7em 0;margin-right:1.2em;border-right:1px solid var(--e-rule);
  font-size:.92em;color:var(--e-ink-2)}
.envlo .e-facts div:last-child{border-right:0;margin-right:0}
.envlo .e-facts b{display:block;font-size:.78em;letter-spacing:.09em;text-transform:uppercase;
  color:var(--e-ink-3);font-weight:normal;margin-bottom:.15em}

/* --- the recommendation --- */
.envlo .e-verdict{border:1px solid var(--e-rule-2);border-left:3px solid var(--e-accent);
  background:var(--e-fill);padding:1.2em 1.5em;margin:0 0 2.4em}
.envlo .e-verdict > :first-child{margin-top:0}
.envlo .e-verdict > :last-child{margin-bottom:0}
.envlo .e-verdict h2{font-size:1.25em;line-height:1.3;margin:.5em 0 .7em;border:0;padding:0}

/* --- labels --- */
.envlo .e-tag{display:inline-block;font-size:.72em;letter-spacing:.09em;text-transform:uppercase;
  padding:.2em .6em;border-radius:2px;background:var(--e-fill-2);color:var(--e-ink-2);
  font-weight:bold;white-space:nowrap}
.envlo .e-tag.bad{background:var(--e-neg-bg);color:var(--e-neg)}
.envlo .e-tag.warn{background:var(--e-warn-bg);color:var(--e-warn)}
.envlo .e-tag.good{background:var(--e-pos-bg);color:var(--e-pos)}

/* --- sections --- */
.envlo h2{font-size:1.3em;line-height:1.3;margin:2.4em 0 .8em;
  padding-bottom:.35em;border-bottom:1px solid var(--e-rule-2)}
.envlo h3{font-size:1.08em;margin:1.8em 0 .5em}
.envlo .e-num{display:block;font-size:.75em;letter-spacing:.11em;text-transform:uppercase;
  color:var(--e-accent);margin:2.6em 0 -1.9em;font-weight:bold}

/* --- contents --- */
.envlo .e-toc{columns:2;column-gap:2em;font-size:.92em;padding:.9em 0;
  border-top:1px solid var(--e-rule);border-bottom:1px solid var(--e-rule);margin:0 0 2.4em}
.envlo .e-toc a{display:block;padding:.18em 0;break-inside:avoid}
@media (max-width:34em){.envlo .e-toc{columns:1}}

/* --- tables: keep the theme's borders and header fill, fix width + numerals --- */
.envlo .e-scroll{overflow-x:auto;margin:1.2em 0 1.6em}
.envlo .e-scroll table{display:table;width:100%;min-width:30em;margin:0}
.envlo caption{caption-side:top;text-align:left;font-size:.86em;color:var(--e-ink-2);
  padding:.5em .2em .6em;line-height:1.45}
.envlo td.n,.envlo th.n{text-align:right;font-variant-numeric:tabular-nums;white-space:nowrap}
.envlo .pos{color:var(--e-pos);font-weight:bold}
.envlo .neg{color:var(--e-neg);font-weight:bold}
.envlo .dim{color:var(--e-ink-3)}
.envlo .e-band td{background:var(--e-fill);font-size:.8em;letter-spacing:.08em;
  text-transform:uppercase;color:var(--e-ink-3)}

/* --- figures for the numbers --- */
.envlo .e-stats{display:flex;flex-wrap:wrap;border-top:1px solid var(--e-rule-2);
  border-bottom:1px solid var(--e-rule-2);margin:1.4em 0 1.8em}
.envlo .e-stats div{flex:1 1 8em;padding:.8em 1em .8em 0;border-right:1px solid var(--e-rule)}
.envlo .e-stats div:last-child{border-right:0}
.envlo .e-stats .v{font-size:1.4em;font-weight:bold;font-variant-numeric:tabular-nums;line-height:1.15}
.envlo .e-stats .k{font-size:.8em;color:var(--e-ink-3);line-height:1.35;margin-top:.25em}

/* --- sensitivity grids --- */
.envlo .e-grids{display:flex;flex-wrap:wrap;gap:1.2em;margin:1.4em 0}
.envlo .e-grid{flex:1 1 17em;border:1px solid var(--e-rule);padding:.9em 1em 1em}
.envlo .e-grid h4{margin:0 0 .1em;font-size:.98em}
.envlo .e-grid .sub{font-size:.8em;color:var(--e-ink-3);margin:0 0 .7em;text-align:left}
.envlo .e-grid table{display:table;width:100%;min-width:0;margin:0;font-size:.82em}
.envlo .e-grid th,.envlo .e-grid td{border:0;padding:.28em .4em}
.envlo .e-grid thead th{text-align:right;font-size:.9em;color:var(--e-ink-3);
  border-bottom:1px solid var(--e-rule);background:none}
.envlo .e-grid thead,.envlo .e-grid tr:hover{background:none}
.envlo .e-grid tbody th{text-align:left;padding-left:0;color:var(--e-ink-3);font-weight:normal}
.envlo .e-grid td{text-align:right;font-variant-numeric:tabular-nums;border-radius:2px}
.envlo .c-neg{background:var(--e-neg-bg);color:var(--e-neg)}
.envlo .c-mid{background:var(--e-fill-2);color:var(--e-ink-2)}
.envlo .c-pos{background:var(--e-pos-bg);color:var(--e-pos)}

/* --- callouts --- */
.envlo .e-note{border-left:3px solid var(--e-warn);background:var(--e-warn-bg);
  padding:.8em 1.2em;margin:1.4em 0;font-size:.95em}
.envlo .e-note.kill{border-left-color:var(--e-neg);background:var(--e-neg-bg)}
.envlo .e-note > :first-child{margin-top:0}
.envlo .e-note > :last-child{margin-bottom:0}
.envlo .e-note b.lbl{display:block;font-size:.8em;letter-spacing:.09em;text-transform:uppercase;
  color:var(--e-ink-2);margin-bottom:.35em}

/* --- diagram --- */
.envlo figure.e-fig{margin:1.6em 0}
.envlo .e-diagram{border:1px solid var(--e-rule);padding:1em .5em;overflow-x:auto}
.envlo .e-diagram svg{display:block;margin:0 auto;max-width:100%;height:auto;border-radius:0}
.envlo figcaption{font-size:.86em;color:var(--e-ink-3);margin-top:.7em;text-align:left;line-height:1.5}

/* --- sources --- */
.envlo .e-src{font-size:.88em;columns:2;column-gap:2.2em}
.envlo .e-src p{margin:0 0 .55em;break-inside:avoid;text-align:left}
@media (max-width:38em){.envlo .e-src{columns:1}}
</style>

<div class="envlo" markdown="0">

<p class="e-dek">A plain-English read on what these two Korean diabetes products are, who already owns the Latin American rights, and what the remaining opportunity is actually worth.</p>

<div class="e-facts">
  <div><b>Molecule</b>Enavogliflozin 0.3 mg</div>
  <div><b>Originator</b>Daewoong Pharmaceutical (KR)</div>
  <div><b>Class</b>SGLT-2 inhibitor, oral</div>
</div>

<div class="e-verdict">
<span class="e-tag bad">Recommendation</span>
<h2>Do not pursue a standalone LATAM licence. The territory you can buy is worth little, and the territory worth having is already sold.</h2>

<p>Three findings drive this. <b>First</b>, Daewoong has already granted exclusive Latin American rights to Arcera (formerly M8/Moksha8) covering at least ten countries including Brazil and Mexico — roughly 80% of the region's value. <b>Second</b>, the countries plausibly still open (Argentina, Colombia, Chile, Peru, Uruguay, Paraguay, Bolivia) carry an SGLT-2 class value of roughly US$200m, and a licence there produces a risk-adjusted NPV of <b class="neg">−US$1.9m</b> in the base case. It needs a 4.7% peak class share to break even — higher than enavogliflozin has achieved in its own home market.</p>

<p><b>Third</b>, and most important for a reader without a science background: this is a <i>me-too</i> molecule entering a market that has already gone generic. Dapagliflozin generics sell in Brazil for R$62–110 a month against a Forxiga price of R$134. Envlo is a fifth branded entrant, with no cardiovascular or kidney outcomes data, arriving after the price has already collapsed.</p>

<p><b>What to do instead.</b> Open a direct conversation with Daewoong for the definitive territory register — the public record is incomplete — and, if the real goal is a LATAM cardiometabolic portfolio, treat Envlomet (the metformin combination) as a possible value-tier line extension inside an existing franchise, not as a franchise anchor. If Brazil and Mexico ever come free, the ceiling on consideration is <b>US$13m</b>, rising to US$46m only on assumptions worth doubting.</p>
</div>

<div class="e-toc">
  <a href="#p1">1 &nbsp;What these products actually are</a>
  <a href="#p2">2 &nbsp;What the evidence shows — and doesn't</a>
  <a href="#p3">3 &nbsp;The competitive set</a>
  <a href="#p4">4 &nbsp;Who already owns Latin America</a>
  <a href="#p5">5 &nbsp;Market size and the price reality</a>
  <a href="#p6">6 &nbsp;Launch prospects and challenges</a>
  <a href="#p7">7 &nbsp;Valuation</a>
  <a href="#p8">8 &nbsp;Deal design and next 100 days</a>
</div>

<span class="e-num">Part 01</span>
<h2 id="p1">Envlo is a pill that makes you urinate out excess sugar; Envlomet is that pill combined with the standard first-line drug</h2>

<p>Both are oral tablets for type 2 diabetes, developed by Daewoong Pharmaceutical in South Korea. Envlo is the single molecule. Envlomet packages the same molecule together with metformin, the cheap generic drug almost every type 2 diabetic starts on.</p>

<h3>The mechanism, without the biology</h3>

<p>Your kidneys filter your entire blood volume many times a day. Sugar gets filtered out along with waste — but the body treats sugar as too valuable to lose, so a set of molecular "pumps" lining the kidney tubules grab that sugar and push it back into the bloodstream before it can leave in urine. The dominant pump is called <b>SGLT-2</b>, and it recovers roughly 90% of the filtered sugar.</p>

<p>In a diabetic, this is exactly the wrong behaviour: the body is diligently rescuing sugar it already has far too much of. An <b>SGLT-2 inhibitor</b> blocks that pump. Sugar that would have been recovered stays in the urine and leaves the body — typically 50–80 grams a day, roughly the sugar in two cans of soft drink.</p>

<figure class="e-fig">
<div class="e-diagram">
<svg viewBox="0 0 720 290" role="img" aria-label="Without an SGLT-2 inhibitor, glucose filtered by the kidney is pumped back into the blood; with the drug, the pump is blocked and glucose leaves in the urine.">
  <defs>
    <marker id="eah" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto">
      <path d="M0,0 L10,5 L0,10 z" fill="var(--e-warn)"/>
    </marker>
  </defs>
  <g font-size="10.5" font-family="PT Sans, system-ui, sans-serif">
    <text x="18" y="20" font-size="10.5" letter-spacing="1.3" fill="var(--e-ink-3)">UNTREATED DIABETIC</text>
    <line x1="18" y1="28" x2="330" y2="28" stroke="var(--e-rule-2)"/>
    <rect x="58" y="56" width="230" height="50" fill="var(--e-fill)" stroke="var(--e-rule-2)"/>
    <text x="68" y="97" fill="var(--e-ink-2)">KIDNEY TUBULE &#8594;</text>
    <g fill="var(--e-warn)">
      <circle cx="98" cy="72" r="4"/><circle cx="128" cy="74" r="4"/><circle cx="158" cy="71" r="4"/>
      <circle cx="188" cy="73" r="4"/><circle cx="218" cy="72" r="4"/>
    </g>
    <rect x="138" y="106" width="72" height="25" rx="2" fill="var(--e-fill-2)" stroke="var(--e-accent)"/>
    <text x="174" y="123" text-anchor="middle" fill="var(--e-accent)" font-size="9.5" font-weight="bold">SGLT-2</text>
    <path d="M174,131 L174,160" stroke="var(--e-warn)" stroke-width="1.6" fill="none" marker-end="url(#eah)"/>
    <rect x="58" y="164" width="230" height="42" fill="var(--e-neg-bg)" stroke="var(--e-rule-2)"/>
    <text x="68" y="182" fill="var(--e-ink-2)">BLOODSTREAM</text>
    <g fill="var(--e-warn)">
      <circle cx="118" cy="195" r="4"/><circle cx="143" cy="197" r="4"/><circle cx="168" cy="194" r="4"/>
      <circle cx="193" cy="196" r="4"/><circle cx="218" cy="195" r="4"/><circle cx="243" cy="197" r="4"/>
    </g>
    <text x="58" y="232" fill="var(--e-neg)" font-size="10.5" font-weight="bold">~90% of sugar recovered</text>
    <text x="58" y="248" fill="var(--e-ink-3)">Blood sugar stays high</text>

    <line x1="358" y1="12" x2="358" y2="262" stroke="var(--e-rule)" stroke-dasharray="3 4"/>

    <text x="390" y="20" font-size="10.5" letter-spacing="1.3" fill="var(--e-ink-3)">ON ENAVOGLIFLOZIN 0.3 mg</text>
    <line x1="390" y1="28" x2="702" y2="28" stroke="var(--e-rule-2)"/>
    <rect x="430" y="56" width="230" height="50" fill="var(--e-fill)" stroke="var(--e-rule-2)"/>
    <text x="440" y="97" fill="var(--e-ink-2)">KIDNEY TUBULE &#8594;</text>
    <g fill="var(--e-warn)">
      <circle cx="470" cy="72" r="4"/><circle cx="500" cy="74" r="4"/><circle cx="530" cy="71" r="4"/>
      <circle cx="560" cy="73" r="4"/><circle cx="590" cy="72" r="4"/><circle cx="620" cy="74" r="4"/>
    </g>
    <rect x="510" y="106" width="72" height="25" rx="2" fill="var(--e-fill)" stroke="var(--e-rule-2)"/>
    <text x="546" y="123" text-anchor="middle" fill="var(--e-ink-3)" font-size="9.5" font-weight="bold">SGLT-2</text>
    <g stroke="var(--e-neg)" stroke-width="2.2">
      <line x1="514" y1="110" x2="578" y2="127"/><line x1="578" y1="110" x2="514" y2="127"/>
    </g>
    <text x="592" y="124" fill="var(--e-neg)" font-size="9.5" font-weight="bold">BLOCKED</text>
    <rect x="430" y="164" width="230" height="42" fill="var(--e-pos-bg)" stroke="var(--e-rule-2)"/>
    <text x="440" y="182" fill="var(--e-ink-2)">BLOODSTREAM</text>
    <g fill="var(--e-warn)"><circle cx="490" cy="195" r="4"/><circle cx="528" cy="197" r="4"/></g>
    <path d="M662,82 L698,82" stroke="var(--e-warn)" stroke-width="1.6" fill="none" marker-end="url(#eah)"/>
    <text x="634" y="48" fill="var(--e-warn)" font-size="9.5" font-weight="bold">out in urine</text>
    <text x="430" y="232" fill="var(--e-pos)" font-size="10.5" font-weight="bold">~50–80 g of sugar excreted daily</text>
    <text x="430" y="248" fill="var(--e-ink-3)">Blood sugar, weight and blood pressure fall</text>
  </g>
</svg>
</div>
<figcaption>How an SGLT-2 inhibitor works. The drug does not change how the body makes or uses insulin — it simply stops the kidney from rescuing sugar. This is why the class also produces weight loss and a modest blood-pressure fall: calories and fluid leave with the sugar.</figcaption>
</figure>

<h3>Why the two products exist</h3>

<p>Standard diabetes care is a ladder. Almost every patient starts on <b>metformin</b> — a decades-old, near-free generic. When metformin alone stops controlling blood sugar, a second drug is added. Envlo is that second drug. <b>Envlomet</b> puts both into one tablet.</p>

<p>Combination tablets matter commercially far more than they sound. They halve the pill count, which measurably improves whether patients keep taking their medicine, and they let a company defend share when the single molecule genericises. In emerging markets, combination products are frequently where the durable margin sits. <i>For this reason Envlomet, not Envlo, is the more interesting half of this asset.</i></p>

<p>Enavogliflozin is also unusually potent per milligram. The dose is <b>0.3 mg</b>, against 10 mg for dapagliflozin and 10–25 mg for empagliflozin — roughly thirty times less drug substance for a comparable effect. That is a real pharmacological achievement and a modest cost-of-goods advantage. It is not, on its own, a reason a Brazilian endocrinologist switches a patient.</p>

<span class="e-num">Part 02</span>
<h2 id="p2">The clinical package proves the drug works as well as the market leader — but not that it does the thing doctors now prescribe the class for</h2>

<p>Daewoong ran a head-to-head trial against dapagliflozin, the class leader. Read carefully, it is a competent non-inferiority package with one interesting signal and one large strategic hole.</p>

<div class="e-scroll">
<table>
<caption>Enavogliflozin 0.3 mg vs dapagliflozin 10 mg — pooled analysis of two randomised trials, 470 patients, 24 weeks, added to metformin</caption>
<thead><tr><th>Measure</th><th class="n">Enavo.</th><th class="n">Dapa.</th><th>Read</th></tr></thead>
<tbody>
<tr><td>HbA1c, normal kidney function</td><td class="n">−0.88%</td><td class="n">−0.97%</td><td class="dim">No difference (p=0.21)</td></tr>
<tr><td>HbA1c, mildly reduced kidney function</td><td class="n">−0.94%</td><td class="n">−0.77%</td><td><span class="pos">Enavogliflozin better</span> (p=0.02)</td></tr>
<tr><td>Body weight</td><td class="n">−3.25 kg</td><td class="n">−3.21 kg</td><td class="dim">No difference</td></tr>
<tr><td>Sugar excreted in urine (UGCR)</td><td class="n">+64.2</td><td class="n">+43.8</td><td><span class="pos">Markedly higher</span> (p&lt;0.0001)</td></tr>
<tr><td>Blood pressure</td><td class="n">—</td><td class="n">—</td><td class="dim">No difference</td></tr>
<tr><td>Adverse events (any)</td><td class="n">22.6%</td><td class="n">23.0%</td><td class="dim">Comparable</td></tr>
<tr><td>Serious adverse events</td><td class="n">1.3%</td><td class="n">3.0%</td><td class="dim">Lower, small numbers</td></tr>
</tbody>
</table>
</div>

<p><b>HbA1c</b> is the standard three-month average of blood sugar; a fall of about 1 percentage point is what a good second-line drug delivers. Enavogliflozin matches dapagliflozin on that, and beats it in patients whose kidneys are already slightly impaired — a meaningful subgroup, because SGLT-2 inhibitors normally lose potency as kidney function falls, and diabetic patients' kidneys decline over time.</p>

<div class="e-note kill">
<b class="lbl">The strategic hole</b>
<p>Since 2015, this class stopped being sold on blood sugar. Empagliflozin and dapagliflozin ran enormous multi-year trials proving they <i>reduce heart attacks, hospitalisation for heart failure, kidney failure and death</i> — in patients with and without diabetes. That is why cardiologists and nephrologists, not just diabetologists, prescribe them, and it is what international guidelines are written around.</p>
<p>Enavogliflozin has no completed outcomes trial. Its cardiorenal study (ENVELOP) is still enrolling. Until it reads out, Envlo is a glucose-lowering drug competing against two molecules that are also proven organ-protective drugs — and that are available as cheap generics.</p>
</div>

<p>For a licensing decision, this is the crux. You would be paying for a branded product whose clinical story is "as good as the generic," in a category where the market leaders' story is "prevents you dying." That gap cannot be closed with a sales force.</p>

<span class="e-num">Part 03</span>
<h2 id="p3">Envlo would be the fifth branded entrant into a class that has already genericised in its two largest LATAM markets</h2>

<div class="e-scroll">
<table>
<caption>The competitive set in Latin America — SGLT-2 inhibitors and the adjacent class taking share from them</caption>
<thead><tr><th>Product</th><th>Position</th><th>Threat</th></tr></thead>
<tbody>
<tr><td><b>Jardiance</b> (empagliflozin)<br><span class="dim">Boehringer / Lilly</span></td><td>Class leader. Cardiovascular <i>and</i> heart-failure outcomes data. Broad guideline position.</td><td><span class="e-tag bad">Severe</span></td></tr>
<tr><td><b>Forxiga</b> (dapagliflozin)<br><span class="dim">AstraZeneca</span></td><td>Heart-failure and chronic-kidney-disease outcomes data. Now facing generics in Brazil and Mexico.</td><td><span class="e-tag bad">Severe</span></td></tr>
<tr><td><b>Dapagliflozin generics</b><br><span class="dim">EMS, Eurofarma, Medley, Germed</span></td><td>Brazil R$62–110 per month vs Forxiga R$134. Eurofarma launched the first dapagliflozin + metformin generic in May 2026.</td><td><span class="e-tag bad">Severe</span></td></tr>
<tr><td><b>Invokana</b> (canagliflozin)<br><span class="dim">Janssen</span></td><td>Declining; amputation-risk labelling damaged it.</td><td><span class="e-tag good">Low</span></td></tr>
<tr><td><b>GLP-1 agonists</b><br><span class="dim">Novo Nordisk, Lilly</span></td><td>Superior HbA1c and dramatic weight loss. Absorbing the private-pay patient and physician mindshare across LATAM.</td><td><span class="e-tag warn">High</span></td></tr>
<tr><td><b>Envlo / Envlomet</b><br><span class="dim">Daewoong, via licensee</span></td><td>Non-inferior on sugar; better in mild kidney impairment; no outcomes data; no brand equity in region.</td><td class="dim">—</td></tr>
</tbody>
</table>
</div>

<p>The competitive question is not "can Envlo match Forxiga?" It can. The question is <b>what a physician is being asked to give up.</b> Switching a patient to Envlo means moving off a molecule with outcomes evidence, onto one without, usually at a higher price than the generic they could have written instead. The set of prescribers for whom that trade makes sense is small.</p>

<div class="e-note">
<b class="lbl">The one credible wedge</b>
<p>The mild-kidney-impairment result is the only clinically ownable claim in the package. A focused nephrology-adjacent positioning — "the SGLT-2 that holds its glucose effect as eGFR declines" — is defensible and differentiating. It is also a narrow slice of the market, and it invites the obvious question of whether the drug protects the kidney, which nobody can yet answer.</p>
</div>

<span class="e-num">Part 04</span>
<h2 id="p4">The rights most worth having are already held by a sovereign-backed platform that has just deepened its relationship with Daewoong</h2>

<p>This is the finding that reframes the question. Public disclosure shows Daewoong granted exclusive Latin American rights to M8 Pharmaceuticals (formerly Moksha8) in February 2023, and expanded that to eight further countries in November 2025. M8 was absorbed into <b>Arcera Life Sciences</b> in December 2024; Arcera also owns Acino and is backed by ADQ, the Abu Dhabi sovereign wealth fund.</p>

<div class="e-scroll">
<table>
<caption>Territory register, reconstructed from public disclosure. <span class="dim">Must be verified directly with Daewoong; the public record is incomplete.</span></caption>
<thead><tr><th>Market</th><th>Status</th><th>Availability</th></tr></thead>
<tbody>
<tr><td><b>Brazil</b></td><td>Exclusively licensed, Feb 2023 — M8 → Arcera</td><td><span class="e-tag bad">Closed</span></td></tr>
<tr><td><b>Mexico</b></td><td>Exclusively licensed; marketing approval granted May 2026</td><td><span class="e-tag bad">Closed</span></td></tr>
<tr><td><b>Ecuador, Costa Rica, Guatemala, Nicaragua, Honduras, Panama, Dominican Rep., El Salvador</b></td><td>Supply agreements, Nov 2025 — M8 → Arcera</td><td><span class="e-tag bad">Closed</span></td></tr>
<tr><td><b>Argentina, Colombia, Chile, Peru</b></td><td>Not publicly announced. Daewoong reports filings in 12 LATAM countries, 7 approved — some of these may sit inside that count.</td><td><span class="e-tag warn">Verify</span></td></tr>
<tr><td><b>Uruguay, Paraguay, Bolivia</b></td><td>No public activity</td><td><span class="e-tag good">Likely open</span></td></tr>
<tr><td><b>Middle East &amp; North Africa</b> (8)</td><td>Licensed June 2026, ~KRW 145.2bn (US$93–105m contract value) — Acino / Arcera</td><td class="dim">Context</td></tr>
</tbody>
</table>
</div>

<p><b>Read the MENA deal as a signal, not a comparable.</b> In June 2026 Daewoong extended the same counterparty from Latin America into the Gulf. A partner that has just been rewarded with a second region is not a partner Daewoong will disintermediate, and Arcera — with ADQ behind it and operations in 90+ markets — is not a forced seller of a Brazilian and Mexican asset it registered itself.</p>

<div class="e-note">
<b class="lbl">Read the headline deal values correctly</b>
<p>Korean pharmaceutical disclosure convention quotes <i>cumulative multi-year supply revenue</i>, not consideration. The "KRW 143.3bn LATAM deal" (~US$104m) is Daewoong's expected product supply revenue across the contract term. At a typical 38% transfer price that implies roughly US$273m of cumulative in-market sales over about a decade — around US$27m a year. Nobody should read US$104m as an upfront payment. Realistic upfronts for a Korean SGLT-2 in an emerging region are <b>US$2–8m</b>.</p>
</div>

<span class="e-num">Part 05</span>
<h2 id="p5">Latin America is a large diabetes market but a modest branded-SGLT-2 market, and the price floor is already set</h2>

<div class="e-stats">
  <div><div class="v">~$970m</div><div class="k">LATAM SGLT-2 class value, 2026 (illustrative, triangulated)</div></div>
  <div><div class="v">~9%</div><div class="k">Forecast class CAGR, 2025–30</div></div>
  <div><div class="v">~72%</div><div class="k">Mexico's share of LATAM class value</div></div>
  <div><div class="v">~$200m</div><div class="k">Class value in territories plausibly open</div></div>
</div>

<p>Two things must be held in mind at once. Latin America has an enormous and fast-growing <i>patient</i> population — regional diabetes prevalence is forecast to rise about 38% over the next decade against 14% population growth. But the <i>value</i> of the branded SGLT-2 market is concentrated in Mexico, where private-pay pricing holds up, and is thin in Brazil, where volume is huge but price is not.</p>

<div class="e-scroll">
<table>
<caption>What a month of SGLT-2 therapy actually costs — retail pharmacy prices, September 2026</caption>
<thead><tr><th>Market</th><th>Product</th><th class="n">Local</th><th class="n">≈ US$/mo</th></tr></thead>
<tbody>
<tr><td>Brazil</td><td>Forxiga 10 mg × 30 (list)</td><td class="n">R$254</td><td class="n">47</td></tr>
<tr><td>Brazil</td><td>Forxiga 10 mg × 30 (discounted)</td><td class="n">R$134</td><td class="n">25</td></tr>
<tr><td>Brazil</td><td>Dapagliflozin generic × 30</td><td class="n">R$62–110</td><td class="n">11–20</td></tr>
<tr><td>Mexico</td><td>Forxiga 10 mg × 28</td><td class="n">MX$1,830</td><td class="n">99</td></tr>
<tr><td>Mexico</td><td>Dapagliflozin generic × 28</td><td class="n">MX$785</td><td class="n">42</td></tr>
</tbody>
</table>
</div>

<p><b>The so-what.</b> In Brazil a new branded SGLT-2 must justify a price against an R$62 generic — a 2–4× premium for a drug with weaker outcomes evidence. That is not a winnable argument at scale. Mexico is the only market where the price architecture supports a branded launch, and Mexico is licensed to Arcera.</p>

<h3>The empirical ceiling on share</h3>

<p>Envlo and Envlomet together produced <b>KRW 12.3bn (≈US$8.9m)</b> in Korea in 2024 — impressive growth of 261%, but roughly a 5% share of its home SGLT-2 class in year two, with full national promotion, home-market prescriber loyalty and no import cost. Treat <b>3% peak class share</b> as the base case abroad and 5% as the optimistic case. Anyone modelling above 5% is modelling something enavogliflozin has never done anywhere.</p>

<span class="e-num">Part 06</span>
<h2 id="p6">Six risks would decide this launch, and four of them are outside the licensee's control</h2>

<div class="e-scroll">
<table>
<caption>Risk register, ranked by effect on value</caption>
<thead><tr><th>Risk</th><th>Why it bites</th><th>Sev.</th><th>Mitigation</th></tr></thead>
<tbody>
<tr><td><b>Territory already encumbered</b></td><td>Brazil and Mexico carry ~74% of regional class value and are licensed. Whatever remains is sub-scale.</td><td><span class="e-tag bad">Critical</span></td><td>Obtain the signed territory schedule from Daewoong before any further spend.</td></tr>
<tr><td><b>No cardiorenal outcomes data</b></td><td>LATAM specialists follow ADA/EASD and ESC guidance. Without outcomes data the product cannot enter the guideline-driven segment, which is where the class grows.</td><td><span class="e-tag bad">Critical</span></td><td>None available. Make the ENVELOP readout a contractual trigger, not a launch assumption.</td></tr>
<tr><td><b>Generic price anchor</b></td><td>Four generic dapagliflozins in Brazil, plus a dapagliflozin + metformin generic since May 2026. Payers and pharmacy chains will benchmark against it directly.</td><td><span class="e-tag bad">Critical</span></td><td>Price at parity-plus, not premium; accept lower unit margin or do not launch.</td></tr>
<tr><td><b>GLP-1 substitution</b></td><td>Semaglutide-class products are absorbing private-pay cardiometabolic spend region-wide. Class growth may accrue to GLP-1s, not SGLT-2s.</td><td><span class="e-tag warn">High</span></td><td>Model class growth at 0–5%, not the 9% market-report figure.</td></tr>
<tr><td><b>Regulatory drag</b></td><td>ANVISA, COFEPRIS, INVIMA, ANMAT, ISP and DIGEMID each want full CTD dossiers, local representation and GMP recognition of the Korean site. 18–30 months is normal; a bridging study adds two years.</td><td><span class="e-tag warn">High</span></td><td>Sequence filings behind an agency that has already approved. Budget US$2.5m and a 2029 launch.</td></tr>
<tr><td><b>Single-source supply and FX</b></td><td>Finished product from Korea, invoiced in USD, sold in BRL/MXN/ARS/COP. A 20% currency move erases the contribution margin.</td><td><span class="e-tag warn">High</span></td><td>FX collar or local-currency transfer price; technology-transfer right to a regional CMO from year 4.</td></tr>
</tbody>
</table>
</div>

<h3>Pre-mortem: if this is done and it fails, here is the story</h3>

<p>It is 2031. US$4m went out as an upfront and US$2m on first approval, US$2.5m on registration in four countries and US$4m launching in two. Endocrinologists were polite about the kidney-subgroup data and kept writing generic dapagliflozin. The private payers who mattered wanted the outcomes trial. Argentina devalued twice. Peak sales reached US$4m, not US$11m. ENVELOP read out neutral. Arcera, meanwhile, launched the same molecule in Mexico at a real price and did fine, because they had the market that was worth having.</p>

<p>Every element of that story is visible today. That is what makes it a recommendation rather than a caution.</p>

<span class="e-num">Part 07</span>
<h2 id="p7">The open-territory licence destroys value; the Brazil–Mexico rights are worth at most US$13m</h2>

<p>Both paths modelled to 2038 on a 15% discount rate, with no terminal value — appropriate for a molecule whose class has already genericised. All figures US$m, risk-adjusted for regulatory and commercial probability of success.</p>

<div class="e-scroll">
<table>
<caption>Scenario summary — risk-adjusted NPV</caption>
<thead><tr><th>Scenario</th><th class="n">Launch</th><th class="n">Peak share</th><th class="n">Peak sales</th><th class="n">rNPV</th></tr></thead>
<tbody>
<tr class="e-band"><td colspan="5">A — Licence the open cluster (AR, CO, CL, PE, UY, PY, BO · class US$200m)</td></tr>
<tr><td>Downside</td><td class="n">2030</td><td class="n">1.8%</td><td class="n">7.2</td><td class="n neg">−2.8</td></tr>
<tr><td>Base</td><td class="n">2029</td><td class="n">3.0%</td><td class="n">15.1</td><td class="n neg">−1.9</td></tr>
<tr><td>Upside</td><td class="n">2029</td><td class="n">5.0%</td><td class="n">31.4</td><td class="n pos">+3.5</td></tr>
<tr class="e-band"><td colspan="5">B — Acquire the Brazil + Mexico rights (class US$715m, already registered)</td></tr>
<tr><td>Downside</td><td class="n">2028</td><td class="n">1.8%</td><td class="n">23.1</td><td class="n neg">−0.2</td></tr>
<tr><td>Base</td><td class="n">2027</td><td class="n">3.0%</td><td class="n">54.0</td><td class="n pos">+13.2</td></tr>
<tr><td>Upside</td><td class="n">2027</td><td class="n">5.0%</td><td class="n">112.2</td><td class="n pos">+45.9</td></tr>
</tbody>
</table>
</div>

<div class="e-note kill">
<b class="lbl">The single number that settles Scenario A</b>
<p>The open-territory licence needs a <b>4.74% peak class share</b> to return its cost of capital. Enavogliflozin's best-ever share, in its home market with every structural advantage, is about 4.9%. That means underwriting a foreign, unpromoted, outcomes-data-free launch to match the originator's home-market peak. Scenario B breaks even at <b>0.92%</b> — because the market is four times larger and the registration is already paid for.</p>
</div>

<h3>Where the answer changes, and where it doesn't</h3>

<div class="e-grids">
<div class="e-grid">
<h4>A — open cluster licence</h4>
<p class="sub">rNPV, US$m. Negative across almost the entire plausible space. Columns = peak class share.</p>
<table>
<thead><tr><th style="text-align:left">CAGR</th><th>1.5%</th><th>2%</th><th>3%</th><th>4%</th><th>5%</th></tr></thead>
<tbody>
<tr><th>0%</th><td class="c-neg">−4.3</td><td class="c-neg">−4.0</td><td class="c-neg">−3.4</td><td class="c-neg">−2.9</td><td class="c-neg">−2.3</td></tr>
<tr><th>2%</th><td class="c-neg">−4.2</td><td class="c-neg">−3.8</td><td class="c-neg">−3.1</td><td class="c-neg">−2.5</td><td class="c-neg">−1.8</td></tr>
<tr><th>5%</th><td class="c-neg">−3.9</td><td class="c-neg">−3.5</td><td class="c-neg">−2.6</td><td class="c-neg">−1.7</td><td class="c-neg">−0.8</td></tr>
<tr><th>8%</th><td class="c-neg">−3.6</td><td class="c-neg">−3.0</td><td class="c-neg">−1.9</td><td class="c-neg">−0.8</td><td class="c-mid">+0.3</td></tr>
<tr><th>10%</th><td class="c-neg">−3.3</td><td class="c-neg">−2.7</td><td class="c-neg">−1.4</td><td class="c-mid">−0.1</td><td class="c-pos">+1.2</td></tr>
</tbody>
</table>
</div>
<div class="e-grid">
<h4>B — Brazil + Mexico rights</h4>
<p class="sub">rNPV, US$m. Positive but never large. Columns = peak class share.</p>
<table>
<thead><tr><th style="text-align:left">CAGR</th><th>1.5%</th><th>2%</th><th>3%</th><th>4%</th><th>5%</th></tr></thead>
<tbody>
<tr><th>0%</th><td class="c-mid">−0.2</td><td class="c-mid">+1.7</td><td class="c-mid">+5.4</td><td class="c-pos">+9.2</td><td class="c-pos">+13.0</td></tr>
<tr><th>2%</th><td class="c-mid">+0.6</td><td class="c-mid">+2.7</td><td class="c-pos">+7.0</td><td class="c-pos">+11.3</td><td class="c-pos">+15.6</td></tr>
<tr><th>5%</th><td class="c-mid">+2.0</td><td class="c-mid">+4.6</td><td class="c-pos">+9.8</td><td class="c-pos">+15.0</td><td class="c-pos">+20.2</td></tr>
<tr><th>8%</th><td class="c-mid">+3.7</td><td class="c-pos">+6.9</td><td class="c-pos">+13.2</td><td class="c-pos">+19.6</td><td class="c-pos">+25.9</td></tr>
<tr><th>10%</th><td class="c-mid">+5.0</td><td class="c-pos">+8.7</td><td class="c-pos">+15.9</td><td class="c-pos">+23.1</td><td class="c-pos">+30.4</td></tr>
</tbody>
</table>
</div>
</div>

<div class="e-scroll">
<table>
<caption>What else moves the answer — Scenario B base case, US$13.2m, flexed one variable at a time</caption>
<thead><tr><th>Variable</th><th>Range</th><th class="n">rNPV</th><th>Implication</th></tr></thead>
<tbody>
<tr><td>Transfer price from Daewoong</td><td>30% → 50% of net sales</td><td class="n">18.4 → 5.4</td><td><b>The most negotiable lever.</b> Every 5 points is ~US$2m of value.</td></tr>
<tr><td>Discount rate</td><td>12% → 20%</td><td class="n">17.2 → 8.4</td><td>Country-risk weighting matters but does not change the sign.</td></tr>
<tr><td>Local bridging study (Scenario A)</td><td>+US$5.5m, +2 yrs</td><td class="n">−1.9 → −4.1</td><td>Turns a marginal case into a clearly bad one.</td></tr>
</tbody>
</table>
</div>

<h3>An asset purchase, priced</h3>

<ul>
<li><b>Open cluster</b> (AR/CO/CL/PE/UY/PY/BO): pay <b>nothing</b> for an outright purchase. If taken at all, take it as a licence with a nominal upfront (≤US$1m), a transfer price at or below 35%, and a right to hand it back.</li>
<li><b>Brazil + Mexico:</b> maximum consideration <b>US$10–13m</b> on an enterprise basis, with no more than 40% at closing. Above US$15m is underwriting the upside case, which needs a 5% peak share and 8%+ class growth in a genericising market.</li>
<li><b>Whole LATAM package</b>, if Daewoong ever restructures: US$12–16m, on the same logic — the open cluster adds volume but essentially no value.</li>
</ul>

<span class="e-num">Part 08</span>
<h2 id="p8">Spend two weeks and no capital confirming the territory register before anyone builds a business case</h2>

<p>The analysis above rests on public disclosure, which is incomplete on exactly the point that matters most. The cheapest possible next step resolves it.</p>

<div class="e-scroll">
<table>
<caption>Next 100 days — sequenced so each stage can kill the project before the next costs money</caption>
<thead><tr><th class="n">Days</th><th>Action</th><th>Kill criterion</th></tr></thead>
<tbody>
<tr><td class="n">0–14</td><td>Direct approach to Daewoong Global BD. Request the signed territory schedule, exclusivity terms and reversion rights for Envlo <i>and</i> Envlomet separately.</td><td><b>Stop if</b> Brazil, Mexico, Colombia, Argentina and Chile are all committed.</td></tr>
<tr><td class="n">14–30</td><td>Confirm whether Envlomet is separately available. The combination is the more defensible product and may sit outside the M8/Arcera grant.</td><td><b>Stop if</b> the FDC follows the mono licence automatically.</td></tr>
<tr><td class="n">14–45</td><td>Regulatory feasibility: written confirmation from local counsel on dossier acceptance of Korean data, GMP recognition, and whether a bridging study is required.</td><td><b>Stop if</b> a bridging study is required in the lead market.</td></tr>
<tr><td class="n">30–60</td><td>Twelve prescriber interviews per lead market: would they switch from generic dapagliflozin on the mild-CKD data alone, and at what price gap?</td><td><b>Stop if</b> stated switching intent implies &lt;2% peak share.</td></tr>
<tr><td class="n">45–75</td><td>Payer and channel test with pharmacy chain buyers and the two largest private insurers per market.</td><td><b>Stop if</b> listing requires parity with generic pricing.</td></tr>
<tr><td class="n">60–100</td><td>Only if all four gates pass: term sheet anchored on a low upfront, transfer price ≤35%, FX protection, mutual sales minimums, and a hand-back right if ENVELOP fails.</td><td class="dim">—</td></tr>
</tbody>
</table>
</div>

<h3>If it proceeds, the terms that matter</h3>

<ul>
<li><b>Transfer price, not royalty.</b> Korean originators usually supply finished product and take margin at the transfer price. Negotiate this above everything else — it is worth more than the upfront.</li>
<li><b>Envlomet must be included</b>, with FDC line extensions. The combination is where durable share lives in emerging markets.</li>
<li><b>ENVELOP as a two-way trigger.</b> Milestones payable on a positive cardiorenal readout; hand-back right, or transfer-price step-down, on a neutral or negative one.</li>
<li><b>Regional manufacturing option from year 4.</b> Technology transfer to a local CMO removes the FX and single-source exposure.</li>
<li><b>Sales minimums must be mutual.</b> One-way minimums on a product with this evidence profile convert a marginal asset into a guaranteed loss.</li>
</ul>

<h3>What would change this recommendation</h3>

<ol>
<li>A positive ENVELOP cardiorenal readout — converts Envlo from a me-too into a guideline-eligible product and roughly doubles the credible peak share.</li>
<li>Brazil or Mexico becoming genuinely available below US$13m.</li>
<li>Envlomet being separately licensable at a transfer price allowing parity pricing with branded generics at 25% contribution — a volume play rather than a premium play.</li>
<li>An obesity or metabolic-liver indication emerging from Daewoong's early metabolic work. Speculative today; worth a watching brief.</li>
</ol>

<h2>Assumptions, and how to break this analysis</h2>

<p>Market values, share assumptions, launch costs and country splits are <b>illustrative</b> and triangulated from the sources below; they are not licensed market-research figures. Prices are September 2026 retail observations converted at roughly R$5.40 and MX$18.50 to the dollar. The Korean class-share anchor uses an estimated Korean SGLT-2 class value. The territory register is reconstructed from press disclosure and must be verified with Daewoong before any decision. The fastest way to break this analysis is to show that Colombia, Argentina or Chile is unencumbered and materially larger than the US$200m cluster assumed here, or that Envlomet is separately available — either would justify re-running Scenario A on better inputs.</p>

<h2>Sources</h2>

<div class="e-src">
<p><a href="https://www.prnewswire.com/news-releases/m8-pharmaceuticals-and-daewoong-pharmaceutical-strengthen-their-strategic-partnership-by-signing-an-exclusive-licensing-agreement-for-envlo-enavoglifozin-for-brazil-and-mexico-301755865.html">M8 Pharmaceuticals and Daewoong — exclusive licence for Envlo, Brazil and Mexico</a></p>
<p><a href="https://evrimagaci.org/gpt/daewoong-signs-major-latin-america-drug-export-deals-516384">Daewoong Latin America export deals, eight additional countries, Nov 2025</a></p>
<p><a href="https://www.koreabiomed.com/news/articleView.html?idxno=31792">Daewoong lands Mexico approval for Enblo/Envlo</a></p>
<p><a href="https://www.globenewswire.com/news-release/2026/06/29/3318648/0/en/Arcera-Life-Sciences-and-Daewoong-Expand-Strategic-Partnership-to-Bring-Enavogliflozin-to-the-Middle-East.html">Arcera Life Sciences and Daewoong expand partnership to the Middle East</a></p>
<p><a href="https://www.koreabiomed.com/news/articleView.html?idxno=32279">Envlo enters MENA in a US$93m licensing deal with Acino</a></p>
<p><a href="https://link.springer.com/article/10.1186/s12933-024-02155-9">Enavogliflozin vs dapagliflozin by renal function — pooled analysis of two RCTs</a></p>
<p><a href="https://www.prnewswire.com/news-releases/daewoong-pharmaceutical-presents-phase-3-clinical-trial-results-of-new-diabetes-treatment-enavogliflozin-and-roadmap-to-enter-50-countries-by-2030-301664432.html">Daewoong phase 3 results for enavogliflozin and global roadmap</a></p>
<p><a href="https://www.e-dmj.org/journal/view.php?doi=10.4093%2Fdmj.2024.0238">ENVELOP: enavogliflozin cardiorenal outcomes trial design</a></p>
<p><a href="https://www.koreabiomed.com/news/articleView.html?idxno=26899">Envlo and Envlomet Korean prescription sales, KRW 12.3bn in 2024</a></p>
<p><a href="https://www.mordorintelligence.com/industry-reports/latin-america-sodium-glucose-cotransport-2-sglt2-inhibitor-market">Latin America SGLT-2 inhibitor market — size, CAGR, Mexico share</a></p>
<p><a href="https://www.gov.br/anvisa/pt-br/assuntos/noticias-anvisa/2026/novo-registro-de-generico-amplia-acesso-ao-tratamento-de-diabetes-tipo-2">ANVISA registers first dapagliflozin + metformin generic, May 2026</a></p>
<p><a href="https://www.cliquefarma.com.br/preco/dapagliflozina">Brazilian retail prices, dapagliflozin generics</a></p>
<p><a href="https://www.drogariaspacheco.com.br/forxiga-10mg-30-comprimidos-revestidos/p">Brazilian retail price, Forxiga 10 mg</a></p>
<p><a href="https://vitau.mx/ingrediente-activo/dapagliflozina">Mexican retail prices, dapagliflozin brand and generic</a></p>
<p><a href="https://www.koreabiomed.com/news/articleView.html?idxno=28057">Daewoong on Envlo's metabolic effects beyond glucose, ADA 2025</a></p>
</div>

</div>
