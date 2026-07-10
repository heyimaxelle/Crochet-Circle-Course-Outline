<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Crochet Circle — Course Outline</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Work+Sans:wght@400;500;600&family=Caveat:wght@600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#FFFFFF;
    --paper-2:#F2F5EC;
    --plum:#1F2B1A;
    --rose:#5C7A4A;
    --rose-deep:#41582F;
    --sage:#C97B4A;
    --mustard:#C97B4A;
    --line:rgba(31,43,26,0.16);
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--paper);
    color:var(--plum);
    font-family:'Work Sans', sans-serif;
    line-height:1.55;
    -webkit-font-smoothing:antialiased;
  }
  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important;}
  }

  /* granny square motif - signature element */
  .granny{
    display:inline-block;
    width:1em; height:1em;
    position:relative;
    flex-shrink:0;
  }
  .granny::before, .granny::after{
    content:"";
    position:absolute;
    inset:0;
    border-radius:3px;
  }
  .granny::before{
    background:var(--rose);
    transform:rotate(0deg);
  }
  .granny::after{
    inset:22%;
    background:var(--paper);
    border-radius:2px;
  }

  header{
    max-width:720px;
    margin:0 auto;
    padding:64px 24px 40px;
    text-align:center;
  }
  .eyebrow{
    font-family:'Caveat', cursive;
    font-size:1.5rem;
    font-weight:700;
    color:var(--rose-deep);
    letter-spacing:0.02em;
  }
  h1{
    font-family:'Fraunces', serif;
    font-optical-sizing:auto;
    font-weight:600;
    font-size:clamp(2.2rem, 6vw, 3.4rem);
    line-height:1.08;
    margin:6px 0 20px;
    color:var(--plum);
  }
  header p.lede{
    font-size:1.08rem;
    max-width:520px;
    margin:0 auto;
    color:rgba(31,43,26,0.82);
  }

  .thread-divider{
    max-width:720px;
    margin:36px auto 0;
    padding:0 24px;
  }
  .thread-divider svg{ width:100%; height:28px; display:block; }

  .outcomes{
    max-width:900px;
    margin:44px auto 0;
    padding:0 24px;
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:18px;
  }
  .outcome-card{
    background:var(--paper-2);
    border-radius:14px;
    padding:20px 18px;
    text-align:center;
  }
  .outcome-card .num{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:2rem;
    color:var(--rose-deep);
    display:block;
  }
  .outcome-card .label{
    font-size:0.92rem;
    color:rgba(31,43,26,0.75);
    margin-top:4px;
  }

  main{
    max-width:760px;
    margin:0 auto;
    padding:72px 24px 40px;
  }

  .section-head{
    display:flex;
    align-items:center;
    gap:10px;
    margin-bottom:10px;
  }
  .section-head h2{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:1.7rem;
  }

  .chain{
    position:relative;
    padding-left:6px;
  }
  .module{
    position:relative;
    padding:0 0 40px 44px;
    border-left:2px dashed var(--line);
  }
  .module:last-child{ border-left:2px dashed transparent; padding-bottom:4px; }
  .module .granny{
    position:absolute;
    left:-13px;
    top:2px;
    width:24px;
    height:24px;
  }
  .module-tag{
    font-family:'Caveat', cursive;
    font-weight:700;
    color:var(--rose-deep);
    font-size:1.15rem;
    display:block;
    margin-bottom:2px;
  }
  .module h3{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:1.28rem;
    margin-bottom:10px;
  }
  .module ul{
    list-style:none;
  }
  .module li{
    position:relative;
    padding-left:20px;
    margin-bottom:7px;
    color:rgba(31,43,26,0.86);
    font-size:0.98rem;
  }
  .module li::before{
    content:"~";
    position:absolute;
    left:0;
    color:var(--sage);
    font-weight:700;
  }
  .module .note{
    display:inline-block;
    margin-top:6px;
    font-size:0.85rem;
    background:rgba(92,122,74,0.16);
    color:#5A6B4C;
    padding:3px 10px;
    border-radius:999px;
  }
  .pattern-grid{
    display:grid;
    grid-template-columns:repeat(2, 1fr);
    gap:8px 20px;
  }
  .pattern-grid li::before{ content:"✽"; color:var(--mustard); font-size:0.85em; top:1px;}

  footer{
    max-width:720px;
    margin:0 auto;
    padding:20px 24px 80px;
    text-align:center;
  }
  .cta{
    display:inline-block;
    text-decoration:none;
    background:var(--rose-deep);
    color:var(--paper);
    border:none;
    font-family:'Work Sans', sans-serif;
    font-weight:600;
    font-size:1rem;
    padding:16px 34px;
    border-radius:999px;
    cursor:pointer;
    box-shadow:0 6px 0 var(--plum);
    transition:transform 0.15s ease, box-shadow 0.15s ease;
  }
  .cta:hover{ transform:translateY(-2px); }
  .cta:active{ transform:translateY(2px); box-shadow:0 3px 0 var(--plum); }
  .cta:focus-visible{ outline:3px solid var(--sage); outline-offset:3px; }
  footer p{
    margin-top:16px;
    font-size:0.9rem;
    color:rgba(31,43,26,0.65);
  }

  @media (max-width:640px){
    .outcomes{ grid-template-columns:1fr; }
    .pattern-grid{ grid-template-columns:1fr; }
  }
