<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>NBA Player Database</title>

<style>
*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

body{
    background:#07090d;
    color:#f5f5f5;
    font-family:Arial,Helvetica,sans-serif;
}

header{
    height:72px;
    position:sticky;
    top:0;
    z-index:100;
    background:rgba(7,9,13,.95);
    border-bottom:1px solid #242936;
    backdrop-filter:blur(15px);
}

.nav{
    width:94%;
    max-width:1450px;
    height:100%;
    margin:auto;
    display:flex;
    align-items:center;
    justify-content:space-between;
}

.brand{
    display:flex;
    align-items:center;
    gap:14px;
}

.logo{
    width:42px;
    height:52px;
}

.brand-title{
    font-size:18px;
    font-weight:900;
    letter-spacing:.08em;
}

.brand-sub{
    font-size:10px;
    color:#777f8d;
    margin-top:4px;
    letter-spacing:.15em;
}

.live{
    display:flex;
    gap:8px;
    align-items:center;
    font-size:11px;
    color:#9ba3af;
}

.dot{
    width:7px;
    height:7px;
    border-radius:50%;
    background:#2ed158;
    box-shadow:0 0 10px #2ed158;
}

/* HERO */

.hero{
    width:94%;
    max-width:1450px;
    margin:auto;
    padding:70px 0 45px;
}

.hero-grid{
    display:grid;
    grid-template-columns:1.5fr 1fr;
    gap:40px;
    align-items:end;
}

.eyebrow{
    color:#e31837;
    font-size:12px;
    font-weight:900;
    letter-spacing:.2em;
    margin-bottom:15px;
}

h1{
    font-size:clamp(45px,6vw,82px);
    line-height:.9;
    letter-spacing:-.055em;
}

h1 span{
    color:#e31837;
}

.description{
    max-width:700px;
    color:#858e9c;
    line-height:1.7;
    margin-top:25px;
    font-size:14px;
}

.stats{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:10px;
}

.stat{
    padding:20px;
    border:1px solid #242936;
    background:#10131a;
    border-radius:14px;
}

.stat-number{
    font-size:28px;
    font-weight:900;
}

.stat-label{
    color:#777f8d;
    font-size:9px;
    margin-top:7px;
    letter-spacing:.12em;
}

/* CONTROLS */

.controls{
    width:94%;
    max-width:1450px;
    margin:0 auto 30px;

    display:grid;
    grid-template-columns:2fr 1fr 1fr 1fr;
    gap:10px;
}

.control{
    height:48px;
    background:#0e1117;
    color:#eee;
    border:1px solid #242936;
    border-radius:9px;
    padding:0 14px;
    outline:none;
}

.control:focus{
    border-color:#555d6b;
}

/* DATABASE BAR */

.database-bar{
    width:94%;
    max-width:1450px;
    margin:auto;
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:18px;
}

.database-title{
    font-size:18px;
    font-weight:900;
}

.database-status{
    font-size:11px;
    color:#777f8d;
}

/* GRID */

.grid{
    width:94%;
    max-width:1450px;
    margin:auto;

    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:16px;
}

.card{
    min-height:380px;
    background:#10131a;
    border:1px solid #242936;
    border-radius:17px;
    overflow:hidden;
    cursor:pointer;
    position:relative;
    transition:.25s;
}

.card:hover{
    transform:translateY(-5px);
    border-color:#444b58;
    box-shadow:0 20px 50px rgba(0,0,0,.4);
}

.card-image{
    height:270px;
    background:
        radial-gradient(
            circle at 50% 20%,
            rgba(227,24,55,.18),
            transparent 42%
        ),
        linear-gradient(
            180deg,
            #171b24,
            #0c0f14
        );

    display:flex;
    align-items:flex-end;
    justify-content:center;
}

.card-image img{
    width:100%;
    height:100%;
    object-fit:contain;
    object-position:center bottom;
}

.card-info{
    padding:16px;
}

.player-name{
    font-size:18px;
    font-weight:900;
}

