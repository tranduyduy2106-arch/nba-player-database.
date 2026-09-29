<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NBA Player Database</title>

<style>
:root{
  --bg:#080a0f;
  --panel:#10131a;
  --panel2:#151922;
  --line:#262b36;
  --text:#f5f7fa;
  --muted:#8d95a3;
  --red:#e31837;
  --red2:#ff3555;
  --green:#37d67a;
  --yellow:#f4c542;
}

*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

html{
  scroll-behavior:smooth;
}

body{
  background:
    radial-gradient(circle at 80% -10%, rgba(227,24,55,.16), transparent 30%),
    var(--bg);
  color:var(--text);
  font-family:Arial,Helvetica,sans-serif;
  min-height:100vh;
}

button,
input,
select{
  font:inherit;
}

button{
  cursor:pointer;
}

/* NAV */

.navbar{
  position:sticky;
  top:0;
  z-index:100;
  height:68px;
  border-bottom:1px solid var(--line);
  background:rgba(8,10,15,.9);
  backdrop-filter:blur(16px);
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:0 5%;
}

.logo{
  display:flex;
  align-items:center;
  gap:12px;
  font-weight:900;
  letter-spacing:-.5px;
}

.logo-mark{
  width:34px;
  height:34px;
  border-radius:8px;
  background:var(--red);
  display:grid;
  place-items:center;
  font-size:15px;
}

.logo span{
  color:var(--muted);
  font-weight:500;
}

.nav-links{
  display:flex;
  gap:25px;
}

.nav-links a{
  color:var(--muted);
  text-decoration:none;
  font-size:14px;
}

.nav-links a:hover{
  color:white;
}

/* HERO */

.hero{
  padding:75px 5% 45px;
  max-width:1450px;
  margin:auto;
}

.kicker{
  color:var(--red2);
  text-transform:uppercase;
  font-size:12px;
  letter-spacing:2px;
  font-weight:800;
  margin-bottom:14px;
}

.hero h1{
  font-size:clamp(40px,6vw,78px);
  line-height:.95;
  letter-spacing:-4px;
  max-width:900px;
}

.hero p{
  color:var(--muted);
  max-width:700px;
  margin-top:22px;
  line-height:1.7;
  font-size:16px;
}

.hero-stats{
  display:flex;
  gap:14px;
  flex-wrap:wrap;
  margin-top:35px;
}

.hero-stat{
  border:1px solid var(--line);
  background:rgba(255,255,255,.025);
  border-radius:12px;
  padding:17px 22px;
  min-width:145px;
}

.hero-stat strong{
  display:block;
  font-size:25px;
}

.hero-stat span{
  display:block;
  color:var(--muted);
  font-size:12px;
  margin-top:5px;
}

/* CONTROLS */

.container{
  width:90%;
  max-width:1450px;
  margin:auto;
}

.controls{
  position:sticky;
  top:68px;
  z-index:50;
  padding:18px 0;
  background:rgba(8,10,15,.92);
  backdrop-filter:blur(15px);
}

.control-grid{
  display:grid;
  grid-template-columns:2fr 1fr 1fr 1fr;
  gap:12px;
}

.input,
.select{
  width:100%;
  border:1px solid var(--line);
  background:var(--panel);
  color:white;
  border-radius:10px;
  padding:13px 14px;
  outline:none;
}

.input:focus,
.select:focus{
  border-color:var(--red);
}

.results-bar{
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:24px 0 18px;
}

.results-bar strong{
  font-size:18px;
}

.results-bar span{
  color:var(--muted);
  font-size:13px;
}

/* PLAYER GRID */

.player-grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:16px;
  padding-bottom:80px;
}

.card{
  position:relative;
  overflow:hidden;
  border:1px solid var(--line);
  background:linear-gradient(145deg,var(--panel2),var(--panel));
  border-radius:16px;
  padding:20px;
  min-height:300px;
  transition:.22s ease;
  cursor:pointer;
}

