
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#111111">
<meta name="description" content="SUARA - Platform Partisipasi dan Pengawasan Kebijakan Publik">
<link rel="manifest" href="./manifest.json">
<title>SUARA | Ruang Demokrasi Digital</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700;800&family=Playfair+Display:wght@600;700&display=swap');

:root {
 --bg:#101011;
 --card:#1b1b1e;
 --red:#a91e2c;
 --red2:#d43b49;
 --gold:#b99a62;
 --white:#f5f1ed;
 --muted:#aaa3a0;
 --line:#343236;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
 margin:0;background:var(--bg);color:var(--white);
 font-family:'DM Sans',sans-serif;
}
a{text-decoration:none;color:inherit}
button,input,textarea,select{font:inherit}
header{
 position:sticky;top:0;z-index:10;
 background:#111112ed;backdrop-filter:blur(15px);
 border-bottom:1px solid var(--line);
}
nav{
 max-width:1150px;margin:auto;padding:16px 22px;
 display:flex;justify-content:space-between;align-items:center;
}
.logo{display:flex;align-items:center;gap:12px;font-weight:800;letter-spacing:3px}
.logo-icon{
 width:42px;height:42px;border:1px solid var(--gold);
 border-radius:50%;display:grid;place-items:center;
 color:var(--gold);font-size:23px;
}
.logo small{display:block;font-size:9px;color:var(--muted);letter-spacing:2px}
.links{display:flex;gap:23px;font-size:12px;color:#ccc}
.links a:hover{color:var(--gold)}
.btn{
 display:inline-block;padding:12px 19px;
 background:var(--red);border:1px solid var(--red);
 color:white;border-radius:3px;cursor:pointer;
 font-weight:700;font-size:11px;
}
.btn:hover{background:var(--red2)}
.btn.outline{background:transparent;border-color:#66504d}
.hero{
 background:radial-gradient(ellipse at 80% 20%,#761c293b,transparent 40%),
 linear-gradient(120deg,#191518,#101011);
 border-bottom:1px solid var(--line);
}
.container{max-width:1150px;margin:auto;padding:65px 22px}
.hero-grid{display:grid;grid-template-columns:1.3fr .7fr;gap:30px;align-items:center}
.eyebrow{color:var(--gold);font-size:10px;letter-spacing:3px;font-weight:700;text-transform:uppercase}
h1{font:700 clamp(42px,6vw,69px)/1.08 'Playfair Display';margin:20px 0}
h1 span{color:var(--red2)}
.hero p{color:#c0b9b4;line-height:1.8;max-width:620px;font-size:14px}
.actions{display:flex;gap:12px;flex-wrap:wrap;margin-top:27px}
.quote{border-left:2px solid var(--gold);padding-left:15px;margin-top:30px;color:#c5b6a0;font-size:12px;line-height:1.8}
.emblem{
 width:245px;height:245px;border:1px solid #b99a6280;
 border-radius:50%;margin:auto;display:grid;place-items:center;
 box-shadow:0 0 0 18px #b99a620b,0 0 0 40px #b99a6207;
}
.emblem div{
 width:175px;height:175px;border:1px solid #b99a6260;
 border-radius:50%;display:grid;place-items:center;
 color:var(--gold);font:75px Georgia;
}
.stats{display:grid;grid-template-columns:repeat(4,1fr);gap:12px}
.stat{background:var(--card);border:1px solid var(--line);border-top:2px solid var(--red);padding:20px}
.stat strong{display:block;font:30px 'Playfair Display'}
.stat small{color:var(--muted);font-size:10px}
h2{font:600 31px 'Playfair Display';margin:9px 0 12px}
.section-intro{color:var(--muted);font-size:13px;line-height:1.8;max-width:650px}
.section-head{margin-bottom:27px}
.searchbar{display:flex;gap:10px;margin:20px 0}
input,textarea,select{
 background:#151517;border:1px solid var(--line);
 color:white;padding:13px;border-radius:3px;width:100%;
 outline:none;
}
input:focus,textarea:focus,select:focus{border-color:var(--gold)}
.searchbar input{flex:1}
.cases{display:grid;grid-template-columns:repeat(2,1fr);gap:14px}
.case{
 background:var(--card);border:1px solid var(--line);
 padding:22px;border-radius:4px;
}
.case h3{font:600 20px 'Playfair Display';margin:17px 0 10px}
.case p{color:#bcb5b0;font-size:12px;line-height:1.8}
.meta{font-size:10px;color:var(--muted);margin:15px 0}
.tag{color:#e58d94;border:1px solid #70404a;padding:5px 8px;font-size:9px;letter-spacing:1px}
.tag.done{color:#8dd0a8;border-color:#426d53}
.steps{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
.step{padding:21px;background:var(--card);border:1px solid var(--line)}
.step b{font:26px 'Playfair Display';color:var(--gold)}
.step h3{font-size:14px}
.step p{font-size:11px;line-height:1.8;color:var(--muted)}
.tracking{
 display:grid;grid-template-columns:1fr 1fr;gap:25px;
 background:linear-gradient(120deg,#30171c,#191719);
 border:1px solid #583039;padding:28px;
}
.tracking p{font-size:12px;line-height:1.8;color:#c6bcb7}
.track-result{font-size:12px;line-height:1.8;margin-top:14px}
.formbox{background:var(--card);border:1px solid var(--line);padding:25px}
.formgrid{display:grid;grid-template-columns:1fr 1fr;gap:14px}
.field{display:flex;flex-direction:column;gap:7px}
.field label{font-size:11px;color:#ccc}
.full{grid-column:1/-1}
textarea{min-height:130px;resize:vertical}
.notice{font-size:10px;color:var(--muted);line-height:1.7}
footer{border-top:1px solid var(--line);padding:30px 22px;color:var(--muted);font-size:11px}
.footer-inner{max-width:1150px;margin:auto;display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap}
.modal{
 display:none;position:fixed;inset:0;background:#000c;
 z-index:20;align-items:center;justify-content:center;padding:20px;
}
.modal.show{display:flex}
.modal-content{
 background:var(--card);border:1px solid var(--gold);
 padding:28px;width:min(650px,100%);max-height:85vh;overflow:auto;
}
.close{float:right;background:none;border:0;color:white;font-size:24px;cursor:pointer}
.toast{
 position:fixed;bottom:20px;right:20px;z-index:30;
 background:#252225;border:1px solid var(--gold);
 padding:14px;display:none;font-size:12px;
}
@media(max-width:750px){
 .links{display:none}
 .hero-grid,.tracking{grid-template-columns:1fr}
 .emblem{display:none}
 .stats{grid-template-columns:repeat(2,1fr)}
 .cases{grid-template-columns:1fr}
 .steps{grid-template-columns:1fr 1fr}
}
@media(max-width:480px){
 .container{padding:42px 17px}
 .formgrid,.steps{grid-template-columns:1fr}
 .full{grid-column:auto}
 h2{font-size:27px}
}
</style>
</head>

<body>
<header>
<nav>
<a href="#" class="logo">
 <span class="logo-icon">§</span>
 <span>SUARA<small>SISTEM UTAMA ASPIRASI</small></span>
</a>
<div class="links">
<a href="#perkara">Perkara MK</a>
<a href="#mekanisme">Mekanisme</a>
<a href="#lacak">Lacak Aspirasi</a>
<a href="#aspirasi">Partisipasi</a>
</div>
<a href="#aspirasi" class="btn">BERPARTISIPASI ↗</a>
</nav>
</header>

<section class="hero">
<div class="container hero-grid">
<div>
<div class="eyebrow">Demokrasi · Transparansi · Akuntabilitas</div>
<h1>Suara publik,<br><span>jejak perubahan.</span></h1>
<p>
Demokrasi tidak berhenti pada hak untuk berbicara.
SUARA menghadirkan ruang bagi masyarakat untuk memahami
kebijakan, menyampaikan aspirasi, serta menelusuri
bagaimana masukan dipertimbangkan dalam proses legislasi.
</p>
<div class="actions">
<a href="#perkara" class="btn">PANTAU PERKARA</a>
<a href="#aspirasi" class="btn outline">KIRIM ASPIRASI</a>
</div>
<div class="quote">
“Salus populi suprema lex esto”<br>
Kesejahteraan rakyat hendaknya menjadi hukum tertinggi.
</div>
</div>
<div class="emblem"><div>§</div></div>
</div>
</section>

<main>
<section class="container" style="padding-top:30px;padding-bottom:30px">
<div class="stats">
<div class="stat"><strong>06</strong><small>Tahap partisipasi</small></div>
<div class="stat"><strong>1:1</strong><small>Jejak aspirasi dan pasal</small></div>
<div class="stat"><strong>24/7</strong><small>Akses platform</small></div>
<div class="stat"><strong>PWA</strong><small>Dukungan akses offline</small></div>
</div>
</section>

<section class="container" id="perkara">
<div class="section-head">
<div class="eyebrow">Pemantauan konstitusional</div>
<h2>Perkara yang menjadi perhatian publik</h2>
<p class="section-intro">
Pantau permohonan pengujian undang-undang di Mahkamah Konstitusi.
Dalil pemohon, status perkara, dan putusan harus dibedakan.
</p>
</div>
<div class="searchbar">
<input id="search" placeholder="Cari perkara, undang-undang, atau isu...">
<select id="filter">
<option value="">Semua status</option>
<option value="Berjalan">Dalam proses</option>
<option value="Dikabulkan">Dikabulkan</option>
</select>
</div>
<div class="cases" id="caseList"></div>
<p class="notice">
Data perkara merupakan sampel berdasarkan publikasi resmi MK per 4 November 2026.
Periksa perkembangan terbaru dan dokumen permohonan sebelum mengutip pasal atau dalil.
</p>
</section>

<section class="container" id="mekanisme">
<div class="section-head">
<div class="eyebrow">Sistem kerja SUARA</div>
<h2>Dari aspirasi menjadi jejak kebijakan</h2>
<p class="section-intro">
Enam tahapan untuk memastikan masukan masyarakat dapat diakses,
ditelusuri, dan dipertanggungjawabkan.
</p>
</div>
<div class="steps">
<div class="step"><b>01</b><h3>Policy Registration</h3><p>Pengunggahan rancangan, naskah akademik, dasar hukum, tujuan, dan jadwal pembahasan.</p></div>
<div class="step"><b>02</b><h3>Public Impact Mapping</h3><p>Pemetaan kelompok terdampak, termasuk pemuda, perempuan, masyarakat adat, dan kelompok rentan.</p></div>
<div class="step"><b>03</b><h3>Public Consultation</h3><p>Penyampaian aspirasi pada pasal tertentu disertai alasan, pengalaman, atau bukti.</p></div>
<div class="step"><b>04</b><h3>AI-Based Analysis</h3><p>AI membantu mengelompokkan dan merangkum aspirasi. AI tidak menentukan keputusan.</p></div>
<div class="step"><b>05</b><h3>Legislative Response</h3><p>Lembaga memberikan tanggapan diterima, diterima sebagian, atau tidak diterima disertai alasan.</p></div>
<div class="step"><b>06</b><h3>Public Tracking</h3><p>Masyarakat menelusuri status masukan, tanggapan, dan perubahan pasal.</p></div>
</div>
</section>

<section class="container" id="lacak">
<div class="tracking">
<div>
<div class="eyebrow">Aspirasi-to-Article Tracking</div>
<h2>Setiap aspirasi memiliki jejak.</h2>
<p>
Masukkan kode aspirasi untuk melihat status dan detail
masukan yang tersimpan pada browser ini.
</p>
</div>
<div>
<label class="notice">IDENTITAS JEJAK ASPIRASI</label>
<input id="trackId" placeholder="Contoh: SUA-2026-1234">
<br><br>
<button class="btn" onclick="trackAspirasi()">LACAK ASPIRASI →</button>
<div id="trackResult" class="track-result"></div>
</div>
</div>
</section>

<section class="container" id="aspirasi">
<div class="section-head">
<div class="eyebrow">Public Consultation</div>
<h2>Sampaikan aspirasi Anda</h2>
<p class="section-intro">
Pilih isu dan pasal yang ingin ditanggapi. Sertakan argumentasi
agar masukan lebih mudah ditelaah.
</p>
</div>
<div class="formbox">
<form id="aspForm" class="formgrid">
<div class="field">
<label>Nama atau nama samaran</label>
<input id="nama" required maxlength="80" placeholder="Nama Anda">
</div>
<div class="field">
<label>Kelompok / afiliasi</label>
<input id="kelompok" maxlength="100" placeholder="Mahasiswa, komunitas, warga...">
</div>
<div class="field">
<label>Perkara</label>
<select id="perkara" required>
<option value="">Pilih perkara</option>
<option>355/PUU-XXIV/2026 — UU Polri</option>
<option>411/PUU-XXIV/2026 — UU Advokat</option>
<option>410/PUU-XXIV/2026 — UU Pemilu dan Pilkada</option>
<option>409/PUU-XXIV/2026 — UU Penerbangan</option>
<option>371/PUU-XXIV/2026 — UU KUHAP</option>
</select>
</div>
<div class="field">
<label>Pasal / isu yang ditanggapi</label>
<input id="pasal" required maxlength="150" placeholder="Contoh: Pasal 8 ayat (1)">
</div>
<div class="field full">
<label>Isi aspirasi dan argumentasi</label>
<textarea id="isi" required maxlength="5000" placeholder="Tuliskan pendapat, alasan, dasar hukum, pengalaman, atau bukti pendukung..."></textarea>
</div>
<div class="field full">
<label style="display:flex;gap:8px;align-items:flex-start">
<input type="checkbox" id="consent" required style="width:auto">
Saya memahami bahwa ini merupakan prototype dan data disimpan di browser saya.
</label>
</div>
<div class="field full">
<button class="btn" type="submit">KIRIM ASPIRASI →</button>
<p class="notice">
Prototype ini belum terhubung ke server pemerintah atau MK.
Jangan masukkan NIK, alamat, atau informasi pribadi sensitif.
</p>
</div>
</form>
</div>
</section>
</main>

<footer>
<div class="footer-inner">
<div><b style="color:white;letter-spacing:3px">SUARA</b><br>
Sistem Utama Aspirasi, Representasi, dan Akuntabilitas</div>
<div>Platform partisipasi dan pengawasan kebijakan publik.<br>© 2026 SUARA</div>
</div>
</footer>

<div class="modal" id="modal">
<div class="modal-content">
<button class="close" onclick="closeModal()">×</button>
<div id="modalBody"></div>
</div>
</div>
<div class="toast" id="toast"></div>

<script>
// DATA PERKARA: sumber resmi Mahkamah Konstitusi
const cases = [
{
 id:"355/PUU-XXIV/2026",
 title:"Pengujian UU Kepolisian",
 law:"UU Nomor 2 Tahun 2002 jo. UU Nomor 5 Tahun 2026",
 article:"Pokok isu: kedudukan kelembagaan Polri",
 status:"Berjalan",
 date:"23 September 2026",
 summary:"Permohonan pengujian materiil UU Kepolisian. Pemohon mempersoalkan kedudukan Polri dalam struktur pemerintahan.",
 claim:"Isu yang dipublikasikan dalam proses persidangan berkaitan dengan permintaan agar Polri berada di bawah kementerian. Ini merupakan posisi pemohon, bukan kesimpulan Mahkamah.",
 source:"https://sippi.mkri.id/home/kegiatansidangdetail/5198"
},
{
 id:"411/PUU-XXIV/2026",
 title:"Pengujian UU Advokat",
 law:"UU Nomor 18 Tahun 2003 tentang Advokat",
 article:"Pasal yang diuji: periksa dokumen permohonan resmi",
 status:"Berjalan",
 date:"4 November 2026",
 summary:"Permohonan pengujian materiil UU Advokat telah diregistrasi di Mahkamah Konstitusi.",
 claim:"Ringkasan registrasi belum cukup untuk menyimpulkan pasal dan argumentasi konstitusional yang dipersoalkan.",
 source:"https://www.mkri.id/puu/pengujian-uud-dan-skln/2026/permohonan-diterima"
},
{
 id:"410/PUU-XXIV/2026",
 title:"Pengujian UU Pemilu dan UU Pilkada",
 law:"UU Nomor 7 Tahun 2017 dan UU Nomor 10 Tahun 2016",
 article:"Pasal yang diuji: periksa dokumen permohonan resmi",
 status:"Berjalan",
 date:"4 November 2026",
 summary:"Permohonan pengujian materiil UU Pemilu dan UU Pilkada telah diregistrasi di MK.",
 claim:"Pokok pasal dan petitum perlu diverifikasi melalui dokumen permohonan sebelum disimpulkan.",
 source:"https://www.mkri.id/puu/pengujian-uud-dan-skln/2026/permohonan-diterima"
},
{
 id:"409/PUU-XXIV/2026",
 title:"Pengujian UU Penerbangan",
 law:"UU Nomor 1 Tahun 2009 tentang Penerbangan",
 article:"Pasal yang diuji: periksa dokumen permohonan resmi",
 status:"Berjalan",
 date:"3 November 2026",
 summary:"Permohonan pengujian materiil UU Penerbangan telah diregistrasi di MK.",
 claim:"Pasal dan alasan pengujian perlu dibaca dari dokumen permohonan resmi.",
 source:"https://www.mkri.id/puu/pengujian-uud-dan-skln/2026/permohonan-diterima"
},
{
 id:"371/PUU-XXIV/2026",
 title:"Pertanggungjawaban Pidana Korporasi",
 law:"UU Nomor 20 Tahun 2025 tentang KUHAP",
 article:"Pasal 326 ayat (1), kata “dan”",
 status:"Dikabulkan",
 date:"29 Oktober 2026",
 summary:"MK mengabulkan permohonan dan menyatakan kata “dan” dalam Pasal 326 ayat (1) inkonstitusional bersyarat sepanjang tidak dimaknai “dan/atau”.",
 claim:"Ini merupakan perkara yang telah diputus, bukan perkara yang masih berjalan. Putusan mengubah pemaknaan norma terkait pertanggungjawaban tindak pidana korporasi.",
 source:"https://www.mkri.id/perkara/persidangan/putusan?search=2026"
}
];

function renderCases(){
 const query=document.getElementById("search").value.toLowerCase();
 const filter=document.getElementById("filter").value;
 const filtered=cases.filter(c=>{
  const text=[c.id,c.title,c.law,c.article,c.summary].join(" ").toLowerCase();
  return text.includes(query)&&(!filter||c.status===filter);
 });
 document.getElementById("caseList").innerHTML=filtered.map(c=>`
 <article class="case">
  <span class="tag ${c.status==="Dikabulkan"?"done":""}">${c.status}</span>
  <h3>${c.title}</h3>
  <p>${c.summary}</p>
  <div class="meta">
   <b>${c.id}</b><br>
   ${c.law}<br>${c.article}
  </div>
  <button class="btn outline" onclick="showDetail('${c.id}')">LIHAT DETAIL ↗</button>
 </article>`).join("")||"<p>Tidak ada perkara ditemukan.</p>";
}

document.getElementById("search").addEventListener("input",renderCases);
document.getElementById("filter").addEventListener("change",renderCases);

function showDetail(id){
 const c=cases.find(x=>x.id===id);
 document.getElementById("modalBody").innerHTML=`
 <div class="eyebrow">Detail perkara · ${c.status}</div>
 <h2>${c.title}</h2>
 <p><b>Nomor:</b> ${c.id}</p>
 <p><b>Undang-undang:</b> ${c.law}</p>
 <p><b>Pasal / isu:</b> ${c.article}</p>
 <p><b>Tanggal:</b> ${c.date}</p>
 <p>${c.summary}</p>
 <h3>Pokok isu dan posisi pemohon</h3>
 <p>${c.claim}</p>
 <p class="notice">Selalu periksa dokumen terbaru. Dalil pemohon tidak sama dengan pertimbangan atau putusan MK.</p>
 <a class="btn" href="${c.source}" target="_blank" rel="noopener">BUKA SUMBER MK ↗</a>`;
 document.getElementById("modal").classList.add("show");
}
function closeModal(){
 document.getElementById("modal").classList.remove("show");
}

// Penyimpanan demo lokal
function getData(){
 try{return JSON.parse(localStorage.getItem("suara_data")||"[]")}
 catch(e){return []}
}
function notify(message){
 const el=document.getElementById("toast");
 el.textContent=message;el.style.display="block";
 setTimeout(()=>el.style.display="none",3500);
}

document.getElementById("aspForm").addEventListener("submit",function(e){
 e.preventDefault();
 const id="SUA-"+new Date().getFullYear()+"-"+Math.random().toString(10).slice(2,7);
 const item={
  id,
  nama:document.getElementById("nama").value.trim(),
  kelompok:document.getElementById("kelompok").value.trim(),
  perkara:document.getElementById("perkara").value,
  pasal:document.getElementById("pasal").value.trim(),
  isi:document.getElementById("isi").value.trim(),
  status:"Tersimpan lokal",
  tanggal:new Date().toLocaleString("id-ID")
 };
 const data=getData();
 data.push(item);
 localStorage.setItem("suara_data",JSON.stringify(data));
 document.getElementById("trackId").value=id;
 document.getElementById("trackResult").innerHTML=
 `<b>Kode aspirasi Anda: ${id}</b><br>Simpan kode ini untuk melacak aspirasi.`;
 this.reset();
 notify("Aspirasi berhasil disimpan di browser!");
});

function trackAspirasi(){
 const id=document.getElementById("trackId").value.trim();
 const item=getData().find(x=>x.id===id);
 const result=document.getElementById("trackResult");
 if(!item){
  result.textContent="Kode tidak ditemukan. Gunakan browser dan perangkat yang sama saat membuat aspirasi.";
  return;
 }
 result.innerHTML=`
 <b style="color:#b99a62">${item.status}</b><br>
 Nama: ${escapeHTML(item.nama)}<br>
 Perkara: ${escapeHTML(item.perkara)}<br>
 Pasal: ${escapeHTML(item.pasal)}<br>
 Tanggal: ${escapeHTML(item.tanggal)}<br>
 Aspirasi: ${escapeHTML(item.isi)}<br>
 <span class="notice">Data ini hanya tersimpan di perangkat Anda.</span>`;
}
function escapeHTML(value){
 return String(value).replace(/[&<>"']/g,c=>({
 "&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#039;"
 })[c]);
}
renderCases();

// PWA
if("serviceWorker" in navigator && location.protocol.startsWith("http")){
 navigator.serviceWorker.register("./sw.js").catch(console.error);
}
</script>
</body>
</html>
# SUARA
WEB ASPIRASI DAN FUNGSI PENGAWASAN MASYARAKAT