.team{
    margin-top:7px;
    color:#aab2be;
    font-size:12px;
}

.badges{
    display:flex;
    flex-wrap:wrap;
    gap:6px;
    margin-top:13px;
}

.badge{
    padding:5px 8px;
    background:#0b0e13;
    border:1px solid #242936;
    border-radius:6px;
    color:#9099a7;
    font-size:9px;
}

.number{
    position:absolute;
    right:13px;
    top:11px;
    color:#717a88;
    font-size:11px;
    font-weight:bold;
}

/* PAGINATION */

.pagination{
    width:94%;
    max-width:1450px;
    margin:30px auto 70px;
    display:flex;
    justify-content:center;
    gap:7px;
}

.page{
    width:40px;
    height:40px;
    border:1px solid #242936;
    background:#10131a;
    color:white;
    border-radius:7px;
    cursor:pointer;
}

.page.active{
    background:#e31837;
    border-color:#e31837;
}

.page:disabled{
    opacity:.3;
}

/* MODAL */

.modal{
    display:none;
    position:fixed;
    inset:0;
    z-index:1000;

    background:rgba(0,0,0,.82);
    backdrop-filter:blur(10px);

    align-items:center;
    justify-content:center;

    padding:20px;
}

.modal.open{
    display:flex;
}

.modal-box{
    width:min(1050px,100%);
    max-height:90vh;
    overflow:auto;

    background:#0d1016;
    border:1px solid #303642;
    border-radius:20px;
}

.modal-top{
    display:grid;
    grid-template-columns:340px 1fr;
}

.modal-image{
    height:430px;

    display:flex;
    align-items:flex-end;
    justify-content:center;

    background:
        radial-gradient(
            circle at 50% 20%,
            rgba(227,24,55,.2),
            transparent 42%
        ),
        linear-gradient(
            180deg,
            #171b24,
            #0a0d12
        );
}

.modal-image img{
    width:100%;
    height:430px;
    object-fit:contain;
}

.modal-content{
    padding:38px;
}

.close{
    float:right;
    width:35px;
    height:35px;
    border:0;
    border-radius:50%;
    background:#191d25;
    color:white;
    font-size:20px;
    cursor:pointer;
}

.modal-team{
    color:#e31837;
    font-weight:900;
    font-size:11px;
    letter-spacing:.15em;
    margin-bottom:12px;
}

.modal-name{
    font-size:42px;
    font-weight:950;
    line-height:1;
    margin-bottom:28px;
}

.info-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:9px;
}

.info{
    padding:13px;
    border:1px solid #242936;
    background:#11151c;
    border-radius:9px;
}

.info-label{
    color:#6f7886;
    font-size:9px;
    text-transform:uppercase;
}

.info-value{
    margin-top:6px;
    font-size:13px;
    font-weight:800;
}

.modal-section{
    padding:25px 38px;
    border-top:1px solid #242936;
}

.section-title{
    font-size:11px;
    font-weight:900;
    letter-spacing:.14em;
    margin-bottom:14px;
}

.stat-grid{
    display:grid;
    grid-template-columns:repeat(6,1fr);
    gap:8px;
}

.mini{
    background:#11151c;
    border:1px solid #242936;
    padding:13px 5px;
    text-align:center;
    border-radius:8px;
}

.mini strong{
    display:block;
    font-size:17px;
}

.mini span{
    display:block;
    margin-top:5px;
    color:#707987;
    font-size:8px;
}

.pills{
    display:flex;
    flex-wrap:wrap;
    gap:7px;
}

.pill{
    padding:8px 10px;
    background:#171b23;
    border:1px solid #242936;
    border-radius:7px;
    font-size:10px;
    color:#b7bec9;
}

/* LOADING */

.loading{
    text-align:center;
    padding:80px 20px;
    color:#818a98;
}

.spinner{
    width:34px;
    height:34px;
    margin:0 auto 18px;

    border:3px solid #262c36;
    border-top-color:#e31837;
    border-radius:50%;

    animation:spin 1s linear infinite;
}