.card:hover{
  transform:translateY(-5px);
  border-color:#414957;
  box-shadow:0 15px 45px rgba(0,0,0,.35);
}

.card-top{
  display:flex;
  justify-content:space-between;
  align-items:flex-start;
}

.team-badge{
  padding:6px 9px;
  border-radius:7px;
  background:rgba(227,24,55,.12);
  color:#ff5b72;
  font-size:11px;
  font-weight:800;
}

.number{
  color:#4d5563;
  font-size:22px;
  font-weight:900;
}

.avatar{
  width:92px;
  height:92px;
  margin:22px 0 15px;
  border-radius:50%;
  background:
    linear-gradient(145deg,#292f3b,#11141b);
  border:1px solid #363d49;
  display:grid;
  place-items:center;
  font-size:27px;
  font-weight:900;
}

.card h2{
  font-size:21px;
  letter-spacing:-.5px;
}

.position{
  color:var(--muted);
  font-size:13px;
  margin-top:6px;
}

.card-meta{
  display:flex;
  gap:8px;
  flex-wrap:wrap;
  margin-top:17px;
}

.tag{
  border:1px solid var(--line);
  border-radius:7px;
  padding:6px 8px;
  color:#c5cad2;
  font-size:11px;
}

.mini-stats{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  border-top:1px solid var(--line);
  margin-top:18px;
  padding-top:15px;
  gap:10px;
}

.mini-stat strong{
  display:block;
  font-size:16px;
}

.mini-stat span{
  color:var(--muted);
  font-size:10px;
  margin-top:3px;
}

/* EMPTY */

.empty{
  display:none;
  text-align:center;
  padding:70px 20px;
  color:var(--muted);
}

/* MODAL */

.modal{
  position:fixed;
  inset:0;
  z-index:200;
  display:none;
  align-items:center;
  justify-content:center;
  padding:20px;
  background:rgba(0,0,0,.78);
  backdrop-filter:blur(8px);
}

.modal.show{
  display:flex;
}

.modal-box{
  width:min(950px,100%);
  max-height:90vh;
  overflow:auto;
  border:1px solid #303642;
  border-radius:20px;
  background:#0d1016;
  box-shadow:0 30px 100px rgba(0,0,0,.65);
}

.modal-header{
  padding:28px;
  border-bottom:1px solid var(--line);
  display:flex;
  justify-content:space-between;
  gap:20px;
}

.close{
  width:36px;
  height:36px;
  border:1px solid var(--line);
  border-radius:8px;
  background:var(--panel);
  color:white;
  font-size:20px;
}

.profile{
  display:grid;
  grid-template-columns:240px 1fr;
  gap:30px;
  padding:30px;
}

.profile-avatar{
  height:240px;
  border-radius:18px;
  background:linear-gradient(145deg,#292f3b,#11141b);
  display:grid;
  place-items:center;
  font-size:65px;
  font-weight:900;
  border:1px solid #343b48;
}

.profile h2{
  font-size:38px;
  letter-spacing:-1.5px;
}

.profile-sub{
  color:var(--muted);
  margin-top:8px;
}

.data-grid{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:10px;
  margin-top:25px;
}

.data-box{
  background:var(--panel);
  border:1px solid var(--line);
  padding:14px;
  border-radius:10px;
}

.data-box span{
  display:block;
  color:var(--muted);
  font-size:11px;
  margin-bottom:7px;
}

.data-box strong{
  font-size:16px;
}

.section{
  padding:0 30px 30px;
}

.section h3{
  font-size:17px;
  margin-bottom:15px;
}

.stats-table{
  width:100%;
  border-collapse:collapse;
  overflow:hidden;
  border:1px solid var(--line);
  border-radius:10px;
}

.stats-table th,
.stats-table td{
  text-align:left;
  padding:13px;
  border-bottom:1px solid var(--line);
  font-size:13px;
}

.stats-table th{
  color:var(--muted);
  font-weight:600;
  background:var(--panel);
}

.awards{
  display:flex;
  flex-wrap:wrap;
  gap:8px;
}

.award{
  padding:8px 11px;
  border-radius:8px;
  background:rgba(244,197,66,.1);
  border:1px solid rgba(244,197,66,.2);
  color:#f4c542;
  font-size:12px;
}

.injury{
  border:1px solid var(--line);
  background:var(--panel);
  border-radius:10px;
  padding:14px;
  margin-bottom:9px;
  display:grid;
  grid-template-columns:100px 1fr auto;
  gap:15px;
  align-items:center;
}

.injury-date{
  color:var(--muted);
  font-size:12px;
}

.status{
  padding:6px 8px;
  border-radius:7px;
  font-size:11px;
  font-weight:700;
}

.status.out{
  color:#ff657d;
  background:rgba(227,24,55,.1);
}

.status.returned{
  color:var(--green);
  background:rgba(55,214,122,.1);
}

/* FOOTER */

footer{
  border-top:1px solid var(--line);
  padding:30px 5%;
  color:var(--muted);
  font-size:12px;
  display:flex;
  justify-content:space-between;
}

/* RESPONSIVE */

@media(max-width:1100px){
  .player-grid{
    grid-template-columns:repeat(3,1fr);
  }

  .control-grid{
    grid-template-columns:1fr 1fr;
  }
}

@media(max-width:760px){
  .nav-links{
    display:none;
  }

  .hero h1{
    letter-spacing:-2px;
  }

  .player-grid{
    grid-template-columns:1fr;
  }

  .control-grid{
    grid-template-columns:1fr;
  }

  .profile{
    grid-template-columns:1fr;
  }

  .profile-avatar{
    height:180px;
  }

  .data-grid{
    grid-template-columns:1fr 1fr;
  }

  .injury{
    grid-template-columns:1fr;
  }

  footer{
    flex-direction:column;
    gap:8px;
  }
}
</style>
</head>

<body>

<nav class="navbar">
  <div class="logo">
    <div class="logo-mark">NBA</div>
    PLAYER DATABASE
  </div>

  <div class="nav-links">
    <a href="#players">Players</a>
    <a href="#database">Database</a>
    <a href="#about">About</a>
  </div>
</nav>

<header class="hero">
  <div class="kicker">Basketball Data Project</div>

  <h1>NBA PLAYER<br>DATABASE</h1>

  <p>
    Cơ sở dữ liệu cầu thủ NBA với thông tin thể hình,
    đội bóng, thống kê, danh hiệu và lịch sử chấn thương.
  </p>

  <div class="hero-stats">
    <div class="hero-stat">
      <strong id="totalPlayers">0</strong>
      <span>Cầu thủ trong database</span>
    </div>

    <div class="hero-stat">
      <strong>30</strong>
      <span>NBA Teams</span>
    </div>

    <div class="hero-stat">
      <strong>2026</strong>
      <span>Database season</span>
    </div>
  </div>
</header>

<section class="controls" id="database">
  <div class="container">

    <div class="control-grid">

      <input
        id="search"
        class="input"
        type="text"
        placeholder="Tìm cầu thủ, đội bóng..."
      >

      <select id="team" class="select">
        <option value="">Tất cả đội</option>
      </select>

      <select id="position" class="select">
        <option value="">Tất cả vị trí</option>
        <option value="PG">PG</option>
        <option value="SG">SG</option>
        <option value="SF">SF</option>
        <option value="PF">PF</option>
        <option value="C">C</option>
      </select>

      <select id="sort" class="select">
        <option value="name">Tên A-Z</option>
        <option value="age">Tuổi</option>
        <option value="ppg">PPG</option>
        <option value="height">Chiều cao</option>
      </select>

    </div>

  </div>
</section>

<main class="container" id="players">

  <div class="results-bar">
    <strong>Player Directory</strong>
    <span id="resultCount"></span>
  </div>

  <div id="playerGrid" class="player-grid"></div>

  <div id="empty" class="empty">
    Không tìm thấy cầu thủ phù hợp.
  </div>

</main>

<footer id="about">
  <div>NBA PLAYER DATABASE</div>
  <div>Personal basketball data project · 2026</div>
</footer>


<!-- MODAL -->

<div class="modal" id="modal">

  <div class="modal-box">

    <div class="modal-header">
      <div>
        <div class="kicker">Player Profile</div>
        <div id="modalTeam"></div>
      </div>

      <button class="close" onclick="closeModal()">×</button>
    </div>

    <div class="profile">

      <div id="modalAvatar" class="profile-avatar"></div>

      <div>

        <h2 id="modalName"></h2>

        <div id="modalSub" class="profile-sub"></div>

        <div class="data-grid">

          <div class="data-box">
            <span>Chiều cao</span>
            <strong id="mHeight"></strong>
          </div>

          <div class="data-box">
            <span>Cân nặng</span>
            <strong id="mWeight"></strong>
          </div>

          <div class="data-box">
            <span>Tuổi</span>
            <strong id="mAge"></strong>
          </div>

          <div class="data-box">
            <span>Quốc tịch</span>
            <strong id="mNation"></strong>
          </div>

          <div class="data-box">
            <span>Draft</span>
            <strong id="mDraft"></strong>
          </div>

          <div class="data-box">
            <span>Năm vào NBA</span>
            <strong id="mNBA"></strong>
          </div>

        </div>

      </div>

    </div>

    <section class="section">

      <h3>Season Statistics</h3>

      <table class="stats-table">
        <thead>
          <tr>
            <th>PPG</th>
            <th>RPG</th>
            <th>APG</th>
            <th>SPG</th>
            <th>BPG</th>
            <th>FG%</th>
            <th>3P%</th>
            <th>FT%</th>
          </tr>
        </thead>

        <tbody>
          <tr>
            <td id="sPPG"></td>
            <td id="sRPG"></td>
            <td id="sAPG"></td>
            <td id="sSPG"></td>
            <td id="sBPG"></td>
            <td id="sFG"></td>
            <td id="s3P"></td>
            <td id="sFT"></td>
          </tr>
        </tbody>
      </table>

    </section>

    <section class="section">

      <h3>Career Achievements</h3>

      <div id="awards" class="awards"></div>

    </section>

    <section class="section">

      <h3>Injury History</h3>

      <div id="injuries"></div>

    </section>

  </div>
</div>


<script>

/* =========================================================
   PLAYER DATABASE
   =========================================================

   Đây là dữ liệu mẫu để chạy giao diện.
   Khi có nguồn dữ liệu chính thức, có thể thay object
   trong mảng PLAYERS bằng dữ liệu thật.
========================================================= */

const PLAYERS = [

{
 name:"Victor Wembanyama",
 team:"San Antonio Spurs",
 abbr:"SAS",
 number:1,
 position:"C",
 height:224,
 weight:106,
 age:22,
 nation:"France",
 draft:"2023 — Pick 1",
 nba:2023,

 stats:{
   ppg:26.2,
   rpg:10.1,
   apg:4.0,
   spg:1.8,
   bpg:3.8,
   fg:47.6,
   three:35.2,
   ft:83.0
 },

 awards:[
   "Rookie of the Year",
   "All-Rookie First Team",
   "Defensive honors"
 ],

 injuries:[
   {
     date:"2025",
     type:"Ankle",
     status:"returned"
   }
 ]
},

{
 name:"Bam Adebayo",
 team:"Miami Heat",
 abbr:"MIA",
 number:13,
 position:"C",
 height:206,
 weight:115,
 age:29,
 nation:"USA",
 draft:"2017 — Pick 14",
 nba:2017,

 stats:{
   ppg:20.1,
   rpg:9.8,
   apg:4.3,
   spg:1.0,
   bpg:0.8,
   fg:49.1,
   three:31.0,
   ft:79.8
 },

 awards:[
   "NBA All-Star",
   "All-Defensive Team",
   "Olympic Gold Medal"
 ],

 injuries:[
   {
     date:"2024",
     type:"Knee",
     status:"returned"
   }
 ]
},

{
 name:"Kevin Durant",
 team:"Houston Rockets",
 abbr:"HOU",
 number:7,
 position:"SF",
 height:208,
 weight:109,
 age:37,
 nation:"USA",
 draft:"2007 — Pick 2",
 nba:2007,

 stats:{
   ppg:26.0,
   rpg:6.4,
   apg:4.4,
   spg:0.9,
   bpg:1.1,
   fg:52.3,
   three:41.0,
   ft:88.5
 },

 awards:[
   "2× NBA Champion",
   "2× Finals MVP",
   "NBA MVP",
   "15× All-Star",
   "4× Scoring Champion",
   "Olympic Gold Medal"
 ],

 injuries:[
   {
     date:"2019",
     type:"Achilles",
     status:"returned"
   },
   {
     date:"2024",
     type:"Calf",
     status:"returned"
   }
 ]
},

{
 name:"Joel Embiid",
 team:"Philadelphia 76ers",
 abbr:"PHI",
 number:21,
 position:"C",
 height:213,
 weight:127,
 age:32,
 nation:"Cameroon",
 draft:"2014 — Pick 3",
 nba:2014,

 stats:{
   ppg:30.6,
   rpg:11.2,
   apg:4.2,
   spg:1.0,
   bpg:1.7,
   fg:49.9,
   three:33.8,
   ft:88.3
 },

 awards:[
   "NBA MVP",
   "NBA Scoring Champion",
   "7× All-Star",
   "All-NBA",
   "All-Defensive Team"
 ],

 injuries:[
   {
     date:"2024",
     type:"Knee",
     status:"returned"
   },
   {
     date:"2025",
     type:"Knee",
     status:"out"
   }
 ]
},

{
 name:"Giannis Antetokounmpo",
 team:"Milwaukee Bucks",
 abbr:"MIL",
 number:34,
 position:"PF",
 height:211,
 weight:110,
 age:31,
 nation:"Greece",
 draft:"2013 — Pick 15",
 nba:2013,

 stats:{
   ppg:30.4,
   rpg:11.9,
   apg:6.5,
   spg:1.2,
   bpg:1.5,
   fg:60.1,
   three:35.0,
   ft:70.5
 },

 awards:[
   "2× NBA MVP",
   "NBA Champion",
   "Finals MVP",
   "8× All-Star",
   "Defensive Player of the Year",
   "Most Improved Player"
 ],

 injuries:[
   {
     date:"2024",
     type:"Calf",
     status:"returned"
   }
 ]
},

{
 name:"Stephen Curry",
 team:"Golden State Warriors",
 abbr:"GSW",
 number:30,
 position:"PG",
 height:188,
 weight:84,
 age:38,
 nation:"USA",
 draft:"2009 — Pick 7",
 nba:2009,

 stats:{
   ppg:24.5,
   rpg:4.4,
   apg:6.1,
   spg:1.1,
   bpg:0.2,
   fg:43.8,
   three:39.7,
   ft:92.0
 },

 awards:[
   "4× NBA Champion",
   "2× NBA MVP",
   "Finals MVP",
   "12× All-Star",
   "2× Scoring Champion",
   "3× Three-Point Champion"
 ],

 injuries:[
   {
     date:"2024",
     type:"Ankle",
     status:"returned"
   }
 ]
},

{
 name:"LeBron James",
 team:"Los Angeles Lakers",
 abbr:"LAL",
 number:23,
 position:"SF",
 height:206,
 weight:113,
 age:41,
 nation:"USA",
 draft:"2003 — Pick 1",
 nba:2003,

 stats:{
   ppg:24.4,
   rpg:7.8,
   apg:8.2,
   spg:0.9,
   bpg:0.6,
   fg:50.5,
   three:37.6,
   ft:73.5
 },

 awards:[
   "4× NBA Champion",
   "4× NBA MVP",
   "4× Finals MVP",
   "21× All-Star",
   "All-Time Scoring Leader",
   "Olympic Gold Medal"
 ],

 injuries:[
   {
     date:"2023",
     type:"Foot",
     status:"returned"
   }
 ]
},

{
 name:"Tyrese Haliburton",
 team:"Indiana Pacers",
 abbr:"IND",
 number:0,
 position:"PG",
 height:196,
 weight:84,
 age:26,
 nation:"USA",
 draft:"2020 — Pick 12",
 nba:2020,

 stats:{
   ppg:18.7,
   rpg:3.5,
   apg:9.2,
   spg:1.4,
   bpg:0.5,
   fg:47.2,
   three:39.5,
   ft:85.9
 },

 awards:[
   "2× NBA All-Star",
   "All-NBA",
   "All-Rookie Team"
 ],

 injuries:[
   {
     date:"2025",
     type:"Achilles",
     status:"out"
   }
 ]
},

{
 name:"Jimmy Butler III",
 team:"Golden State Warriors",
 abbr:"GSW",
 number:10,
 position:"SF",
 height:201,
 weight:104,
 age:36,
 nation:"USA",
 draft:"2011 — Pick 30",
 nba:2011,

 stats:{
   ppg:17.3,
   rpg:5.6,
   apg:5.9,
   spg:1.3,
   bpg:0.4,
   fg:50.0,
   three:35.4,
   ft:85.0
 },

 awards:[
   "6× NBA All-Star",
   "5× All-Defensive Team",
   "Most Improved Player"
 ],

 injuries:[
   {
     date:"2024",
     type:"Knee",
     status:"returned"
   }
 ]
}

];


/* =========================================================
   DOM
========================================================= */

const grid = document.getElementById("playerGrid");
const search = document.getElementById("search");
const teamFilter = document.getElementById("team");
const positionFilter = document.getElementById("position");
const sortFilter = document.getElementById("sort");
const empty = document.getElementById("empty");
const resultCount = document.getElementById("resultCount");
const totalPlayers = document.getElementById("totalPlayers");


/* =========================================================
   TEAM FILTER
========================================================= */

const teams = [...new Set(PLAYERS.map(p => p.team))].sort();

teams.forEach(team => {

  const option = document.createElement("option");

  option.value = team;
  option.textContent = team;

  teamFilter.appendChild(option);

});


/* =========================================================
   HELPERS
========================================================= */

function initials(name){

  return name
    .split(" ")
    .filter(Boolean)
    .slice(0,2)
    .map(x => x[0])
    .join("")
    .toUpperCase();

}


function renderPlayers(){

  let list = [...PLAYERS];

  const q = search.value.toLowerCase().trim();
  const team = teamFilter.value;
  const position = positionFilter.value;
  const sort = sortFilter.value;


  if(q){

    list = list.filter(p =>
      p.name.toLowerCase().includes(q) ||
      p.team.toLowerCase().includes(q) ||
      p.abbr.toLowerCase().includes(q)
    );

  }


  if(team){
    list = list.filter(p => p.team === team);
  }


  if(position){
    list = list.filter(p => p.position === position);
  }


  if(sort === "name"){
    list.sort((a,b) => a.name.localeCompare(b.name));
  }

  if(sort === "age"){
    list.sort((a,b) => b.age - a.age);
  }

  if(sort === "ppg"){
    list.sort((a,b) => b.stats.ppg - a.stats.ppg);
  }

  if(sort === "height"){
    list.sort((a,b) => b.height - a.height);
  }


  grid.innerHTML = "";

  resultCount.textContent =
    `${list.length} cầu thủ`;

  empty.style.display =
    list.length ? "none" : "block";


  list.forEach(player => {

    const card = document.createElement("article");

    card.className = "card";

    card.onclick = () => openModal(player);

    card.innerHTML = `

      <div class="card-top">

        <div class="team-badge">
          ${player.abbr}
        </div>

        <div class="number">
          #${player.number}
        </div>

      </div>

      <div class="avatar">
        ${initials(player.name)}
      </div>

      <h2>${player.name}</h2>

      <div class="position">
        ${player.position} · ${player.team}
      </div>

      <div class="card-meta">

        <div class="tag">
          ${player.height} cm
        </div>

        <div class="tag">
          ${player.weight} kg
        </div>

        <div class="tag">
          ${player.age} tuổi
        </div>

      </div>

      <div class="mini-stats">

        <div class="mini-stat">
          <strong>${player.stats.ppg}</strong>
          <span>PPG</span>
        </div>

        <div class="mini-stat">
          <strong>${player.stats.rpg}</strong>
          <span>RPG</span>
        </div>

        <div class="mini-stat">
          <strong>${player.stats.apg}</strong>
          <span>APG</span>
        </div>

      </div>
    `;

    grid.appendChild(card);

  });

}


totalPlayers.textContent = PLAYERS.length;

renderPlayers();


/* =========================================================
   EVENTS
========================================================= */

search.addEventListener("input", renderPlayers);
teamFilter.addEventListener("change", renderPlayers);
positionFilter.addEventListener("change", renderPlayers);
sortFilter.addEventListener("change", renderPlayers);


/* =========================================================
   MODAL
========================================================= */

function openModal(player){

  document.getElementById("modal").classList.add("show");

  document.getElementById("modalAvatar").textContent =
    initials(player.name);

  document.getElementById("modalName").textContent =
    player.name;

  document.getElementById("modalSub").textContent =
    `${player.position} · #${player.number} · ${player.team}`;

  document.getElementById("modalTeam").textContent =
    player.team;


  document.getElementById("mHeight").textContent =
    `${player.height} cm`;

  document.getElementById("mWeight").textContent =
    `${player.weight} kg`;

  document.getElementById("mAge").textContent =
    player.age;

  document.getElementById("mNation").textContent =
    player.nation;

  document.getElementById("mDraft").textContent =
    player.draft;

  document.getElementById("mNBA").textContent =
    player.nba;


  document.getElementById("sPPG").textContent =
    player.stats.ppg;

  document.getElementById("sRPG").textContent =
    player.stats.rpg;

  document.getElementById("sAPG").textContent =
    player.stats.apg;

  document.getElementById("sSPG").textContent =
    player.stats.spg;

  document.getElementById("sBPG").textContent =
    player.stats.bpg;

  document.getElementById("sFG").textContent =
    player.stats.fg + "%";

  document.getElementById("s3P").textContent =
    player.stats.three + "%";

  document.getElementById("sFT").textContent =
    player.stats.ft + "%";


  const awards =
    document.getElementById("awards");

  awards.innerHTML = "";

  player.awards.forEach(a => {

    const el = document.createElement("div");

    el.className = "award";

    el.textContent = a;

    awards.appendChild(el);

  });


  const injuries =
    document.getElementById("injuries");

  injuries.innerHTML = "";

  if(!player.injuries.length){

    injuries.innerHTML =
      `<div class="data-box">Không có dữ liệu.</div>`;

  }else{

    player.injuries.forEach(i => {

      const row = document.createElement("div");

      row.className = "injury";

      row.innerHTML = `

        <div class="injury-date">
          ${i.date}
        </div>

        <div>
          <strong>${i.type}</strong>
        </div>

        <div class="status ${i.status}">
          ${
            i.status === "out"
              ? "OUT"
              : "RETURNED"
          }
        </div>

      `;

      injuries.appendChild(row);

    });

  }

}


function closeModal(){

  document
    .getElementById("modal")
    .classList.remove("show");

}


document.getElementById("modal")
  .addEventListener("click", function(e){

    if(e.target === this){
      closeModal();
    }

  });


document.addEventListener("keydown", function(e){

  if(e.key === "Escape"){
    closeModal();
  }

});

</script>

</body>
</html>