</style>
</head>
<body>

<header>
  <div class="eyebrow">🌸 Crochet Circle</div>
  <h1>The Empowerment Class</h1>
  <p class="lede">A beginner-friendly course that turns curious hands into confident makers — 11 finished projects, real skills, and the joy of creating something with your own two hands.</p>
</header>

<div class="thread-divider" aria-hidden="true">
  <svg viewBox="0 0 700 28" preserveAspectRatio="none">
    <path d="M0,14 Q35,0 70,14 T140,14 T210,14 T280,14 T350,14 T420,14 T490,14 T560,14 T630,14 T700,14"
      fill="none" stroke="#D3768A" stroke-width="2.5" stroke-linecap="round"/>
  </svg>
</div>

<section class="outcomes">
  <div class="outcome-card">
    <span class="num">11</span>
    <span class="label">finished projects by the end</span>
  </div>
  <div class="outcome-card">
    <span class="num">5</span>
    <span class="label">guided modules, step by step</span>
  </div>
  <div class="outcome-card">
    <span class="num">1</span>
    <span class="label">new lifelong skill</span>
  </div>
</section>

<main>
  <div class="section-head">
    <span class="granny" style="width:1.3em;height:1.3em;"></span>
    <h2>What your child will learn</h2>
  </div>
  <p style="color:rgba(31,43,26,0.75); margin-bottom:36px; font-size:0.98rem;">Every module builds on the last — starting with the very first stitch and ending with a full pattern library they can keep making from.</p>

  <div class="chain">

    <div class="module">
      <span class="granny"></span>
      <span class="module-tag">Module 1</span>
      <h3>Foundations</h3>
      <ul>
        <li>Crochet tools and their uses</li>
        <li>Crochet terms and abbreviations</li>
        <li>How to hold your hook and create a chain</li>
        <li>Beginner-friendly stitches</li>
        <li>Adding new yarn and changing colors</li>
        <li>How to make a granny square</li>
      </ul>
    </div>

    <div class="module">
      <span class="granny"></span>
      <span class="module-tag">Module 2</span>
      <h3>Granny Square Hat</h3>
      <ul>
        <li>Full tutorial video</li>
        <li>Written pattern notes</li>
      </ul>
      <span class="note">Project 1</span>
    </div>

    <div class="module">
      <span class="granny"></span>
      <span class="module-tag">Module 3</span>
      <h3>Checkerboard Bag</h3>
      <ul>
        <li>Full tutorial video</li>
        <li>Written pattern notes</li>
      </ul>
      <span class="note">Project 2</span>
    </div>

    <div class="module">
      <span class="granny"></span>
      <span class="module-tag">Module 4</span>
      <h3>Bunny Teddy Bear</h3>
      <ul>
        <li>Full tutorial video</li>
        <li>Written pattern notes</li>
      </ul>
      <span class="note">Project 3</span>
    </div>

    <div class="module">
      <span class="granny"></span>
      <span class="module-tag">Module 5</span>
      <h3>Bonus Pattern Library</h3>
      <p style="font-size:0.9rem; color:rgba(31,43,26,0.65); margin-bottom:10px;">Written pattern notes for seven extra makes to keep growing their skills:</p>
      <ul class="pattern-grid">
        <li>Crochet skirt</li>
        <li>Crochet cap-sleeve top</li>
        <li>Crochet sunflower</li>
        <li>Crochet smiski amigurumi</li>
        <li>Mini crochet wallet</li>
        <li>Crochet star bag</li>
        <li>Crochet bunny balaclava</li>
      </ul>
    </div>

  </div>
</main>

<footer>
  <a class="cta" href="https://www.instagram.com/hey.im.axelle" target="_blank" rel="noopener noreferrer">Reserve a spot for my child</a>
  <p>Questions before you enroll? Send us a message — we're happy to walk you through it.</p>
</footer>

</body>
</html>