@keyframes spin{
    to{
        transform:rotate(360deg);
    }
}

/* ERROR */

.error{
    width:94%;
    max-width:900px;
    margin:50px auto;
    padding:25px;

    border:1px solid #54232d;
    background:#190c10;
    color:#ff9aaa;
    border-radius:12px;
    line-height:1.7;
}

/* RESPONSIVE */

@media(max-width:1100px){

    .grid{
        grid-template-columns:repeat(3,1fr);
    }

    .hero-grid{
        grid-template-columns:1fr;
    }

    .controls{
        grid-template-columns:1fr 1fr;
    }
}

@media(max-width:760px){

    .grid{
        grid-template-columns:repeat(2,1fr);
    }

    .modal-top{
        grid-template-columns:1fr;
    }

    .modal-image{
        height:300px;
    }

    .modal-image img{
        height:300px;
    }

    .stats{
        grid-template-columns:repeat(3,1fr);
    }

    .stat{
        padding:13px;
    }

    .stat-number{
        font-size:21px;
    }

    .stat-label{
        font-size:8px;
    }
}

@media(max-width:500px){

    .grid{
        grid-template-columns:1fr;
    }

    .controls{
        grid-template-columns:1fr;
    }

    .hero{
        padding-top:45px;
    }

    .modal-name{
        font-size:32px;
    }

    .stat-grid{
        grid-template-columns:repeat(3,1fr);
    }
}
</style>
</head>

<body>

<header>

<div class="nav">

<div class="brand">

<img
class="logo"
src="https://cdn.nba.com/logos/leagues/logo-nba.svg"
alt="NBA"
>

<div>

<div class="brand-title">
NBA DATABASE
</div>

<div class="brand-sub">
PLAYER INFORMATION SYSTEM
</div>

</div>

</div>

<div class="live">

<span class="dot"></span>

LIVE DATABASE

</div>

</div>

</header>


<main>

<section class="hero">

<div class="hero-grid">

<div>

<div class="eyebrow">
NATIONAL BASKETBALL ASSOCIATION
</div>

<h1>
NBA<br>
PLAYER <span>DATABASE</span>
</h1>

<p class="description">
Search and explore NBA players with roster,
physical profile, statistics, achievements and
career information.
</p>

</div>


<div class="stats">

<div class="stat">

<div
class="stat-number"
id="totalPlayers"
>
—
</div>

<div class="stat-label">
PLAYERS LOADED
</div>

</div>


<div class="stat">

<div class="stat-number">
30
</div>

<div class="stat-label">
NBA TEAMS
</div>

</div>


<div class="stat">

<div
class="stat-number"
id="visiblePlayers"
>
—
</div>

<div class="stat-label">
CURRENT VIEW
</div>

</div>

</div>

</div>

</section>


<section class="controls">

<input
id="search"
class="control"
placeholder="Search player..."
>

<select
id="team"
class="control"
>

<option value="">
All Teams
</option>

</select>


<select
id="position"
class="control"
>

<option value="">
All Positions
</option>

</select>


<select
id="sort"
class="control"
>

<option value="az">
Name A → Z
</option>

<option value="za">
Name Z → A
</option>

<option value="height">
Height
</option>

<option value="weight">
Weight
</option>

</select>

</section>


<section class="database-bar">

<div class="database-title">
Player Directory
</div>

<div
class="database-status"
id="status"
>
Connecting...
</div>

</section>


<div
id="loading"
class="loading"
>

<div class="spinner"></div>

Loading NBA player database...

</div>


<div
id="error"
class="error"
style="display:none"
></div>


<section
id="grid"
class="grid"
style="display:none"
></section>


<div
id="pagination"
class="pagination"
style="display:none"
></div>

</main>


<!-- MODAL -->

<div
id="modal"
class="modal"
>

<div class="modal-box">

<div class="modal-top">

<div class="modal-image">

<img
id="modalImg"
src=""
alt=""
>

</div>


<div class="modal-content">

<button
class="close"
onclick="closeModal()"
>
×
</button>


<div
id="modalTeam"
class="modal-team"
></div>


