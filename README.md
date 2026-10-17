
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BSIT 1-C OFFICIAL</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');

:root {
  --bg:#090710;
  --panel:#15111f;
  --border:#302541;
  --purple:#8b5cf6;
  --light:#c4b5fd;
  --text:#f5f3ff;
  --muted:#a39ab5;
}

*{box-sizing:border-box}
body{margin:0;font-family:Inter,Arial,sans-serif;background:var(--bg);color:var(--text)}
button,input{font:inherit}
button{cursor:pointer;transition:.2s}
button:hover{filter:brightness(1.15)}
.hidden{display:none!important}
.muted{color:var(--muted)}
.primary{background:linear-gradient(135deg,#a78bfa,#6d28d9);color:white;border:0;padding:12px 16px;border-radius:9px;font-weight:700}
.secondary{background:#21172f;color:white;border:1px solid #49345f;padding:11px 14px;border-radius:9px}
.full{width:100%;margin-top:18px}

.auth{
 min-height:100vh;display:grid;place-items:center;padding:20px;
 background:radial-gradient(ellipse at top,#321653,#090710 70%);
}
.auth-card{
 width:100%;max-width:420px;padding:30px;background:#15111fee;
 border:1px solid #493265;border-radius:22px;text-align:center;
 box-shadow:0 20px 80px #0008;
}
.logo,.mini-logo{
 display:grid;place-items:center;color:white;font-weight:800;
 background:linear-gradient(135deg,#c4b5fd,#6d28d9);
 box-shadow:0 0 25px #8b5cf655;
}
.logo{width:65px;height:65px;border-radius:20px;margin:auto;font-size:24px}
.eyebrow{font-size:10px;letter-spacing:2px;color:var(--light);margin-top:22px}
h1{letter-spacing:2px}
h1 span{color:var(--light)}
.tabs{display:flex;gap:5px;background:#0b0912;padding:5px;border-radius:10px;margin:25px 0}
.tabs button{flex:1;padding:11px;background:transparent;border:0;color:var(--muted);border-radius:8px}
.tabs button.active{background:#38224f;color:white}
form{text-align:left}
label{display:block;font-size:12px;margin:14px 0 7px;color:#ddd5ef}
input{
 width:100%;padding:12px;background:#0c0912;border:1px solid var(--border);
 border-radius:9px;color:white;outline:none;
}
input:focus{border-color:var(--purple)}
.footer{color:#766b89;font-size:10px;margin-top:28px;letter-spacing:1px}

.app{min-height:100vh}
.sidebar{
 width:245px;position:fixed;inset:0 auto 0 0;display:flex;flex-direction:column;
 padding:22px 14px;background:#0e0b16;border-right:1px solid var(--border);z-index:5;
}
.brand{display:flex;align-items:center;gap:12px;padding:0 7px 28px}
.mini-logo{width:42px;height:42px;border-radius:12px}
.brand b,.brand small{display:block}
.brand b{font-size:14px}
.brand small{font-size:9px;letter-spacing:1px;color:var(--muted);margin-top:5px}
.nav-title{color:#746984;font-size:10px;letter-spacing:2px;padding:0 10px}
.nav{
 text-align:left;padding:13px;border:0;border-radius:9px;margin:3px 0;
 color:#aaa0bd;background:transparent;font-size:12px;
}
.nav:hover,.nav.active{background:#281b3b;color:white}
.nav.active{box-shadow:inset 3px 0 var(--purple)}
.sidebar-bottom{margin-top:auto;padding:15px 5px;color:#8d83a0;font-size:10px}
.main{margin-left:245px;min-width:0}
.topbar{
 height:70px;display:flex;align-items:center;gap:15px;padding:0 28px;
 border-bottom:1px solid var(--border);background:#0c0913;
 position:sticky;top:0;z-index:3;
}
.crumb{font-size:12px;color:var(--muted)}
.crumb b{color:white}
.user{margin-left:auto;display:flex;gap:10px;align-items:center}
.user b,.user small{display:block}
.user b{font-size:11px}
.user small{font-size:10px;color:var(--muted);margin-top:4px}
.avatar{
 display:grid;place-items:center;width:36px;height:36px;border-radius:11px;
 background:linear-gradient(135deg,#a78bfa,#6d28d9);font-weight:800;
}
.content{padding:28px;max-width:1400px;margin:auto}
.page-heading{display:flex;align-items:center;justify-content:space-between;gap:12px;margin-bottom:24px}
.page-heading h2{font-size:25px;margin:0 0 8px}
.page-heading p{font-size:12px;line-height:1.7;color:var(--muted);margin:0}
.hero{
 background:linear-gradient(120deg,#30174a,#171022);border:1px solid #4a3065;
 border-radius:17px;padding:28px;margin-bottom:20px;
}
.hero h2{font-size:24px}
.hero p{color:#c7bbd9;font-size:12px;line-height:1.8;max-width:550px}
.hero .eyebrow{color:var(--light);letter-spacing:2px;font-size:10px}
.hero button{margin:8px 8px 0 0}
.stats{display:grid;grid-template-columns:repeat(4,1fr);gap:14px;margin-bottom:20px}
.stat,.panel,.person{
 background:var(--panel);border:1px solid var(--border);border-radius:14px;padding:18px;
}
.stat small{color:var(--muted);font-size:10px}
.stat strong{display:block;font-size:27px;margin:14px 0 8px}
.stat-title{font-size:11px;color:var(--muted)}
.columns{display:grid;grid-template-columns:1.2fr 1fr;gap:18px}
.panel{margin-bottom:18px}
.panel h3{font-size:14px;margin:0 0 17px}
.announcement,.task{border-bottom:1px solid var(--border);padding:14px 0}
.announcement:last-child,.task:last-child{border:0}
.announcement h4,.task b{font-size:12px;margin:0 0 8px;display:block}
.announcement p{color:var(--muted);font-size:11px;line-height:1.8;margin:0}
.task small{color:var(--muted);font-size:10px}
.tag{color:var(--light);background:#30203f;padding:5px 8px;font-size:9px;border-radius:5px;display:inline-block;margin-bottom:8px}
.people{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.person{text-align:center}
.person .avatar{margin:0 auto 12px;width:52px;height:52px}
.person h4{font-size:12px;margin:5px 0}
.person p{font-size:10px;color:var(--muted)}
.toast{
 position:fixed;right:20px;top:20px;z-index:10;padding:13px 18px;
 border:1px solid #69458e;background:#21152e;border-radius:10px;
 transform:translateY(-150%);transition:.3s;
}
.toast.show{transform:translateY(0)}
.menu-btn{display:none;background:#20172f;border:1px solid var(--border);color:white;padding:8px 11px;border-radius:8px}

@media(max-width:1050px){
 .stats{grid-template-columns:repeat(2,1fr)}
 .columns{grid-template-columns:1fr}
 .people{grid-template-columns:repeat(2,1fr)}
}
@media(max-width:720px){
 .sidebar{transform:translateX(-100%);transition:.25s;box-shadow:20px 0 40px #0008}
 .sidebar.open{transform:translateX(0)}
 .main{margin-left:0}
 .menu-btn{display:block}
 .topbar{padding:0 13px}
 .content{padding:20px 14px}
 .user>div:last-child{display:none}
 .page-heading h2{font-size:21px}
 .hero{padding:20px}
 .people{grid-template-columns:repeat(2,1fr)}
}
</style>
</head>

<body>
<section id="auth" class="auth">
 <div class="auth-card">
  <div class="logo">1C</div>
  <p class="eyebrow">COLLEGE OF COMPUTER STUDIES</p>
  <h1>BSIT <span>1-C</span></h1>
  <p class="muted">OFFICIAL CLASS PORTAL</p>

  <div class="tabs">
   <button id="loginTab" class="active" onclick="showForm('login')">Login</button>
   <button id="registerTab" onclick="showForm('register')">Register</button>
  </div>

  <form id="loginForm">
   <label>Email</label>
   <input id="loginEmail" type="email" placeholder="Enter email" required>
   <label>Password</label>
   <input id="loginPassword" type="password" placeholder="Enter password" required>
   <button class="primary full">LOG IN →</button>
   <p class="muted" style="font-size:10px">Demo admin: admin@bsit1c.local / Admin123!</p>
  </form>

  <form id="registerForm" class="hidden">
   <label>Full Name</label>
   <input id="regName" placeholder="Your full name" required>
   <label>Email</label>
   <input id="regEmail" type="email" placeholder="Your email" required>
   <label>Password</label>
   <input id="regPassword" type="password" minlength="6" placeholder="At least 6 characters" required>
   <label>Student ID</label>
   <input id="regID" placeholder="Student ID (optional)">
   <button class="primary full">CREATE ACCOUNT →</button>
  </form>
  <p class="footer">ONE TEAM • ONE GOAL • BSIT 1-C</p>
 </div>
</section>

<section id="dashboard" class="app hidden">
 <aside class="sidebar" id="sidebar">
  <div class="brand"><div class="mini-logo">1C</div><div><b>BSIT 1-C</b><small>OFFICIAL PORTAL</small></div></div>
  <p class="nav-title">MAIN MENU</p>
  <button class="nav active" onclick="navigate('home',this)">▦ Dashboard</button>
  <button class="nav" onclick="navigate('announcements',this)">◉ Announcements</button>
  <button class="nav" onclick="navigate('assignments',this)">▤ Assignments</button>
  <button class="nav" onclick="navigate('attendance',this)">✓ Attendance</button>
  <button class="nav" onclick="navigate('classmates',this)">♙ Classmates</button>
  <button class="nav" onclick="navigate('officers',this)">♛ Class Officers</button>
  <button class="nav" onclick="navigate('settings',this)">⚙ Settings</button>
  <button id="adminNav" class="nav hidden" onclick="navigate('admin',this)">◆ Admin Panel</button>
  <div class="sidebar-bottom">● Class portal active</div>
 </aside>

 <main class="main">
  <header class="topbar">
   <button class="menu-btn" onclick="toggleMenu()">☰</button>
   <div class="crumb">BSIT 1-C / <b id="pageTitle">Dashboard</b></div>
   <div class="user"><div class="avatar" id="avatar">S</div><div><b id="userName">Student</b><small id="userRole">Student</small></div></div>
  </header>
  <div id="content" class="content"></div>
 </main>
</section>

<div id="toast" class="toast"></div>

<script>
const $ = id => document.getElementById(id);

const defaultData = {
 users:[],
 announcements:[
  {title:"Welcome to BSIT 1-C Official!",body:"Welcome, classmates! Stay connected and check this portal for class updates and activities.",tag:"WELCOME",date:new Date().toLocaleDateString()},
  {title:"Keep Your Information Updated",body:"Please use correct information when creating your portal account.",tag:"REMINDER",date:new Date().toLocaleDateString()}
 ],
 assignments:[
  {title:"Introduction to Programming",subject:"Programming",due:"Check with your instructor"},
  {title:"Web Design Activity",subject:"Web Development",due:"Check with your instructor"}
 ]
};

let data;
try{
 data=JSON.parse(localStorage.getItem("bsit1c_data"))||defaultData;
}catch(e){data=defaultData}

let currentUser=null;

function save(){
 localStorage.setItem("bsit1c_data",JSON.stringify(data));
}

function escapeHTML(value){
 return String(value??"").replace(/[&<>"']/g,c=>({
  "&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"
 })[c]);
}

function showToast(message){
 const t=$("toast");
 t.textContent=message;
 t.classList.add("show");
 setTimeout(()=>t.classList.remove("show"),2500);
}

function showForm(type){
 $("loginForm").classList.toggle("hidden",type!=="login");
 $("registerForm").classList.toggle("hidden",type!=="register");
 $("loginTab").classList.toggle("active",type==="login");
 $("registerTab").classList.toggle("active",type==="register");
}

$("registerForm").addEventListener("submit",e=>{
 e.preventDefault();
 const name=$("regName").value.trim();
 const email=$("regEmail").value.trim().toLowerCase();
 const password=$("regPassword").value;
 const id=$("regID").value.trim();

 if(data.users.some(u=>u.email===email)){
  showToast("Email is already registered.");
  return;
 }

 const user={name,email,password,id,role:"student"};
 data.users.push(user);
 save();
 e.target.reset();
 login(user);
 showToast("Account created successfully!");
});

$("loginForm").addEventListener("submit",e=>{
 e.preventDefault();
 const email=$("loginEmail").value.trim().toLowerCase();
 const password=$("loginPassword").value;

 if(email==="admin@bsit1c.local"&&password==="Admin123!"){
  login({name:"BSIT 1-C Admin",email,role:"admin"});
  return;
 }

 const user=data.users.find(u=>u.email===email&&u.password===password);
 if(!user){showToast("Incorrect email or password.");return}
 login(user);
});

function login(user){
 currentUser=user;
 $("auth").classList.add("hidden");
 $("dashboard").classList.remove("hidden");
 $("userName").textContent=user.name;
 $("userRole").textContent=user.role==="admin"?"Administrator":"Student";
 $("avatar").textContent=user.name.split(/\s+/).map(n=>n[0]).join("").slice(0,2).toUpperCase();
 $("adminNav").classList.toggle("hidden",user.role!=="admin");
 navigate("home");
}

function logout(){
 currentUser=null;
 $("dashboard").classList.add("hidden");
 $("auth").classList.remove("hidden");
 $("loginForm").reset();
 showForm("login");
 showToast("Logged out successfully.");
}

function toggleMenu(){
 $("sidebar").classList.toggle("open");
}

function heading(title,description){
 return `<div class="page-heading"><div><h2>${title}</h2><p>${description}</p></div></div>`;
}

function navigate(page,button){
 $("sidebar").classList.remove("open");
 document.querySelectorAll(".nav").forEach(n=>n.classList.remove("active"));
 if(button)button.classList.add("active");

 const titles={
  home:"Dashboard",announcements:"Announcements",assignments:"Assignments",
  attendance:"Attendance",classmates:"Classmates",officers:"Class Officers",
  settings:"Settings",admin:"Admin Panel"
 };
 $("pageTitle").textContent=titles[page]||"Dashboard";

 if(page==="home")renderHome();
 if(page==="announcements")renderAnnouncements();
 if(page==="assignments")renderAssignments();
 if(page==="attendance")renderAttendance();
 if(page==="classmates")renderClassmates();
 if(page==="officers")renderOfficers();
 if(page==="settings")renderSettings();
 if(page==="admin"){
  if(currentUser.role!=="admin"){navigate("home");return}
  renderAdmin();
 }
}

function renderHome(){
 $("content").innerHTML=`
 ${heading("Dashboard","Welcome back, "+escapeHTML(currentUser.name)+". Here is your class overview.")}
 <section class="hero">
  <p class="eyebrow">YOUR CLASS • YOUR COMMUNITY</p>
  <h2>One Team. One Goal. <span style="color:#c4b5fd">BSIT 1-C.</span></h2>
  <p>Stay connected with classmates, keep track of class activities, and never miss an important update.</p>
  <button class="primary" onclick="navigate('announcements')">View Announcements →</button>
  <button class="secondary" onclick="navigate('assignments')">Check Assignments</button>
 </section>
 <div class="stats">
  <div class="stat"><div class="stat-title">Registered Students</div><strong>${data.users.length}</strong><small>Portal accounts</small></div>
  <div class="stat"><div class="stat-title">Announcements</div><strong>${data.announcements.length}</strong><small>Class updates</small></div>
  <div class="stat"><div class="stat-title">Assignments</div><strong>${data.assignments.length}</strong><small>Listed activities</small></div>
  <div class="stat"><div class="stat-title">Account Status</div><strong>${currentUser.role==="admin"?"Admin":"Active"}</strong><small>Current session</small></div>
 </div>
 <div class="columns">
  <section class="panel"><h3>Latest Announcements</h3>
   ${data.announcements.slice().reverse().slice(0,3).map(a=>`
    <article class="announcement"><span class="tag">${escapeHTML(a.tag)}</span><h4>${escapeHTML(a.title)}</h4><p>${escapeHTML(a.body)}</p></article>
   `).join("")}
  </section>
  <section class="panel"><h3>Upcoming Assignments</h3>
   ${data.assignments.map(a=>`<div class="task"><b>${escapeHTML(a.title)}</b><small>${escapeHTML(a.subject)} · ${escapeHTML(a.due)}</small></div>`).join("")}
  </section>
 </div>`;
}

function renderAnnouncements(){
 $("content").innerHTML=`
 ${heading("Announcements","Important class updates and reminders.")}
 ${currentUser.role==="admin"?'<button class="primary" onclick="addAnnouncement()">＋ New Announcement</button>':""}
 <section class="panel" style="margin-top:18px">
 ${data.announcements.slice().reverse().map((a,i)=>`
  <article class="announcement">
   <span class="tag">${escapeHTML(a.tag)} · ${escapeHTML(a.date)}</span>
   <h4>${escapeHTML(a.title)}</h4><p>${escapeHTML(a.body)}</p>
   ${currentUser.role==="admin"?`<button class="secondary" style="margin-top:10px" onclick="deleteAnnouncement(${data.announcements.length-1-i})">Delete</button>`:""}
  </article>
 `).join("")||"<p>No announcements yet.</p>"}
 </section>`;
}

function addAnnouncement(){
 const title=prompt("Announcement title:");
 if(!title||!title.trim())return;
 const body=prompt("Announcement message:");
 if(!body||!body.trim())return;
 data.announcements.push({
  title:title.trim(),body:body.trim(),tag:"UPDATE",
  date:new Date().toLocaleDateString()
 });
 save();renderAnnouncements();showToast("Announcement published.");
}

function deleteAnnouncement(index){
 if(currentUser.role!=="admin")return;
 if(!confirm("Delete this announcement?"))return;
 data.announcements.splice(index,1);
 save();renderAnnouncements();showToast("Announcement deleted.");
}

function renderAssignments(){
 $("content").innerHTML=`
 ${heading("Assignments","Review your class tasks and activities.")}
 <div class="people">
 ${data.assignments.map(a=>`<article class="person" style="text-align:left">
  <span class="tag">${escapeHTML(a.subject)}</span>
  <h4>${escapeHTML(a.title)}</h4><p>Deadline: ${escapeHTML(a.due)}</p>
 </article>`).join("")}
 </div>`;
}

function renderAttendance(){
 const key="bsit1c_att_"+currentUser.email+"_"+new Date().toISOString().slice(0,10);
 const status=localStorage.getItem(key)||"Not marked";
 $("content").innerHTML=`
 ${heading("Attendance","Demo attendance tracker for your browser.")}
 <section class="panel">
  <h3>Today's Attendance</h3>
  <p class="muted">Current status: <b>${escapeHTML(status)}</b></p>
  <button class="primary" onclick="markAttendance('Present')">Mark Present</button>
  <button class="secondary" onclick="markAttendance('Late')">Mark Late</button>
  <button class="secondary" onclick="markAttendance('Absent')">Mark Absent</button>
  <p class="muted">Demo only. This does not submit official school attendance.</p>
 </section>`;
}

function markAttendance(status){
 const key="bsit1c_att_"+currentUser.email+"_"+new Date().toISOString().slice(0,10);
 localStorage.setItem(key,status);
 renderAttendance();showToast("Attendance marked: "+status);
}

function renderClassmates(){
 $("content").innerHTML=`
 ${heading("Classmates","Registered members of this demo portal.")}
 <input id="searchPeople" placeholder="Search classmates..." style="margin-bottom:18px">
 <div id="peopleGrid" class="people"></div>`;
 drawPeople(data.users.filter(u=>u.role!=="admin"));
 $("searchPeople").addEventListener("input",e=>{
  const q=e.target.value.toLowerCase();
  drawPeople(data.users.filter(u=>u.role!=="admin"&&(u.name+" "+u.email).toLowerCase().includes(q)));
 });
}

function drawPeople(users){
 $("peopleGrid").innerHTML=users.map(u=>`
 <article class="person">
  <div class="avatar">${escapeHTML(u.name.split(/\s+/).map(n=>n[0]).join("").slice(0,2).toUpperCase())}</div>
  <h4>${escapeHTML(u.name)}</h4><p>${escapeHTML(u.id||"BSIT 1-C Student")}</p>
 </article>`).join("")||"<p class='muted'>No classmates found.</p>";
}

function renderOfficers(){
 const officers=[
 ["Joan Sarometman","President"],
 ["King Martin Rumbines","Vice President"],
 ["Lovely Rose Tibor","Secretary"],
 ["Dione Marco Bonggawil","Assistant Secretary"],
 ["Janelle Benito","Treasurer"],
 ["Jerich Sta Ana","Assistant Treasurer"],
 ["Jaja Nadong","Auditor"],
 ["Richie Lance Mapa","Business Manager"],
 ["Eljhunn Sua","Escort"],
 ["Jean Ashley Sumugat","Muse"],
 ["Jeric Dasmariñas","Assistant PIO"]
 ];
 $("content").innerHTML=`
 ${heading("Class Officers","The student leadership team of BSIT 1-C.")}
 <div class="people">${officers.map(o=>`
 <article class="person">
  <div class="avatar">${escapeHTML(o[0].split(/\s+/).map(n=>n[0]).join("").slice(0,2).toUpperCase())}</div>
  <h4>${escapeHTML(o[0])}</h4><p>${escapeHTML(o[1])}</p>
 </article>`).join("")}</div>`;
}

function renderSettings(){
 $("content").innerHTML=`
 ${heading("Settings","Manage your account and session.")}
 <section class="panel">
  <h3>Account Information</h3>
  <div class="task"><b>Full Name</b><small>${escapeHTML(currentUser.name)}</small></div>
  <div class="task"><b>Email Address</b><small>${escapeHTML(currentUser.email)}</small></div>
  <div class="task"><b>Account Type</b><small>${escapeHTML(currentUser.role)}</small></div>
  <br><button class="primary" onclick="logout()">Log Out</button>
  <p class="muted">Demo accounts are stored in this browser. Do not use real passwords or sensitive information.</p>
 </section>`;
}

function renderAdmin(){
 $("content").innerHTML=`
 ${heading("Admin Panel","Review demo accounts and manage announcements.")}
 <div class="stats">
  <div class="stat"><div class="stat-title">Accounts</div><strong>${data.users.length}</strong></div>
  <div class="stat"><div class="stat-title">Announcements</div><strong>${data.announcements.length}</strong></div>
  <div class="stat"><div class="stat-title">Assignments</div><strong>${data.assignments.length}</strong></div>
  <div class="stat"><div class="stat-title">Admin Status</div><strong>Active</strong></div>
 </div>
 <section class="panel"><h3>Registered Accounts</h3>
 ${data.users.map(u=>`<article class="announcement"><h4>${escapeHTML(u.name)}</h4><p>${escapeHTML(u.email)} · ${escapeHTML(u.role)}</p></article>`).join("")}
 </section>
 <button class="primary" onclick="addAnnouncement()">＋ Add Announcement</button>`;
}
</script>
</body>
</html>
