
<!doctype html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#070b1c">
<title>Batalha Matemática | Arena Gamer</title>

<style>
:root{
  --bg:#070b1c;
  --card:#101a35;
  --card2:#142344;
  --cyan:#35e7ff;
  --purple:#a477ff;
  --blue:#526dff;
  --green:#55f5bd;
  --text:#f4f7ff;
  --muted:#9caccb;
  --border:#30466f;
  --danger:#ff647f;
}

*{box-sizing:border-box}

html{scroll-behavior:smooth}

body{
 margin:0;
 min-height:100vh;
 padding:22px;
 color:var(--text);
 font-family:Inter,system-ui,Arial,sans-serif;
 background:
 radial-gradient(ellipse at 15% 5%,#243b85 0%,transparent 38%),
 radial-gradient(ellipse at 90% 20%,#422477 0%,transparent 35%),
 radial-gradient(ellipse at 50% 100%,#102e50 0%,transparent 45%),
 var(--bg);
 background-attachment:fixed;
 overflow-x:hidden;
}

body:before{
 content:"";
 position:fixed;
 inset:0;
 pointer-events:none;
 opacity:.13;
 background-image:
 linear-gradient(#8b9fff22 1px,transparent 1px),
 linear-gradient(90deg,#8b9fff22 1px,transparent 1px);
 background-size:42px 42px;
 mask-image:linear-gradient(to bottom,black,transparent 85%);
 z-index:-1;
}

main{
 max-width:900px;
 margin:auto;
 position:relative;
}

.brand{
 text-align:center;
 margin:20px 0 30px;
}

.brand h1{
 font-size:clamp(2rem,7vw,3.7rem);
 font-weight:1000;
 letter-spacing:2px;
 margin:0;
 color:var(--cyan);
 text-shadow:
 0 0 10px #35e7ff99,
 0 0 28px #35e7ff66,
 0 0 55px #526dff66;
}

.brand p{
 color:var(--muted);
 font-size:1rem;
 letter-spacing:1px;
}

.card{
 position:relative;
 overflow:hidden;
 background:linear-gradient(145deg,#142343f5,#0c1630f7);
 border:1px solid var(--border);
 border-radius:23px;
 padding:26px;
 margin:18px 0;
 box-shadow:
 0 20px 55px #0007,
 inset 0 1px 0 #ffffff0c;
 backdrop-filter:blur(15px);
 animation:appear .35s ease;
}

.card:before{
 content:"";
 position:absolute;
 top:0;
 left:0;
 right:0;
 height:2px;
 background:linear-gradient(90deg,transparent,var(--cyan),var(--purple),transparent);
 opacity:.85;
}

@keyframes appear{
 from{opacity:0;transform:translateY(10px)}
 to{opacity:1;transform:translateY(0)}
}

h2{
 margin-top:0;
 font-size:1.55rem;
 color:var(--text);
}

h3{
 color:var(--cyan);
 margin-top:25px;
}

label{
 display:block;
 color:#d5e2ff;
 font-weight:700;
 margin-top:15px;
}

input{
 width:100%;
 padding:16px;
 border-radius:13px;
 border:1px solid #3b5682;
 background:#080f24;
 color:white;
 font-size:1rem;
 margin:9px 0 15px;
 outline:none;
 transition:.25s;
}

input:focus{
 border-color:var(--cyan);
 box-shadow:0 0 0 3px #35e7ff20,0 0 20px #35e7ff20;
}

input::placeholder{color:#7384a8}

button{
 border:1px solid transparent;
 border-radius:13px;
 padding:14px 20px;
 font-weight:850;
 font-size:1rem;
 cursor:pointer;
 color:#071426;
 background:linear-gradient(110deg,var(--cyan),#75f5d0);
 box-shadow:0 5px 20px #35e7ff22;
 transition:transform .2s,box-shadow .2s,filter .2s;
 margin:5px;
}

button:hover:not(:disabled){
 transform:translateY(-3px);
 box-shadow:0 9px 28px #35e7ff40;
 filter:brightness(1.1);
}

button:active:not(:disabled){
 transform:scale(.97);
}

button.alt{
 color:white;
 background:linear-gradient(110deg,#6954db,#a477ff);
 box-shadow:0 5px 20px #a477ff30;
}

button:disabled{
 opacity:.4;
 cursor:not-allowed;
 transform:none;
}

.actions{
 display:flex;
 gap:10px;
 flex-wrap:wrap;
 margin-top:12px;
}

.actions button{
 flex:1;
 min-width:140px;
}

hr{
 border:0;
 border-top:1px solid var(--border);
 margin:24px 0;
}

.hidden{display:none!important}

.pin{
 font-size:clamp(2.2rem,9vw,3.4rem);
 letter-spacing:9px;
 color:var(--cyan);
 font-weight:1000;
 text-align:center;
 padding:20px 10px;
 margin:15px 0;
 border-radius:18px;
 border:1px solid #35e7ff55;
 background:linear-gradient(120deg,#142f50,#202052);
 text-shadow:0 0 18px #35e7ff99;
 box-shadow:inset 0 0 25px #35e7ff12,0 0 25px #35e7ff12;
}

.player{
 padding:14px 16px;
 background:linear-gradient(100deg,#1a3155,#172344);
 border:1px solid #354e77;
 border-radius:13px;
 margin:9px 0;
 display:flex;
 justify-content:space-between;
 align-items:center;
 gap:10px;
 transition:.2s;
}

.player:hover{
 border-color:var(--cyan);
 background:#203b62;
}

.player b{
 color:var(--cyan);
 white-space:nowrap;
}

.question{
 font-size:clamp(1.25rem,4vw,1.8rem);
 font-weight:900;
 line-height:1.5;
 padding:22px;
 margin:20px 0;
 border:1px solid #526dff66;
 border-radius:17px;
 background:linear-gradient(130deg,#172c50,#251c50);
 box-shadow:inset 0 0 30px #526dff12;
}

.answers{
 display:grid;
 grid-template-columns:1fr 1fr;
 gap:13px;
 margin-top:20px;
}

.answers button{
 min-height:75px;
 color:white;
 font-size:1.05rem;
 background:linear-gradient(135deg,#1d365c,#202b50);
 border:1px solid #526dff88;
 box-shadow:0 5px 18px #0003;
}

.answers button:hover:not(:disabled){
 border-color:var(--cyan);
 background:linear-gradient(135deg,#245078,#34356e);
 box-shadow:0 0 20px #35e7ff25;
}

.answers button:disabled{
 opacity:.65;
}

.meta{
 display:flex;
 justify-content:space-between;
 align-items:center;
 gap:12px;
 color:var(--muted);
 flex-wrap:wrap;
 font-weight:750;
}

#roundInfo{
 color:var(--cyan);
 font-size:1.05rem;
}

#timer{
 color:var(--cyan);
 font-size:1.35rem;
}

#timeBar{
 transition:width .25s linear;
 box-shadow:0 0 15px #35e7ff99;
}

.notice{
 color:#ffd27a;
 min-height:24px;
 margin-top:15px;
 font-weight:650;
}

.good{color:var(--green)}
.bad{color:var(--danger)}

#finalRanking .player:first-child{
 border-color:#ffcf5a;
 background:linear-gradient(100deg,#453b24,#24304b);
}

#finalRanking .player:nth-child(2){
 border-color:#b6c9e8;
}

#finalRanking .player:nth-child(3){
 border-color:#c58d62;
}

#nextBtn{
 margin-top:15px;
 width:100%;
}

#startBtn{
 background:linear-gradient(110deg,#35e7ff,#55f5bd);
}

footer{
 text-align:center;
 color:#8193b8;
 font-size:.85rem;
 margin:30px 0 15px;
 letter-spacing:.5px;
}

@media(max-width:520px){
 body{padding:12px}
 .brand{margin:15px 0 22px}
 .card{padding:19px;border-radius:18px}
 .answers{grid-template-columns:1fr}
 .answers button{min-height:62px}
 .pin{letter-spacing:6px}
 .actions{flex-direction:column}
 .actions button{width:100%;margin:3px 0}
 .question{padding:17px}
}

@media(prefers-reduced-motion:reduce){
 *,*:before,*:after{
  animation:none!important;
  transition:none!important;
  scroll-behavior:auto!important;
 }
}
</style>
</head>

<body>
<main>

<header class="brand">
<h1>⚡ BATALHA MATEMÁTICA</h1>
<p>ARENA DIGITAL • DESAFIE SEUS AMIGOS</p>
</header>

<section id="home" class="card">
<h2>🎮 Entrar na batalha</h2>

<label>Seu nome</label>
<input id="playerName" maxlength="18" placeholder="Digite seu nome">

<div class="actions">
<button id="createBtn">⚡ Criar sala</button>
</div>

<hr>

<label>PIN da sala</label>
<input id="pinInput" inputmode="numeric" maxlength="6" placeholder="Ex.: 482193">

<button class="alt" id="joinBtn">🚀 Entrar com PIN</button>

<p class="notice" id="homeMsg"></p>
</section>

<section id="lobby" class="card hidden">
<h2>🏆 Sala de espera</h2>

<p>Compartilhe este PIN com seus amigos:</p>
<div class="pin" id="roomPin"></div>

<p id="lobbyCount"></p>
<div id="lobbyPlayers"></div>

<div class="actions">
<button id="startBtn">🚀 Começar partida</button>
<button class="alt" id="leaveBtn">↩ Sair da sala</button>
</div>

<p class="notice" id="lobbyMsg">Aguardando o anfitrião iniciar...</p>
</section>

<section id="game" class="card hidden">

<div class="meta">
<span id="roundInfo">Pergunta 1</span>
<span>⏱ <b id="timer">20</b>s</span>
</div>

<div style="height:9px;background:#29425c;border-radius:9px;margin:12px 0 20px">
<div id="timeBar" style="height:100%;width:100%;background:var(--cyan);border-radius:9px"></div>
</div>

<div class="question" id="questionText"></div>

<div class="answers" id="answerButtons"></div>

<p class="notice" id="gameMsg"></p>

<h3>📊 Placar da batalha</h3>
<div id="gamePlayers"></div>

<button id="nextBtn" class="hidden">➡ Próxima pergunta</button>
</section>

<section id="result" class="card hidden">
<h2>🏅 Resultado final</h2>
<div id="finalRanking"></div>
<button onclick="location.reload()">🏠 Voltar ao início</button>
</section>

<footer>
⚡ BATALHA MATEMÁTICA • ARENA GAMER<br>
Protótipo educacional
</footer>

</main>

<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-auth-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-database-compat.js"></script>

<script>
const firebaseConfig={
 apiKey:"AIzaSyAakf_54XSCQijFp4bjDXiiFwV6PSZwJfQ",
 authDomain:"batalhamatematica-16322.firebaseapp.com",
 databaseURL:"https://batalhamatematica-16322-default-rtdb.firebaseio.com",
 projectId:"batalhamatematica-16322",
 storageBucket:"batalhamatematica-16322.firebasestorage.app",
 messagingSenderId:"48762205432",
 appId:"1:48762205432:web:141f27085374d67892b70d"
};

firebase.initializeApp(firebaseConfig);

const auth=firebase.auth(), db=firebase.database();
const $=id=>document.getElementById(id);

const questions=[
{q:"Qual é o limite de x + 2 quando x tende a 3?",a:["3","5","6","2"],c:1},
{q:"Qual é a derivada de f(x) = x²?",a:["x","2x","x²","2"],c:1},
{q:"Quanto vale lim (2x + 1), quando x → 2?",a:["3","4","5","6"],c:2},
{q:"Qual é a derivada de f(x) = 5x?",a:["5","x","5x","0"],c:0},
{q:"Qual é a derivada de uma constante?",a:["1","A própria constante","0","x"],c:2},
{q:"Quanto vale 3² + 1?",a:["7","9","10","12"],c:2},
{q:"A derivada de x³ é:",a:["3x²","x²","3x","x⁴"],c:0},
{q:"Qual é o limite de x² quando x → 4?",a:["8","12","16","4"],c:2},
{q:"A inclinação da reta y = 2x + 3 é:",a:["3","2","5","1"],c:1},
{q:"A derivada de f(x) = x é:",a:["0","x","1","2x"],c:2}
];

let uid=null,room=null,pin=null,isHost=false,unsub=null,localTimer=null,remaining=20,answered=false,roomData=null;

function show(id){
 ["home","lobby","game","result"].forEach(x=>$(x).classList.toggle("hidden",x!==id))
}

function msg(id,t,cls=""){
 $(id).textContent=t;
 $(id).className="notice "+cls
}

function cleanName(){
 return $("playerName").value.trim().slice(0,18)
}

function randomPin(){
 return String(Math.floor(100000+Math.random()*900000))
}

function shuffle(a){
 return [...a].sort(()=>Math.random()-.5)
}

async function ensureAuth(){
 if(!auth.currentUser)await auth.signInAnonymously();
 uid=auth.currentUser.uid
}

function roomRef(){
 return db.ref("salas/"+pin)
}

async function createRoom(){
 const name=cleanName();
 if(!name){msg("homeMsg","Digite seu nome primeiro.");return}

 try{
  await ensureAuth();
  let p=randomPin();
  let ref=db.ref("salas/"+p);

  await ref.set({
   host:uid,
   status:"lobby",
   createdAt:Date.now(),
   players:{[uid]:{name,score:0,streak:0}},
   deck:shuffle(questions).map((q)=>q),
   index:0,
   deadline:0
  });

  pin=p;
  isHost=true;
  enterRoom();

 }catch(e){
  msg("homeMsg","Não foi possível criar: "+e.message)
 }
}

async function joinRoom(){
 const name=cleanName(),p=$("pinInput").value.trim();

 if(!name){msg("homeMsg","Digite seu nome primeiro.");return}
 if(!/^\d{6}$/.test(p)){msg("homeMsg","Digite um PIN de 6 números.");return}

 try{
  await ensureAuth();
  pin=p;
  const ref=roomRef();
  let joined=false;

  await ref.child("players").transaction(players=>{
   players=players||{};

   if(players[uid]){
    joined=true;
    return players
   }

   if(Object.keys(players).length>=10)return;

   players[uid]={name,score:0,streak:0};
   joined=true;
   return players;
  });

  const snap=await ref.get();

  if(!snap.exists()){
   msg("homeMsg","Sala não encontrada.");
   return
  }

  if(!joined){
   msg("homeMsg","A sala já tem 10 jogadores.");
   return
  }

  isHost=snap.val().host===uid;
  enterRoom();

 }catch(e){
  msg("homeMsg","Erro ao entrar: "+e.message)
 }
}

function enterRoom(){
 show("lobby");
 $("roomPin").textContent=pin;
 subscribe();

 if(isHost)$("startBtn").classList.remove("hidden");
 else $("startBtn").classList.add("hidden")
}

function subscribe(){
 if(unsub)unsub();

 const ref=roomRef();

 const handler=s=>{
  if(!s.exists()){
   msg("lobbyMsg","A sala foi encerrada.");
   return
  }

  roomData=s.val();
  renderPlayers();

  if(roomData.status==="playing"&&$("game").classList.contains("hidden")){
   show("game");
   renderQuestion()
  }else if(roomData.status==="playing"){
   renderQuestion()
  }else if(roomData.status==="finished"){
   renderFinal()
  }
 };

 ref.on("value",handler);
 unsub=()=>ref.off("value",handler)
}

function renderPlayers(){
 const players=Object.entries(roomData.players||{}).sort((a,b)=>(b[1].score||0)-(a[1].score||0));

 $("lobbyCount").textContent=players.length+"/10 jogadores";

 $("lobbyPlayers").innerHTML=players.map(([id,p],i)=>
  `<div class="player"><span>${i+1}. ${esc(p.name)} ${id===roomData.host?"👑":""}</span><b>${p.score||0} pts</b></div>`
 ).join("");

 $("gamePlayers").innerHTML=players.map(([id,p],i)=>
  `<div class="player"><span>${i+1}. ${esc(p.name)}</span><b>${p.score||0} pts</b></div>`
 ).join("")
}

function esc(s){
 return String(s).replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]))
}

async function startGame(){
 const deck=shuffle(questions);
 await roomRef().update({
  status:"playing",
  deck,
  index:0,
  deadline:Date.now()+20000
 })
}

function renderQuestion(){
 if(!roomData||roomData.status!=="playing")return;

 const idx=roomData.index||0,q=(roomData.deck||questions)[idx];

 if(!q){
  if(isHost)roomRef().update({status:"finished"});
  return
 }

 $("roundInfo").textContent=`Pergunta ${idx+1} de ${roomData.deck.length}`;
 $("questionText").textContent=q.q;

 $("answerButtons").innerHTML=q.a.map((a,i)=>
  `<button data-i="${i}" ${roomData.players[uid]?.answers?.[idx]!==undefined?"disabled":""}>${esc(a)}</button>`
 ).join("");

 [...$("answerButtons").querySelectorAll("button")].forEach(b=>
  b.onclick=()=>answer(Number(b.dataset.i))
 );

 answered=roomData.players[uid]?.answers?.[idx]!==undefined;

 if(answered)
  msg("gameMsg","Resposta registrada! Aguarde a próxima pergunta.","good");
 else
  msg("gameMsg","Escolha uma alternativa.");

 startTimer(roomData.deadline||Date.now()+20000);
 renderPlayers();

 if(isHost)$("nextBtn").classList.remove("hidden");
 else $("nextBtn").classList.add("hidden")
}

function startTimer(deadline){
 clearInterval(localTimer);

 function tick(){
  remaining=Math.max(0,Math.ceil((deadline-Date.now())/1000));
  $("timer").textContent=remaining;
  $("timeBar").style.width=(remaining/20*100)+"%";

  if(remaining<=0){
   clearInterval(localTimer);
   if(isHost)advance()
  }
 }

 tick();
 localTimer=setInterval(tick,250)
}

async function answer(i){
 if(answered)return;

 answered=true;

 [...$("answerButtons").querySelectorAll("button")].forEach(b=>b.disabled=true);

 const idx=roomData.index,q=roomData.deck[idx],correct=i===q.c;

 const updates={};
 updates[`players/${uid}/answers/${idx}`]=i;

 if(correct){
  const p=roomData.players[uid]||{};
  const streak=(p.streak||0)+1;

  updates[`players/${uid}/score`]=(p.score||0)+10+(streak%3===0?5:0);
  updates[`players/${uid}/streak`]=streak;

 }else{
  updates[`players/${uid}/streak`]=0
 }

 try{
  await roomRef().update(updates);

  msg("gameMsg",
   correct?"Resposta correta! + pontos":"Resposta registrada. Boa sorte na próxima!",
   correct?"good":""
  );

 }catch(e){
  msg("gameMsg","Erro ao enviar resposta: "+e.message)
 }
}

async function advance(){
 if(!isHost)return;

 const next=(roomData.index||0)+1;

 if(next>=roomData.deck.length){
  await roomRef().update({status:"finished"});
  return
 }

 await roomRef().update({
  index:next,
  deadline:Date.now()+20000
 })
}

function renderFinal(){
 clearInterval(localTimer);
 show("result");

 const players=Object.values(roomData.players||{}).sort((a,b)=>(b.score||0)-(a.score||0));

 $("finalRanking").innerHTML=players.map((p,i)=>
  `<div class="player"><span>${["🥇","🥈","🥉"][i]||`${i+1}.`} ${esc(p.name)}</span><b>${p.score||0} pts</b></div>`
 ).join("")
}

async function leave(){
 clearInterval(localTimer);

 if(pin&&uid){
  try{
   await roomRef().child("players/"+uid).remove()
  }catch(e){}
 }

 if(unsub)unsub();
 location.reload()
}

$("createBtn").onclick=createRoom;
$("joinBtn").onclick=joinRoom;
$("startBtn").onclick=startGame;
$("nextBtn").onclick=advance;
$("leaveBtn").onclick=leave;

</script>
</body>
</html>