<div
id="modalName"
class="modal-name"
></div>


<div
id="infoGrid"
class="info-grid"
></div>

</div>

</div>


<div class="modal-section">

<div class="section-title">
STATISTICS
</div>

<div
id="statGrid"
class="stat-grid"
></div>

</div>


<div class="modal-section">

<div class="section-title">
AWARDS & ACHIEVEMENTS
</div>

<div
id="awards"
class="pills"
></div>

</div>


<div class="modal-section">

<div class="section-title">
INJURY HISTORY
</div>

<div
id="injuries"
class="pills"
></div>

</div>

</div>

</div>


<script>

/* =====================================================
   CONFIG
===================================================== */

const API =
"https://www.balldontlie.io/api/v1/players";

const NBA_IMAGE =
"https://cdn.nba.com/headshots/nba/latest/1040x760/";


const PER_PAGE = 24;


/* =====================================================
   VARIABLES
===================================================== */

let players = [];

let filtered = [];

let currentPage = 1;


/* =====================================================
   DOM
===================================================== */

const grid =
document.getElementById("grid");

const loading =
document.getElementById("loading");

const error =
document.getElementById("error");

const pagination =
document.getElementById("pagination");

const search =
document.getElementById("search");

const team =
document.getElementById("team");

const position =
document.getElementById("position");

const sort =
document.getElementById("sort");


/* =====================================================
   LOAD
===================================================== */

async function loadPlayers(){

try{

let all = [];

let page = 1;

let more = true;


/*
   Load multiple pages.
   The API may impose a limit.
*/

while(more && page <= 30){

const response =
await fetch(
`${API}?per_page=100&page=${page}`
);


if(!response.ok){

throw new Error(
"API request failed."
);

}


const data =
await response.json();


if(
!data.data ||
!data.data.length
){

break;

}


all =
all.concat(data.data);


more =
data.meta &&
data.meta.next_page
? true
: false;


page++;

}


/*
   Remove duplicate IDs
*/

const map =
new Map();


all.forEach(player => {

if(player.id){

map.set(
player.id,
player
);

}

});


players =
Array.from(
map.values()
)
.map(normalize);


filtered =
[...players];


document
.getElementById("totalPlayers")
.textContent =
players.length;


document
.getElementById("visiblePlayers")
.textContent =
players.length;


document
.getElementById("status")
.textContent =
`${players.length} PLAYERS LOADED`;


loading.style.display =
"none";


grid.style.display =
"grid";


pagination.style.display =
"flex";


populateFilters();

render();


}

catch(err){

loading.style.display =
"none";


error.style.display =
"block";


error.innerHTML = `

<strong>
DATABASE CONNECTION ERROR
</strong>

<br><br>

${escapeHTML(err.message)}

<br><br>

The external player API may be
temporarily unavailable or may have
changed its access policy.

`;

}

}


/* =====================================================
   NORMALIZE
===================================================== */

function normalize(p){

return {

id:p.id,

name:
`${p.first_name || ""}
 ${p.last_name || ""}`
.trim(),

team:
p.team
? p.team.full_name
: "Unknown",

teamAbbr:
p.team
? p.team.abbreviation
: "",

position:
p.position || "",

height:
p.height_feet
?
`${p.height_feet}'${p.height_inches || 0}"`
:
"",

weight:
p.weight_pounds
?
`${p.weight_pounds} lb`
:
"",

number:
p.jersey_number || "",

country:
p.country || "",

college:
p.college || "",

stats:{},

awards:[],

injuries:[]

};

}


/* =====================================================
   FILTERS
===================================================== */

function populateFilters(){

const teams =
[
...new Set(
players
.map(p => p.team)
.filter(Boolean)
)
]
.sort();


teams.forEach(t => {

team.innerHTML += `
<option value="${escapeHTML(t)}">
${escapeHTML(t)}
</option>
`;

});


const positions =
[
...new Set(
players
.map(p => p.position)
.filter(Boolean)
)
]
.sort();


positions.forEach(p => {

position.innerHTML += `
<option value="${escapeHTML(p)}">
${escapeHTML(p)}
</option>
`;

});

}


