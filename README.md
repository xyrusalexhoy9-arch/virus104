
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>virus101</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fredoka:wght@400;500;600&family=Pacifico&display=swap">
<style>
:root{--bg:#ffeaf2;--paper:#fffafc;--ink:#5a1f3a;--wine:#d63a73;--gold:#c28a2c;--gold2:#f3d27a;--line:#f1b8cc;--glow:rgba(214,58,115,.3);--a:#ffc2d8;--b:#ffe3a6;--star:#c28a2c;--on:#fff;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#12060b;--paper:#251018;--ink:#f6e9cf;--wine:#f1b9c4;--gold:#e3c878;--gold2:#fff0b8;--line:#6e5522;--glow:rgba(227,200,120,.4);--a:#5a1428;--b:#3b2a0e;--star:#f0d98f;--on:#12060b}}
:root[data-theme="dark"]{--bg:#12060b;--paper:#251018;--ink:#f6e9cf;--wine:#f1b9c4;--gold:#e3c878;--gold2:#fff0b8;--line:#6e5522;--glow:rgba(227,200,120,.4);--a:#5a1428;--b:#3b2a0e;--star:#f0d98f;--on:#12060b}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
html,body{height:100%;margin:0}
body{background:radial-gradient(ellipse at 50% 25%,var(--paper),var(--bg) 70%);color:var(--ink);font-family:"Fredoka","Trebuchet MS",system-ui,sans-serif;overflow:hidden}
.blob{position:fixed;width:55vmax;height:55vmax;border-radius:50%;filter:blur(80px);opacity:.5;z-index:0;animation:drift 20s ease-in-out infinite alternate}
.b1{background:var(--a);top:-20vmax;left:-15vmax}
.b2{background:var(--b);bottom:-22vmax;right:-18vmax;animation-delay:-8s}
@keyframes drift{to{transform:translate(8vmax,5vmax) scale(1.15)}}
.frame{position:fixed;inset:calc(12px + env(safe-area-inset-top,0px)) 12px calc(12px + env(safe-area-inset-bottom,0px));border:1px solid var(--gold);pointer-events:none;z-index:1;opacity:.75}
.frame::after{content:"";position:absolute;inset:5px;border:1px solid var(--line)}
#fx{position:fixed;inset:0;z-index:0;pointer-events:none}
.scene{position:absolute;inset:0;z-index:2;display:none;flex-direction:column;align-items:center;justify-content:center;gap:.9rem;padding:2.2rem 1.8rem;text-align:center}
.scene.on{display:flex;animation:in .9s ease both}
@keyframes in{from{opacity:0;transform:translateY(14px) scale(.98)}}
h1,h2,p{margin:0}
h1{font-size:clamp(2.4rem,11vw,4.6rem);line-height:1.05;font-weight:600;max-width:9em}
h2{font-size:clamp(1.9rem,8vw,3rem);line-height:1.1;font-weight:600;max-width:12em}
p{font-size:1.2rem;line-height:1.45;max-width:24em}
.shine{background:linear-gradient(100deg,var(--wine) 20%,var(--gold) 42%,var(--gold2) 50%,var(--gold) 58%,var(--wine) 80%);background-size:250% 100%;-webkit-background-clip:text;background-clip:text;color:transparent;animation:rise 1.8s ease both,shine 6s linear 1.8s infinite}
@keyframes rise{0%{opacity:0;transform:scale(.4) translateY(30px);filter:blur(10px)}60%{opacity:1;transform:scale(1.08);filter:blur(0)}80%{transform:scale(.97)}to{transform:scale(1)}}
@keyframes shine{to{background-position:-250% 0}}
.script{font-family:"Pacifico","Brush Script MT",cursive;color:var(--gold);text-shadow:0 0 26px var(--glow);font-weight:400}
.name{font-size:clamp(3rem,15vw,5.2rem);line-height:1.25;animation:in 1.4s .9s ease both,float 3s ease-in-out 2.4s infinite}
.note{font-size:1.6rem;line-height:1.4}
.orn{color:var(--gold);letter-spacing:.7em;font-size:1.2rem}
.medal{width:5.2rem;height:5.2rem;border-radius:50%;border:1px solid var(--gold);outline:1px solid var(--line);outline-offset:5px;display:grid;place-items:center;font-size:2rem;font-weight:600;color:var(--gold);background:var(--paper)}
.big{font-size:clamp(9rem,44vw,15rem);line-height:.9;font-weight:600}
button{font:inherit;cursor:pointer;border:0;border-radius:999px;padding:.65rem 2rem;background:var(--wine);color:var(--on);font-size:1.35rem;font-weight:600;letter-spacing:.04em;box-shadow:0 8px 28px var(--glow);transition:transform .2s}
button:hover{transform:scale(1.05)}
button:focus-visible{outline:3px solid var(--gold);outline-offset:3px}
.ghost{background:transparent;color:var(--ink);border:1px solid var(--gold);box-shadow:none}
.seal{width:104px;height:104px;padding:0;border-radius:50%;background:radial-gradient(circle at 35% 30%,#d94a5c,#8e1328 60%,#5e0b1b);color:#f6d9a0;font-size:2.6rem;position:relative;box-shadow:0 8px 20px rgba(0,0,0,.35),inset 0 -5px 9px rgba(0,0,0,.35),inset 0 3px 6px rgba(255,255,255,.25);text-shadow:0 -1px 1px rgba(0,0,0,.5);animation:pulse 2.4s ease-in-out infinite}
.seal::after{content:"";position:absolute;inset:10px;border-radius:50%;border:2px dashed rgba(246,217,160,.5)}
@keyframes pulse{50%{transform:scale(1.07) rotate(-4deg);box-shadow:0 0 0 16px transparent,0 8px 46px var(--glow)}}
.chips{display:flex;gap:.6rem;flex-wrap:wrap;justify-content:center}
.chips span{padding:.2rem 1rem;border:1px solid var(--gold);border-radius:999px;font-size:1.25rem;background:var(--paper);animation:in .8s both}
.chips span:nth-child(1){animation-delay:1.6s}.chips span:nth-child(2){animation-delay:1.9s}.chips span:nth-child(3){animation-delay:2.2s}
.hearts{display:flex;gap:1rem}
.hearts button{width:4.2rem;height:4.2rem;padding:0;font-size:2rem;background:var(--paper);color:var(--wine);border:1px solid var(--gold);box-shadow:none}
.hearts button.open{transform:scale(1.15);background:var(--wine);color:var(--gold2);box-shadow:0 0 28px var(--glow)}
#reason{min-height:3.6em;font-size:1.3rem}
#no{position:absolute}
.letter{background:var(--paper);border:1px solid var(--gold);outline:1px solid var(--line);outline-offset:-8px;border-radius:6px;padding:1.7rem 1.5rem;width:min(26em,100%);height:min(54vh,25rem);overflow-y:auto;font-size:1.1rem;line-height:1.65;text-align:left;white-space:pre-line;box-shadow:0 10px 50px var(--glow)}
.medal{box-shadow:0 0 24px var(--glow);animation:halo 3s ease-in-out infinite}
@keyframes halo{50%{box-shadow:0 0 0 14px transparent,0 0 44px var(--glow)}}
.seal.crack{animation:crack .8s ease forwards}
@keyframes crack{20%{transform:scale(1.15) rotate(8deg)}40%{transform:scale(.95) rotate(-8deg)}to{transform:scale(1.7);opacity:0;filter:blur(6px)}}
.heartwrap{position:relative;width:min(72vw,17rem);height:min(66vw,16rem)}
.constel{position:absolute;inset:0}
.heartwrap .big{position:absolute;inset:0;display:grid;place-items:center;font-size:clamp(3.4rem,17vw,5.2rem);margin-top:-1rem}
.st{position:absolute;width:11px;height:11px;margin:-5.5px;border-radius:50%;background:var(--line);opacity:.7}
.st.on{background:var(--gold2);border:1px solid var(--gold);opacity:1;box-shadow:0 0 14px var(--gold),0 0 4px var(--gold2);animation:pop .6s ease both}
@keyframes pop{from{transform:scale(0)}60%{transform:scale(2)}}
.beat{animation:beat 1.1s ease-in-out infinite}
@keyframes beat{0%,45%,100%{transform:scale(1)}15%{transform:scale(1.15)}30%{transform:scale(1.02)}}
.frame b{position:absolute;font-size:1.7rem;font-weight:400;line-height:1;animation:sway 4s ease-in-out infinite alternate}
.c1{top:-12px;left:-8px}.c2{top:-12px;right:-8px}.c3{bottom:-12px;left:-8px}.c4{bottom:-12px;right:-8px}
@keyframes sway{to{transform:rotate(14deg) scale(1.12)}}
.cat{position:fixed;bottom:calc(10px + env(safe-area-inset-bottom,0px));z-index:3;font-size:3rem;line-height:1;cursor:pointer;user-select:none;transform-origin:50% 100%;animation:sway2 3s ease-in-out infinite alternate}
.cl{left:14%}.cr{right:14%;animation-delay:-1.5s}
@keyframes sway2{to{transform:rotate(7deg) translateY(-3px)}}
.bub{position:fixed;z-index:4;bottom:calc(5.2rem + env(safe-area-inset-bottom,0px));left:50%;transform:translateX(-50%);background:var(--paper);border:1px solid var(--gold);border-radius:18px;padding:.3rem 1rem;font-size:1.1rem;box-shadow:0 4px 20px var(--glow);opacity:0;pointer-events:none;transition:opacity .25s;white-space:nowrap}
.bub.on{opacity:1}
@keyframes float{50%{transform:translateY(-8px) rotate(-2deg)}}
@keyframes wig{0%,100%{transform:rotate(0)}25%{transform:rotate(-9deg)}75%{transform:rotate(9deg)}}
.hearts button{animation:wig 2.4s ease-in-out infinite}
.hearts button:nth-child(2){animation-delay:-.8s}.hearts button:nth-child(3){animation-delay:-1.6s}
.hearts button.open{animation:none}
button:active{transform:scale(.92)}
.walker{position:fixed;top:calc(2.4rem + env(safe-area-inset-top,0px));left:-4rem;z-index:3;font-size:2.4rem;line-height:1;pointer-events:none;animation:walk 16s linear 3s infinite,hop .5s ease-in-out infinite}
@keyframes walk{to{left:110vw}}
@keyframes hop{0%,100%{transform:scaleX(-1)}50%{transform:scaleX(-1) translateY(-9px)}}
[hidden]{display:none!important}
.lilybtn{width:5.2rem;height:5.2rem;padding:0;border-radius:50%;background:var(--paper);border:2px solid var(--wine);display:grid;place-items:center;animation:pulse 2.2s ease-in-out infinite}
.lilybtn svg{width:3.6rem;height:3.6rem}
.lilyart{width:min(70vw,15rem);height:auto;overflow:visible}
.pt{transform-origin:0 0;transform:rotate(0deg) scale(.25,.5);opacity:0;animation:budin .6s ease 2.4s forwards,open 2.4s cubic-bezier(.2,.9,.3,1.15) calc(3.2s + var(--i)*.28s) forwards}
@keyframes budin{to{opacity:1}}
@keyframes open{to{transform:rotate(var(--r)) scale(var(--s,1))}}
.stem{stroke-dasharray:320;stroke-dashoffset:320;animation:draw 2.2s ease .3s forwards}
@keyframes draw{to{stroke-dashoffset:0}}
.lf,.sm{transform-origin:0 0;transform:scale(0);animation:grow 1.4s cubic-bezier(.2,.9,.3,1.3) 1.6s forwards}
.sm{animation-delay:5.4s}
@keyframes grow{to{transform:scale(1)}}
.glow{opacity:0;animation:glow 3s ease 4.6s forwards}
@keyframes glow{to{opacity:.55}}
.lt{animation:fadeup 1.2s ease 6.8s both}
#lt2{animation-delay:7.6s}
@keyframes fadeup{from{opacity:0;transform:translateY(14px)}}
.date{color:var(--gold);font-size:1.05rem;letter-spacing:.12em}
.flash{position:fixed;inset:0;z-index:5;pointer-events:none;opacity:0;background:radial-gradient(circle,rgba(255,255,255,.95) 0,rgba(255,200,222,.8) 40%,transparent 72%)}
.flash.on{animation:flash .9s ease}
@keyframes flash{30%{opacity:.85}to{opacity:0}}
.stage{position:relative;display:grid;place-items:center}
.rays{position:absolute;left:50%;top:34%;width:130vmin;height:130vmin;border-radius:50%;background:repeating-conic-gradient(rgba(255,170,205,.38) 0 5deg,transparent 5deg 20deg);-webkit-mask-image:radial-gradient(circle,#000 0,transparent 62%);mask-image:radial-gradient(circle,#000 0,transparent 62%);opacity:0;transform:translate(-50%,-50%);animation:rayin 2s ease 4.6s forwards,spin 50s linear 4.6s infinite}
@keyframes rayin{to{opacity:1}}
@keyframes spin{to{transform:translate(-50%,-50%) rotate(360deg)}}
.sway{transform-origin:150px 432px;animation:sway 5s ease-in-out 7s infinite alternate}
@keyframes sway{from{transform:rotate(-1.6deg)}to{transform:rotate(1.6deg)}}
.dew circle{fill:#fff;opacity:0;transform-box:fill-box;transform-origin:center;animation:twk 2.4s ease-in-out 6.5s infinite}
.dew circle:nth-child(2){animation-delay:7.2s}.dew circle:nth-child(3){animation-delay:7.9s}.dew circle:nth-child(4){animation-delay:8.4s}.dew circle:nth-child(5){animation-delay:9s}
@keyframes twk{50%{opacity:.95;transform:scale(1.7)}}
#lt3{animation-delay:8.6s}
.bk{position:absolute;bottom:-40px;border-radius:50%;background:radial-gradient(circle,rgba(255,190,215,.75),rgba(255,190,215,0) 70%);opacity:0;pointer-events:none;animation:bk 10s linear infinite}
@keyframes bk{10%{opacity:.8}to{transform:translateY(-110vh);opacity:0}}
@media(prefers-reduced-motion:reduce){.rays,.sway,.dew circle,.flash,.bk{animation:none}.flash,.bk{display:none}.rays{opacity:.6}}
@media(prefers-reduced-motion:reduce){.pt,.stem,.lf,.sm,.glow,.lt,.lilybtn{animation:none}.pt{opacity:1;transform:rotate(var(--r)) scale(var(--s,1))}.stem{stroke-dashoffset:0}.lf,.sm{transform:scale(1)}.glow{opacity:.5}}
@media(prefers-reduced-motion:reduce){.walker,.hearts button,.cat,.frame b,.medal,.beat,.st.on,.blob,.seal,.shine,.name,.scene.on,.chips span{animation:none}.shine{color:var(--wine);background:none}}
</style>
</head>
<body>
<div class="blob b1"></div><div class="blob b2"></div>
<canvas id="fx"></canvas>
<div class="flash" id="flash"></div>
<div class="frame"><b class="c1">🌷</b><b class="c2">🌸</b><b class="c3">🌼</b><b class="c4">🌸</b></div>
<div class="cat cl" id="c1" role="button" aria-label="Cat">🐈</div><div class="cat cr" id="c2" role="button" aria-label="Cat">🐱</div><div class="bub" id="bub"></div><div class="walker" aria-hidden="true">🐈</div>

<section class="scene on" id="s0">
  <div class="medal">II</div>
  <h1 class="shine">Happy 2nd Anniversary</h1>
  <div class="script name">Beb</div>
  <div class="orn">🌷 ❦ 🐱 ❦ 🌷</div>
  <p class="date">November 20, 2026</p>
  <p>Click the flower</p>
  <button class="seal" id="open" aria-label="Click the flower">🌸</button>
</section>

<section class="scene" id="s1">
  <p class="script note">Two beautiful years</p>
  <div class="heartwrap"><div class="constel" id="constel"></div><div class="big shine" id="count">0</div></div>
  <h2 id="mlabel">months, one star each</h2>
  
  <button data-next>Continue</button>
</section>

<section class="scene" id="s2">
  <h2>Why I love you</h2>
  <p>Touch each one</p>
  <div class="hearts" id="hearts"></div>
  <p id="reason"></p>
  <button data-next id="n2" hidden>One more thing</button>
</section>

<section class="scene" id="s3">
  <h2>Do you still love me, Beb?</h2>
  <p id="hint">You only have two choices</p>
  <button id="yes">Always</button>
  <button class="ghost" id="no">No</button>
</section>

<section class="scene" id="s4">
  <p class="script note" id="endnote">Happy 2nd Anniversary</p>
  <div class="letter" id="letter" tabindex="0"></div>
  <button class="lilybtn" id="lily" hidden aria-label="Press the pink lily"><svg viewBox="-125 -125 250 250" aria-hidden="true"><use href="#petal" transform="rotate(0)"/><use href="#petal" transform="rotate(120)"/><use href="#petal" transform="rotate(240)"/><use href="#petal" transform="rotate(60) scale(.92)"/><use href="#petal" transform="rotate(180) scale(.92)"/><use href="#petal" transform="rotate(300) scale(.92)"/><circle r="9" fill="#c9de7a"/></svg></button>
  <p id="lilyhint" hidden>Press the pink lily</p>
</section>

<svg width="0" height="0" style="position:absolute" aria-hidden="true"><defs>
<linearGradient id="pg" x1="0" y1="1" x2="0" y2="0"><stop offset="0" stop-color="#e9f2a0"/><stop offset=".12" stop-color="#fff0c8"/><stop offset=".3" stop-color="#ffc4dc"/><stop offset=".65" stop-color="#ff86b6"/><stop offset="1" stop-color="#f0477f"/></linearGradient>
<linearGradient id="pg2" x1="0" y1="1" x2="0" y2="0"><stop offset="0" stop-color="#fff" stop-opacity="0"/><stop offset=".6" stop-color="#fff" stop-opacity=".5"/><stop offset="1" stop-color="#fff" stop-opacity="0"/></linearGradient>
<radialGradient id="gl"><stop offset="0" stop-color="#ffb3d1" stop-opacity=".9"/><stop offset="1" stop-color="#ffb3d1" stop-opacity="0"/></radialGradient>
<g id="petal"><path d="M0 0C-30-30-34-78-8-112Q0-132 8-112C34-78 30-30 0 0Z" fill="url(#pg)" stroke="#ffd6e6" stroke-width="1.2"/><path d="M0 0C-12-30-14-70 0-118C14-70 12-30 0 0Z" fill="url(#pg2)" opacity=".55"/><path d="M0-6V-104" stroke="#d92f6f" stroke-width="1.8" opacity=".5" fill="none" stroke-linecap="round"/><path d="M-5-14C-14-44-14-74-3-102M5-14C14-44 14-74 3-102" stroke="#fff" stroke-width="1" opacity=".3" fill="none"/><g fill="#b0245f" opacity=".7"><circle cx="-7" cy="-30" r="1.8"/><circle cx="8" cy="-36" r="1.7"/><circle cx="-4" cy="-46" r="2"/><circle cx="7" cy="-54" r="1.6"/><circle cx="-9" cy="-58" r="1.5"/><circle cx="3" cy="-66" r="1.8"/><circle cx="-6" cy="-74" r="1.3"/><circle cx="8" cy="-72" r="1.2"/><circle cx="0" cy="-84" r="1.1"/></g></g>
<g id="an"><path d="M0 0Q7-28 3-52" stroke="#f1dc8a" stroke-width="2.4" fill="none" stroke-linecap="round"/><ellipse cx="3" cy="-57" rx="4.2" ry="10" fill="#b5502b" transform="rotate(8 3 -57)"/><circle cx="1" cy="-65" r="1.7" fill="#ffb45e"/><circle cx="6" cy="-50" r="1.3" fill="#ffb45e"/></g>
</defs></svg>

<section class="scene" id="s5">
  <div class="stage"><div class="rays"></div><svg class="lilyart" viewBox="0 0 300 440" aria-label="A pink lily blooming">
    <circle class="glow" cx="150" cy="150" r="150" fill="url(#gl)"/>
    <g class="sway"><path class="stem" d="M150 432C148 360 154 250 150 152" fill="none" stroke="#3f9d62" stroke-width="8" stroke-linecap="round"/>
    <g transform="translate(149,350)"><path class="lf" d="M0 0C40-10 80-40 110-95 70-55 35-25 0 0Z" fill="#3f9d62"/></g>
    <g transform="translate(151,300) scale(-1,1)"><path class="lf" style="animation-delay:2s" d="M0 0C34-8 66-34 92-80 58-46 28-20 0 0Z" fill="#35875a"/></g>
    <g transform="translate(150,150)">
      <use href="#petal" class="pt" style="--r:0deg;--i:0;--s:1"/>
      <use href="#petal" class="pt" style="--r:120deg;--i:2;--s:1"/>
      <use href="#petal" class="pt" style="--r:240deg;--i:4;--s:1"/>
      <use href="#petal" class="pt" style="--r:60deg;--i:1;--s:.92"/>
      <use href="#petal" class="pt" style="--r:180deg;--i:3;--s:.92"/>
      <use href="#petal" class="pt" style="--r:300deg;--i:5;--s:.92"/>
      <g class="sm"><path d="M0 0Q-5-34 0-70" stroke="#b9d46a" stroke-width="3.4" fill="none" stroke-linecap="round"/><circle cx="-3" cy="-74" r="3.4" fill="#8fbf4f"/><circle cx="3" cy="-74" r="3.4" fill="#8fbf4f"/><circle cx="0" cy="-77" r="3.4" fill="#8fbf4f"/><use href="#an"/><use href="#an" transform="rotate(60)"/><use href="#an" transform="rotate(120)"/><use href="#an" transform="rotate(180)"/><use href="#an" transform="rotate(240)"/><use href="#an" transform="rotate(300)"/><circle r="7" fill="#c9de7a"/></g>
      <g class="dew"><circle cx="-28" cy="-62" r="2.4"/><circle cx="34" cy="-48" r="2"/><circle cx="-46" cy="22" r="2.2"/><circle cx="40" cy="58" r="2.4"/><circle cx="6" cy="-92" r="2"/></g>
    </g>
  </g></svg></div>
  <p class="script note lt" id="lt1">My favorite pink lily</p>
  <p class="lt" id="lt2">Just like this lily, you made my whole life bloom. Happy 2nd Anniversary, Beb. I love you. 🌸</p>
  <p class="script note lt" id="lt3">November 20, 2026</p>
</section>

<script>
/* EDIT HERE: reasons and letter */
const C={
  years:2,
  reasons:[
    "Because I’m handsome 😎",
    "Because you’re so cute.",
    "Because you’re the only moody one who’s still cute."
  ],
  letter:"My dearest Beb,\n\nTwo years. Sometimes I still can’t believe it, because every day with you feels like the first good day all over again. Thank you for choosing me, for staying, and for loving me even on the days I made it hard.\n\nThank you for every laugh, every late-night conversation, and every time you understood me without me saying a word. You’ve seen me at my best and at my worst, and you stayed anyway. I will never take that for granted.\n\nYes, you can be moody, and yes, I’ve learned to read the weather. But even on your stormiest days you’re still the cutest person I know, and I would choose every one of those days over a quiet life without you.\n\nYou are my home, my favorite person, and my best decision. I promise to keep making you laugh, to keep showing up, and to love you a little more every day. Here’s to our second year, and to every year after this one.\n\nHappy 2nd Anniversary, Beb. I love you, always.\n\nForever yours,\nYour Pogi 🐾"
};
const $=id=>document.getElementById(id),RM=matchMedia("(prefers-reduced-motion:reduce)").matches;
const sc=[...document.querySelectorAll(".scene")];
const cv=$("fx"),x=cv.getContext("2d");let W,H,P=[],S=[],T=0,col="#fff",tw;
function rs(){W=cv.width=innerWidth;H=cv.height=innerHeight;
  col=getComputedStyle(document.documentElement).getPropertyValue("--star").trim()||"#fff";
  S=Array.from({length:60},()=>({x:Math.random()*W,y:Math.random()*H,r:Math.random()*1.5+.4,p:Math.random()*6,s:Math.random()*2+.6}))}
addEventListener("resize",rs);rs();
function spawn(px,py,n,ch,o={}){if(RM)return;
  for(let i=0;i<n;i++){const a=Math.random()*6.283,v=(o.v||5)*(.4+Math.random());
    P.push({x:px,y:py,vx:Math.cos(a)*v,vy:Math.sin(a)*v,g:o.g??.12,l:0,m:(o.m||70)+Math.random()*40,c:ch[i%ch.length],z:(o.z||18)+Math.random()*14,r:Math.random()*6,vr:(Math.random()-.5)*.1})}}
function drop(from,n,ch){if(RM)return;
  for(let i=0;i<n;i++)P.push({x:Math.random()*W,y:from?-20:H+20,vx:(Math.random()-.5)*(from?2:.6),vy:from?2+Math.random()*3:-(.8+Math.random()),g:from?.02:0,l:0,m:from?260:600,c:ch[i%ch.length],z:14+Math.random()*16,r:0,vr:(Math.random()-.5)*.1})}
function frame(){T+=.016;x.clearRect(0,0,W,H);x.fillStyle=col;
  for(const s of S){x.globalAlpha=.15+.6*Math.abs(Math.sin(T*s.s+s.p));x.beginPath();x.arc(s.x,s.y,s.r,0,6.283);x.fill()}
  for(const s of SS){s.l++;s.x+=s.vx;s.y+=s.vy;x.globalAlpha=Math.max(0,1-s.l/40);x.strokeStyle=col;x.lineWidth=2;x.beginPath();x.moveTo(s.x,s.y);x.lineTo(s.x-s.vx*5,s.y-s.vy*5);x.stroke()}SS=SS.filter(s=>s.l<40);
  x.textAlign="center";x.textBaseline="middle";
  P=P.filter(p=>p.l<p.m);
  for(const p of P){p.l++;p.vy+=p.g;p.x+=p.vx;p.y+=p.vy;p.vx*=.99;p.r+=p.vr;
    x.globalAlpha=Math.max(0,1-p.l/p.m);x.font=p.z+"px serif";x.save();x.translate(p.x,p.y);x.rotate(p.r);x.fillText(p.c,0,0);x.restore()}
  x.globalAlpha=1;requestAnimationFrame(frame)}
let SS=[];if(!RM){frame();setInterval(()=>SS.push({x:Math.random()*W*.6,y:Math.random()*H*.3,vx:9,vy:4,l:0}),5000);setInterval(()=>drop(false,1,["🌸","🌷","🐱","🐾","🌼","🌹"]),700)}
addEventListener("pointermove",e=>{if(Math.random()<.5)spawn(e.clientX,e.clientY,1,["✦","✧"],{v:1.2,g:.02,m:30,z:14})});
addEventListener("pointerdown",e=>spawn(e.clientX,e.clientY,10,["🌸","🐱","🌷","✨","🐾","♥"],{v:6,m:60}));

function go(n){const f=$("flash");f.classList.remove("on");void f.offsetWidth;f.classList.add("on");sc.forEach((s,i)=>s.classList.toggle("on",i===n));if(n===1)count();if(n===4)finish();if(n===5)bloom()}
function count(){const k=$("constel"),el=$("count");k.innerHTML="";el.textContent="0";$("mlabel").textContent="months, one star each";
  const pts=[];for(let i=0;i<24;i++){const t=i/24*6.2832,px=16*Math.sin(t)**3,py=13*Math.cos(t)-5*Math.cos(2*t)-2*Math.cos(3*t)-Math.cos(4*t);
    const d=document.createElement("i");d.className="st";d.style.left=50+px/16*46+"%";d.style.top=50-(py+2.5)/14.5*44+"%";k.appendChild(d);pts.push(d)}
  let v=0;const t=setInterval(()=>{pts[v].classList.add("on");const r=pts[v].getBoundingClientRect();spawn(r.left,r.top,4,["✦"],{v:3,m:40});el.textContent=++v;
    if(v>=24){clearInterval(t);$("mlabel").textContent="Two years with you";spawn(W/2,H*.4,40,["🌸","🐱","🌷","💖","🐾"],{v:9,m:100})}},130)}
function type(el,t,done){clearInterval(tw);el.textContent="";if(RM){el.textContent=t;done&&done();return}const a=Array.from(t);
  let i=0;tw=setInterval(()=>{el.textContent=a.slice(0,++i).join("");el.scrollTop=el.scrollHeight;if(i>=a.length){clearInterval(tw);done&&done()}},18);
  el.onclick=()=>{clearInterval(tw);el.textContent=t;done&&done()}}
$("open").onclick=()=>{const r=$("open").getBoundingClientRect();spawn(r.left+r.width/2,r.top+r.height/2,30,["🌸","🐱","🌷","💖","🐾"],{v:9,m:90});$("open").classList.add("crack");setTimeout(()=>go(1),RM?0:800)};
document.querySelectorAll("[data-next]").forEach(b=>b.onclick=()=>go(sc.findIndex(s=>s.classList.contains("on"))+1));

let opened=0;
C.reasons.forEach((r,i)=>{const b=document.createElement("button");b.textContent=["🌷","🐱","🌸"][i];b.setAttribute("aria-label","Reason "+(i+1));
  b.onclick=()=>{type($("reason"),r);if(!b.classList.contains("open")){b.classList.add("open");opened++}
    if(opened===C.reasons.length)$("n2").hidden=false};
  $("hearts").appendChild(b)});

const says=["Meow! 🐾","Happy 2nd Anniversary, Beb!","Purr purr… I love you too","Beb, you’re so cute","Mew mew ♥","Beb + Pogi forever"];let bt;
function meow(e){e.stopPropagation();const b=$("bub");b.textContent=says[Math.floor(Math.random()*says.length)];b.classList.add("on");clearTimeout(bt);bt=setTimeout(()=>b.classList.remove("on"),1800);const r=e.currentTarget.getBoundingClientRect();spawn(r.left+r.width/2,r.top,8,["💖","🐾","🌸"],{v:5,m:60})}
$("c1").onclick=meow;$("c2").onclick=meow;
const no=$("no");let dodges=0;
function dodge(e){e.preventDefault();dodges++;
  const s=$("s3").getBoundingClientRect(),b=no.getBoundingClientRect();
  no.style.left=Math.random()*(s.width-b.width-16)+8+"px";
  no.style.top=Math.random()*(s.height-b.height-16)+8+"px";
  $("hint").textContent=dodges>4?"Just press Always already, Beb":"You can’t catch the No button"}
["pointerenter","pointerdown","click"].forEach(t=>no.addEventListener(t,dodge));
$("yes").onclick=()=>go(4);

function bloom(){const s5=$("s5");if(!s5.querySelector(".bk")&&!RM)for(let i=0;i<14;i++){const b=document.createElement("i"),z=14+Math.random()*30;b.className="bk";b.style.cssText="left:"+Math.random()*100+"%;width:"+z+"px;height:"+z+"px;animation-delay:"+(Math.random()*8+3)+"s;animation-duration:"+(8+Math.random()*8)+"s";s5.appendChild(b)}
  const c=()=>{const b=document.querySelector("#s5 svg.lilyart").getBoundingClientRect();return[b.left+b.width/2,b.top+b.height*.34]};
  setTimeout(()=>{const[p,q]=c();spawn(p,q,30,["🌸","✨","💖"],{v:8,m:100})},3300);
  setTimeout(()=>{const[p,q]=c();spawn(p,q,50,["🌸","✨","💖","🌷"],{v:11,m:120});fire()},5200);
  setTimeout(()=>{if(RM)return;let n=0;const t=setInterval(()=>{const[p,q]=c();spawn(p,q,2,["✦","✧"],{v:1.6,g:-.03,m:110,z:14});drop(true,1,["🌸"]);if(++n>60)clearInterval(t)},200)},5600)}
$("lily").onclick=()=>go(5);
function fire(){if(RM)return;let n=0;const f=setInterval(()=>{const px=W*(.15+Math.random()*.7),py=H*(.12+Math.random()*.35);spawn(px,py,36,["✦","•","✧","✨"],{v:7,g:.06,m:70,z:16});if(++n>7)clearInterval(f)},550)}
function finish(){$("endnote").textContent="Happy 2nd Anniversary";$("endnote").classList.remove("beat");$("lily").hidden=true;$("lilyhint").hidden=true;type($("letter"),C.letter,()=>{$("endnote").textContent="I love you, Beb";$("endnote").classList.add("beat");$("lily").hidden=false;$("lilyhint").hidden=false});fire();spawn(W/2,H*.5,40,["🌸","🐱","🌷","💖","🐾","✨"],{v:10,m:100});
  if(RM)return;let n=0;const r=setInterval(()=>{drop(true,6,["🌸","🌷","🐱","🌼","🐾","💖","✨"]);if(++n>14)clearInterval(r)},250)}
function reset(){opened=0;dodges=0;clearInterval(tw);$("n2").hidden=true;$("reason").textContent="";
  document.querySelectorAll(".hearts button").forEach(b=>b.classList.remove("open"));
  $("open").classList.remove("crack");no.removeAttribute("style");$("hint").textContent="You only have two choices";go(0)};
</script>
</body>
</html>