/* =====================================================
   APPLY
===================================================== */

function apply(){

const q =
search.value
.toLowerCase()
.trim();


const selectedTeam =
team.value;


const selectedPosition =
position.value;


filtered =
players.filter(p => {

const matchSearch =
!q ||
p.name
.toLowerCase()
.includes(q);


const matchTeam =
!selectedTeam ||
p.team === selectedTeam;


const matchPosition =
!selectedPosition ||
p.position === selectedPosition;


return (
matchSearch &&
matchTeam &&
matchPosition
);

});


sortPlayers();

currentPage = 1;

render();

}


/* =====================================================
   SORT
===================================================== */

function sortPlayers(){

const mode =
sort.value;


if(mode === "az"){

filtered.sort(
(a,b) =>
a.name.localeCompare(b.name)
);

}


if(mode === "za"){

filtered.sort(
(a,b) =>
b.name.localeCompare(a.name)
);

}


if(mode === "height"){

filtered.sort(
(a,b) =>
parseHeight(b.height)
-
parseHeight(a.height)
);

}


if(mode === "weight"){

filtered.sort(
(a,b) =>
parseWeight(b.weight)
-
parseWeight(a.weight)
);

}

}


/* =====================================================
   PARSE HEIGHT
===================================================== */

function parseHeight(v){

if(!v)
return 0;


const m =
v.match(/(\d+)'(\d+)/);


if(!m)
return 0;


return (
Number(m[1]) * 12 +
Number(m[2])
);

}


/* =====================================================
   PARSE WEIGHT
===================================================== */

function parseWeight(v){

if(!v)
return 0;


const m =
v.match(/\d+/);


return m
? Number(m[0])
: 0;

}


/* =====================================================
   RENDER
===================================================== */

function render(){

grid.innerHTML = "";


document
.getElementById("visiblePlayers")
.textContent =
filtered.length;


document
.getElementById("status")
.textContent =
`${filtered.length} MATCHING PLAYERS`;


const start =
(currentPage - 1)
* PER_PAGE;


const pagePlayers =
filtered.slice(
start,
start + PER_PAGE
);


pagePlayers.forEach(player => {

grid.appendChild(
createCard(player)
);

});


renderPagination();

}


/* =====================================================
   CARD
===================================================== */

function createCard(player){

const card =
document.createElement("article");


card.className =
"card";


card.onclick =
() => openModal(player);


const image =
NBA_IMAGE +
player.id +
".png";


card.innerHTML = `

<div class="number">
${escapeHTML(player.number)}
</div>

<div class="card-image">

<img
src="${image}"
alt="${escapeHTML(player.name)}"
loading="lazy"
onerror="this.style.display='none'"
>

</div>


<div class="card-info">

<div class="player-name">
${escapeHTML(player.name)}
</div>

<div class="team">
${escapeHTML(player.team)}
</div>


<div class="badges">

${
player.position
?
`
<span class="badge">
${escapeHTML(player.position)}
</span>
`
:""
}


${
player.height
?
`
<span class="badge">
${escapeHTML(player.height)}
</span>
`
:""
}


${
player.weight
?
`
<span class="badge">
${escapeHTML(player.weight)}
</span>
`
:""
}

</div>

</div>

`;


return card;

}


/* =====================================================
   PAGINATION
===================================================== */

function renderPagination(){

pagination.innerHTML = "";


const pages =
Math.ceil(
filtered.length /
PER_PAGE
);


if(pages <= 1)
return;


const previous =
document.createElement("button");


previous.className =
"page";


previous.textContent =
"‹";


previous.disabled =
currentPage === 1;


previous.onclick = () => {

currentPage--;

render();

window.scrollTo({
top:0,
behavior:"smooth"
});

};


pagination.appendChild(
previous
);


let start =
Math.max(
1,
currentPage - 2
);


let end =
Math.min(
pages,
currentPage + 2
);


for(
let i=start;
i<=end;
i++
){

const button =
document.createElement("button");


button.className =
"page";


if(i === currentPage){

button.classList.add(
"active"
);

}


button.textContent =
i;


button.onclick = () => {

currentPage = i;

render();

window.scrollTo({
top:0,
behavior:"smooth"
});

};


pagination.appendChild(
button
);

}


const next =
document.createElement("button");


next.className =
"page";


next.textContent =
"›";


next.disabled =
currentPage === pages;


next.onclick = () => {

currentPage++;

render();

window.scrollTo({
top:0,
behavior:"smooth"
});

};


pagination.appendChild(
next
);

}


/* =====================================================
   MODAL
===================================================== */

function openModal(player){

const modal =
document.getElementById(
"modal"
);


modal.classList.add(
"open"
);


document
.getElementById("modalImg")
.src =
NBA_IMAGE +
player.id +
".png";


document
.getElementById("modalName")
.textContent =
player.name;


document
.getElementById("modalTeam")
.textContent =
`${player.team} ${
player.number
?
"#"+player.number
:""
}`;


const info =
document.getElementById(
"infoGrid"
);


info.innerHTML = "";


addInfo(
"Position",
player.position
);


addInfo(
"Height",
player.height
);


addInfo(
"Weight",
player.weight
);


addInfo(
"Country",
player.country
);


addInfo(
"College",
player.college
);


function addInfo(
label,
value
){

info.innerHTML += `

<div class="info">

<div class="info-label">
${label}
</div>

<div class="info-value">
${escapeHTML(
value || "—"
)}
</div>

</div>

`;

}


renderStats(player);

renderAwards(player);

renderInjuries(player);

}


/* =====================================================
   STATS
===================================================== */

function renderStats(player){

const container =
document.getElementById(
"statGrid"
);


container.innerHTML = "";


const stats = [

["PPG","—"],
["RPG","—"],
["APG","—"],
["SPG","—"],
["BPG","—"],
["FG%","—"]

];


stats.forEach(
([label,value]) => {

container.innerHTML += `

<div class="mini">

<strong>
${value}
</strong>

<span>
${label}
</span>

</div>

`;

});

}


/* =====================================================
   AWARDS
===================================================== */

function renderAwards(player){

const container =
document.getElementById(
"awards"
);


container.innerHTML = "";


if(!player.awards.length){

container.innerHTML = `
<span class="pill">
No award data
</span>
`;

return;

}


player.awards.forEach(
award => {

container.innerHTML += `
<span class="pill">
${escapeHTML(award)}
</span>
`;

});

}


/* =====================================================
   INJURIES
===================================================== */

function renderInjuries(player){

const container =
document.getElementById(
"injuries"
);


container.innerHTML = "";


if(!player.injuries.length){

container.innerHTML = `
<span class="pill">
No injury data
</span>
`;

return;

}


player.injuries.forEach(
injury => {

container.innerHTML += `
<span class="pill">
${escapeHTML(injury)}
</span>
`;

});

}


/* =====================================================
   CLOSE
===================================================== */

function closeModal(){

document
.getElementById("modal")
.classList.remove(
"open"
);

}


document
.getElementById("modal")
.addEventListener(
"click",
e => {

if(
e.target.id === "modal"
){

closeModal();

}

});


document.addEventListener(
"keydown",
e => {

if(
e.key === "Escape"
){

closeModal();

}

});


/* =====================================================
   EVENTS
===================================================== */

search.addEventListener(
"input",
apply
);

team.addEventListener(
"change",
apply
);

position.addEventListener(
"change",
apply
);

sort.addEventListener(
"change",
apply
);


/* =====================================================
   ESCAPE
===================================================== */

function escapeHTML(value){

return String(value)
.replaceAll("&","&amp;")
.replaceAll("<","&lt;")
.replaceAll(">","&gt;")
.replaceAll('"',"&quot;")
.replaceAll("'","&#039;");

}


/* =====================================================
   START
===================================================== */

loadPlayers();

</script>

</body>
</html>
