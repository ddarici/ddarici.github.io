---
layout: archive
title: "Lab Members"
permalink: /team/
author_profile: true
---
{% include base_path %}

<style>
.lab-intro {
  font-size: 15px;
  color: #555;
  line-height: 1.7;
  margin-bottom: 2rem;
  max-width: 720px;
}

.lab-layout {
  display: flex;
  gap: 0;
  align-items: flex-start;
  min-height: 320px;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 28px;
  margin: 20px 0 40px 0;
  transition: width 0.4s cubic-bezier(.4,0,.2,1);
  width: 100%;
}

.lab-layout.panel-open .team-grid {
  width: 42%;
  grid-template-columns: repeat(2, 1fr);
  gap: 16px;
}

.member-card {
  text-align: center;
  padding: 14px 10px;
  border: 0.5px solid #e0e0e0;
  border-radius: 12px;
  cursor: pointer;
  transition: border-color 0.25s ease, background 0.25s ease, box-shadow 0.25s ease;
  pointer-events: auto;
}

.member-card:hover {
  border-color: #1a6db5;
  background: #f8fbff;
  box-shadow: 0 2px 12px rgba(26,109,181,0.07);
}

.member-card.active {
  border-color: #1a6db5;
  background: #f4f8fd;
}

.member-photo {
  width: 130px;
  height: 130px;
  margin: 0 auto 14px;
  border-radius: 50%;
  object-fit: cover;
  display: block;
  filter: grayscale(100%);
  transition: filter 0.5s ease, transform 0.3s ease, border-color 0.3s ease;
  border: 3px solid #eee;
  pointer-events: none;
}

.member-card:hover .member-photo,
.member-card.active .member-photo {
  filter: grayscale(0%);
  transform: scale(1.04);
  border-color: #1a6db5;
}

.member-name {
  font-weight: 600;
  font-size: 1em;
  display: block;
  margin-top: 8px;
  color: #1a1a1a;
  pointer-events: none;
}

.member-role, .member-title {
  pointer-events: none;
  display: block;
}

.member-role { color: #666; font-size: 0.88em; margin-top: 3px; }
.member-title { color: #999; font-size: 0.82em; margin-top: 2px; }

/* Side panel */
.side-panel {
  width: 0;
  opacity: 0;
  overflow: hidden;
  transition: width 0.4s cubic-bezier(.4,0,.2,1), opacity 0.35s ease;
  flex-shrink: 0;
}

.lab-layout.panel-open .side-panel {
  width: calc(58% - 20px);
  opacity: 1;
  margin-left: 20px;
}

.panel-inner {
  background: #fff;
  border: 0.5px solid #dde5ef;
  border-radius: 12px;
  padding: 22px;
  min-width: 240px;
  max-height: 80vh;
  overflow-y: auto;
}

.panel-header {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  margin-bottom: 16px;
  padding-bottom: 14px;
  border-bottom: 0.5px solid #e8e8e8;
}

.panel-photo {
  width: 64px;
  height: 64px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid #1a6db5;
  flex-shrink: 0;
  margin-right: 14px;
}

.close-btn {
  background: none;
  border: none;
  cursor: pointer;
  color: #aaa;
  font-size: 18px;
  padding: 5px;
  line-height: 1;
}

.cv-row { margin-bottom: 13px; }
.cv-label { font-size: 10px; text-transform: uppercase; letter-spacing: 0.09em; color: #aaa; margin-bottom: 3px; }
.cv-value { font-size: 13px; color: #444; line-height: 1.6; }
.cv-tag { display: inline-block; background: #f0f4fa; border: 0.5px solid #d0dcea; border-radius: 4px; padding: 2px 8px; font-size: 11px; color: #4a6fa5; margin: 2px 2px 0 0; }

.accordion-btn {
  width: 100%;
  background: #f7f9fc;
  border: 0.5px solid #dde5ef;
  border-radius: 6px;
  padding: 7px 11px;
  font-size: 10px;
  text-transform: uppercase;
  color: #4a6fa5;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  margin-bottom: 6px;
  font-family: inherit;
}

.accordion-content { display: none; margin-bottom: 10px; }
.accordion-content.open { display: block; }

.pub-list, .award-list { list-style: none; padding: 0; margin: 0; }
.pub-list li, .award-list li { font-size: 11.5px; color: #444; padding: 5px 0; border-bottom: 0.5px solid #f0f0f0; }
.award-year { font-weight: 600; color: #1a6db5; margin-right: 8px; }

.alumni-section { margin-top: 2rem; padding-top: 1.2rem; border-top: 1px solid #eee; }
.alumni-row { display: flex; justify-content: space-between; padding: 8px 0; border-bottom: 0.5px solid #f0f0f0; font-size: 13.5px; }
</style>

<p class="lab-intro">The Darici Lab is a multidisciplinary research group focused on visual expertise in medical education through eye-tracking methodology.</p>

<div class="lab-layout" id="lab-layout">
  <div class="team-grid" id="team-grid">
    <div class="member-card" id="card-0">
      <img src="images/darici.jpg" class="member-photo" alt="Dogus Darici">
      <span class="member-name">Dogus Darici</span>
      <span class="member-role">Principal Investigator</span>
      <span class="member-title">Univ.-Prof. Dr.</span>
    </div>
    <div class="member-card" id="card-1">
      <img src="images/bellstedt.jpg" class="member-photo" alt="Michelle Bellstedt">
      <span class="member-name">Michelle Bellstedt</span>
      <span class="member-role">Master student</span>
      <span class="member-title">B. Sc.</span>
    </div>
    <div class="member-card" id="card-2">
      <img src="images/bio-photo-2.jpg" class="member-photo" alt="Anastasia Samoukina">
      <span class="member-name">Anastasia Samoukina</span>
      <span class="member-role">Doctoral Student</span>
      <span class="member-title">M. Sc.</span>
    </div>
    <div class="member-card" id="card-3">
      <img src="images/bio-photo-2.jpg" class="member-photo" alt="René Bieber">
      <span class="member-name">René Bieber</span>
      <span class="member-role">Technician</span>
      <span class="member-title"></span>
    </div>
  </div>

  <div class="side-panel" id="side-panel">
    <div class="panel-inner" id="panel-inner"></div>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const members = [
    {
      name: "Dogus Darici",
      role: "Principal Investigator",
      degree: "Univ.-Prof. Dr.",
      photo: "images/darici.jpg",
      affiliation: "Lausitz Medical School, Department of Basic Sciences",
      research: "Visual expertise in medical education; Eye-tracking methodology.",
education: [
  "2011–2017 · Medical School, JLU Giessen / Linköpings Universitet (SWE) / University of Zürich (CH)",
  "2013–2022 · B.Sc. & M.Sc. Psychology, FernUniversität Hagen",
  "2018 · Medical licence (Approbation), Ärztekammer Berlin",
  "2018 · Dr. med., JLU Giessen",
  "2021–2024 · Master of Medical Education (MME), University of Heidelberg",
  "2025 · Habilitation, <i>Venia Legendi</i> for Anatomy",
  "2026 · Full professor for Microscopic Anatomy (W3-level), Lausitz Medical School"
],
      keywords: ["Eye-tracking", "Medical Education", "Visual Expertise"],
      awards: [
      { year: "2021", text: "Teacher of the year award, University of Münster" },
      { year: "2022", text: "Paper of the month award 08/2022, University of Münster" },
      { year: "2024", text: "Teacher of the year award, University of Münster" },
      { year: "2025", text: "NRW state teaching prize for outstanding teaching – category: teaching at universities" }
      ],

      reviewer: [
        "Anatomical Sciences Education", "Medical Teacher", "Annals of Anatomy",
        "Journal of Medical Internet Research", "Medical Education and Training",
        "Surgical and Radiologic Anatomy", "Plos One", "BMC Medical Education",
        "GMS Journal for Medical Education", "Cogent Education", "Discover Education",
        "Journal of Advanced Nursing", "Nature Scientific Reports",
        "Journal of Computer Assisted Learning", "Frontiers in Neuroscience",
        "Advances in Health Sciences Education", "Nature Biomedical Engineering",
        "Medical & Biological Engineering & Computing", "Computers in Human Behavior Reports"
        ],

      memberships: ["GMA", "AMEE", "Anatomische Gesellschaft"],
      publications: [
            { authors: "Darici D., Reissner C., Brockhaus J., Missler M.", year: 2021, title: "Implementation of a fully digital histology course in the anatomical teaching curriculum during COVID-19 pandemic", journal: "Ann Anat 236:151718", doi: "10.1016/j.aanat.2021.151718" },
              { authors: "Darici D., Missler M., Schober A., Masthoff M., Schnittler H., Schmitz M.", year: 2022, title: "Fun slipping into the doctor's role – The relationship between sonoanatomy teaching and professional identity formation before and during the Covid-19 pandemic", journal: "Anat Sci Educ 15(3):447–463", doi: "10.1002/ase.2178" },
      { authors: "Darici D., Schneider A.Y.D., Missler M., Pfleiderer B.", year: 2023, title: "Are stereotypes in decline? The portrayal of female anatomy in e-learning", journal: "Anat Sci Educ 16(4):720–732", doi: "10.1002/ase.2211" },
      { authors: "Darici D., Masthoff M., Rischen R., Schmitz M., Ohlenburg H., Missler M.", year: 2023, title: "Medical imaging training with eye movement modeling examples: A randomized controlled study", journal: "Medical Teacher 45(8):918–924", doi: "10.1080/0142159X.2023.2189538" },
      { authors: "Darici D., Reissner C., Missler M.", year: 2023, title: "Webcam-based eye-tracking to measure visual expertise of medical students during online histology training", journal: "GMS J Med Educ 40(5):Doc60", doi: "10.3205/zma001642" },
      { authors: "Darici D., Flägel K., Sternecker K., Missler M.", year: 2023, title: "Transfer of learning in histology: Insights from a longitudinal study", journal: "Anat Sci Educ 17:274–286", doi: "10.1002/ase.2363" },
      { authors: "Otto N., Böckers A., Shiozawa T., Brunk I., Schumann S., Kugelmann D., Missler M., Darici D.", year: 2024, title: "Profiling learning strategies of medical students: A person-centered approach", journal: "Med Educ 58:1304–1314", doi: "10.1111/medu.15388" },
      { authors: "Bostedt D., Dogan E.H., Benker S.C., Rasmus M.A., Eisner E., Simon N.L., Schmitz M., Missler M., Darici D.", year: 2024, title: "Interprofessional socialization of first-year medical and midwifery students: effects of an ultra-brief anatomy training", journal: "BMC Med Educ 24:464", doi: "10.1186/s12909-024-05451-w" },
      { authors: "Mielke Cabello L.A., Meresman G., Darici D., et al.", year: 2024, title: "Assessment of the Ferroptosis Regulators: GPX4, ACSL4, and Transferrin Receptor 1 in Patient-Derived Endometriosis Tissue", journal: "Biomolecules 14(7):876", doi: "10.3390/biom14070876" },
      { authors: "Lohse Y., Last K., Darici D., Becker S.L., Papan C.", year: 2024, title: "Migration background, skin colour, gender, and infectious disease presentation in clinical vignettes", journal: "Lancet Digital Health 16(8):e539–e540", doi: "10.1016/S2589-7500(24)00112-2" },
      { authors: "Bellstedt M., Holtrup A., Otto N., Berndt M., Scherff A.D., Papan C., Robitzsch A., Missler M., Darici D.", year: 2024, title: "Gaze cueing improves pattern recognition of histology learners", journal: "Anat Sci Educ 00:1–12", doi: "10.1002/ase.2498" },
      { authors: "Brügge E., Ricchizzi S., Arenbeck M., Keller M.N., Schur L., Stummer W., Holling M., Lu M.H., Darici D.", year: 2024, title: "Large language models improve clinical decision making of medical students through patient simulation and structured feedback: A randomized controlled trial", journal: "BMC Medical Education 24:1391", doi: "10.1186/s12909-024-06399-7" },
      { authors: "Neubacher M., Darici D., Krawczyk N., Arslan M., Pruss M., Fehm T., Beyer I.", year: 2024, title: "Effects of systematically guided vs. self-directed laparoscopic box training on learning performances: An observational study", journal: "Geburtshilfe und Frauenheilkunde 84(12):1135–1142", doi: "10.1055/a-2415-5929" },
      { authors: "Lorenz J., Zevano J., Otto N., Schneider B., Papan C., Missler M., Darici D.", year: 2024, title: "Looking at Social Interactions in Medical Education with Dual Eye-Tracking Technology: A Scoping Review", journal: "MedEdPublish 14:215", doi: "10.12688/mep.20577.2" },
      { authors: "Beher A., Moreno-Alfonso J.C., Garnier H., Darici D., Salö M.J., Aubert O.", year: 2025, title: "A Survey of Preoperative, Perioperative, and Postoperative Management Practices for Testicular Torsion in Pediatric Patients among European Surgeons", journal: "Eur J Pediatr Surg 35(01):36–42", doi: "10.1055/s-0044-1790244" },
      { authors: "Grüneberg C., Bäuerle A., Karunakaran S., Darici D., Dörrie N., Teufel M., Benson S., Robitzsch A.", year: 2025, title: "Medical students' acceptance of tailored e-mental health applications to foster mental health: a cross-sectional study", journal: "JMIR Medical Education 11:e58183", doi: "10.2196/58183" },
      { authors: "Masthoff M., Pawelka F., Zak G., de Leng B., Darici D., et al.", year: 2025, title: "Students' perspective on new teaching concepts for medical studies: case- and competency-based learning in radiology", journal: "Insights Imaging 16:31", doi: "10.1186/s13244-025-01909-7" },
      { authors: "Papan C., Gärtner B.C., Simon A., Müller R., Fischer M.R., Darici D., Becker S.L., Last K., Bushuven S.", year: 2025, title: "Stewards for future: Piloting a medical undergraduate elective on antimicrobial stewardship", journal: "GMS J Med Educ 42(1):Doc9", doi: "10.3205/zma001733" },
      { authors: "Darici D., Zimmermann J., Jonkmann K.", year: 2025, title: "The Short Form Cultural Intelligence Scale (SFCQ)", journal: "Psychological Test Adaptation and Development 6:1–10", doi: "10.1027/2698-1866/a000093" },
      { authors: "Gravemeyer S., Darici D., Steike D.R., Schmitz M., Eich H.Th., Oertel M.", year: 2025, title: "Defining the student perspective on radiation oncology – an analysis of factors influencing medical students' decisions for specialized training", journal: "Strahlenther Onkol 201(7):732–738", doi: "10.1007/s00066-025-02396-x" },
      { authors: "Storck A., Schönefeld E., Bellstedt M., Janssen M., Seifert K.E., Darici D.", year: 2025, title: "Eye movement modeling examples in robotic surgery training – A randomized controlled study", journal: "Journal of Surgical Education 82(7):103539", doi: "10.1016/j.jsurg.2025.103539" },
      { authors: "Darici D., Ohlenburg H., Jürgensen L., Papan C., Robitzsch A., Missler M., Schneider B.", year: 2025, title: "Should medical teachers spend more time modelling or coaching students? A dual eye-tracking and randomised controlled study on peer instruction in sonography", journal: "Med Educ 59(10):1105–1116", doi: "10.1111/medu.15725" },
      { authors: "Sieg L., Eismann H., Schneider B., Karsten J., Darici D.", year: 2025, title: "How distractions undermine attentional synchronisation in work-based learning: A randomised controlled study using dual mobile eye-tracking", journal: "Journal of Computer Assisted Learning 41(3):e70059", doi: "10.1111/jcal.70059" },
      { authors: "Darici D., Sieg L., Eismann H., Karsten J.", year: 2025, title: "Leader-follower dynamics in medical training: A dual mobile eye-tracking analysis of teacher-student gaze patterns", journal: "Medical Teacher 48(1):122–130", doi: "10.1080/0142159X.2025.2517719" },
      { authors: "Grüneberg C., Bäuerle A., Karanukaran S., Darici D., et al.", year: 2025, title: "Supporting mental health of medical students: Needs and demands concerning an e-mental health application within medical education", journal: "GMS J Med Educ 42(3):Doc41", doi: "10.3205/zma001765" },
      { authors: "Lu M.H., Azevedo R., Kiesow D., Darici D., Jiang W., Schneider B.", year: 2025, title: "Can Money Buy Better Judgment? High Incentives Backfire on Misinformation Discernment, but AI May Fix it", journal: "Proceedings ICLS 2025, pp. 1459–1463", doi: "10.22318/icls2025.631173" },
      { authors: "Barbian B., Shiozawa T., Gellisch M., Brunk I., Langer-Fischer K., Wagner N., Benker S., Bellstedt M., Otto N., Darici D.", year: 2025, title: "Anatomy learning profiles in relation to student motivation and academic success: A multi-center cross-sectional study", journal: "Anat Sci Educ 18(10):1057–1069", doi: "10.1002/ase.70065" },
      { authors: "Gravemeyer S., Darici D., Steike D., Schmitz M., Eich H.T., Oertel M.", year: 2025, title: "Why Choose a Career in Radiation Oncology? A Comprehensive Analysis on Factors Influencing Medical Students' Decision for a Specialized Training", journal: "Int J Radiat Oncol Biol Phys 123(1):e8–e9", doi: "10.1016/j.ijrobp.2025.05.037" },
      { authors: "Storck A., Römer C.G., Ansorge S., Schönefeld E., Bellstedt M., Barbian B., Janssen M., Seifert K.E., Darici D.", year: 2025, title: "Learning and distraction: Evidence for cognitive load interference in medical education", journal: "Med Educ 1–9", doi: "10.1111/medu.70136" },
      { authors: "Storck A., Bellstedt M., Janssen M., Seifert K. E., Darici D", year: 2026, title: "Instructional design unlocks the effects of prior knowledge activation in surgical education", journal: "J Surg Educ 83(5):103915", doi: "10.1016/j.jsurg.2026.103915" }
      ]
    },
    {
      name: "Michelle Bellstedt",
      role: "Master student",
      degree: "B. Sc.",
      photo: "images/bellstedt.jpg",
      affiliation: "University of Münster",
      research: "Visual expertise in medical education; Eye-tracking methodology.",
      education: [
  "2021-2024 · B. Sc. Psychology, University of Münster",
  "since 2024 · M. Sc. Cognitive Neuroscience (ongoing), University of Münster",
  "2025-2026 · Visiting Researcher at Harvard Graduate School of Education",
  "2026 · Visiting Researcher at Utrecht University"
],
      keywords: ["Eye Tracking", "Medical Education", "Interprofessional Education"],
      awards: [
        { year: "2022-2027", text: "Scholarship holder, Studienstiftung des deutschen Volkes" },
      { year: "2025-2026", text: "Scholarship to study abroad, Heinrich-Hertz-Stiftung" },

      ], reviewer: [
  "German Medical Science Journal for Medical Education", "AMEE", "EARLI (Sig6&7)"

      ], memberships: [], 
      publications: [
      { authors: "Bellstedt M., Holtrup A., Otto N., Berndt M., Scherff A.D., Papan C., Robitzsch A., Missler M., Darici D.", year: 2024, title: "Gaze cueing improves pattern recognition of histology learners", journal: "Anat Sci Educ 00:1–12", doi: "10.1002/ase.2498" },
      { authors: "Storck A., Schönefeld E., Bellstedt M., Janssen M., Seifert K.E., Darici D.", year: 2025, title: "Eye movement modeling examples in robotic surgery training – A randomized controlled study", journal: "Journal of Surgical Education 82(7):103539", doi: "10.1016/j.jsurg.2025.103539" },
      { authors: "Barbian B., Shiozawa T., Gellisch M., Brunk I., Langer-Fischer K., Wagner N., Benker S., Bellstedt M., Otto N., Darici D.", year: 2025, title: "Anatomy learning profiles in relation to student motivation and academic success: A multi-center cross-sectional study", journal: "Anat Sci Educ 18(10):1057–1069", doi: "10.1002/ase.70065" },  
     { authors: "Storck A., Römer C.G., Ansorge S., Schönefeld E., Bellstedt M., Barbian B., Janssen M., Seifert K.E., Darici D.", year: 2025, title: "Learning and distraction: Evidence for cognitive load interference in medical education", journal: "Med Educ 1–9", doi: "10.1111/medu.70136" },
      { authors: "Storck A., Bellstedt M., Janssen M., Seifert K. E., Darici D", year: 2026, title: "Instructional design unlocks the effects of prior knowledge activation in surgical education", journal: "J Surg Educ 83(5):103915", doi: "10.1016/j.jsurg.2026.103915" }
      ]
    },
    {
      name: "Anastasia Samoukina",
      role: "Doctoral Student",
      degree: "M. Sc.",
      photo: "images/bio-photo-2.jpg",
      affiliation: "under construction",
      research: "",
      education: [],
      keywords: [],
      awards: [],
      reviewer: [],
      memberships: [],
      publications: []
    },
    {
      name: "René Bieber",
      role: "Technician",
      degree: "",
      photo: "images/bio-photo-2.jpg",
      affiliation: "under construction",
      research: "",
      education: [],
      keywords: [],
      awards: [],
      reviewer: [],
      memberships: [],
      publications: []
    }
  ];

  function esc(str) {
    return String(str).replace(/&/g, '&amp;').replace(/</g, '&lt;').replace(/>/g, '&gt;').replace(/"/g, '&quot;');
  }

function makeAccordion(label, contentHtml) {
  return `<div class="cv-row">
    <button class="accordion-btn">${label} <span class="acc-arrow">▸</span></button>
    <div class="accordion-content">${contentHtml}</div>
  </div>`;
}

  function openPanel(idx) {
    const m = members[idx];
    const layout = document.getElementById('lab-layout');
    const panelInner = document.getElementById('panel-inner');

    document.querySelectorAll('.member-card').forEach(c => c.classList.remove('active'));
    document.getElementById(`card-${idx}`).classList.add('active');

    let awardsHtml = '';
    if (m.awards && m.awards.length) {
      const items = m.awards.map(a => `<li><span class="award-year">${a.year}</span>${esc(a.text)}</li>`).join('');
      awardsHtml = makeAccordion('Awards', `<ul class="award-list">${items}</ul>`);
    }

    let pubHtml = '';
    if (m.publications && m.publications.length) {
      const items = m.publications.map(p => `<li><strong>${p.year}</strong> — ${esc(p.authors)}. ${esc(p.title)}. <em>${esc(p.journal)}</em>. <a href="https://doi.org/${p.doi}" target="_blank">DOI</a></li>`).join('');
      pubHtml = makeAccordion(`Publications (${m.publications.length})`, `<ul class="pub-list">${items}</ul>`);
    }

    panelInner.innerHTML = `
      <div class="panel-header">
        <div style="display:flex; align-items:center;">
          <img src="${m.photo}" class="panel-photo" onerror="this.src='/images/bio-photo-2.jpg'">
          <div>
            <div class="panel-name">${esc(m.name)}</div>
            <div class="panel-role">${esc(m.role)}</div>
            <div style="font-size:11px; color:#999;">${esc(m.degree)}</div>
          </div>
        </div>
        <button class="close-btn" id="close-x">✕</button>
      </div>
      <div class="cv-row"><div class="cv-label">Affiliation</div><div class="cv-value">${m.affiliation}</div></div>
      <div class="cv-row"><div class="cv-label">Research</div><div class="cv-value">${esc(m.research)}</div></div>
      <div class="cv-row"><div class="cv-label">Career</div><div class="cv-value">${m.education.join('<br>')}</div></div>
<div class="cv-row"><div class="cv-label">Keywords</div><div>${m.keywords.map(k => `<span class="cv-tag">${esc(k)}</span>`).join('')}</div></div>
      ${m.reviewer && m.reviewer.length ? `<div class="cv-row"><div class="cv-label">Reviewer</div><div class="cv-value">${m.reviewer.join(', ')}</div></div>` : ''}
      ${m.memberships && m.memberships.length ? `<div class="cv-row"><div class="cv-label">Memberships</div><div>${m.memberships.map(k => `<span class="cv-tag">${esc(k)}</span>`).join('')}</div></div>` : ''}
      ${awardsHtml} ${pubHtml}
    `;

    layout.classList.add('panel-open');
  }

  // Global click handler
  document.addEventListener('click', function(e) {
    // 1. Check for card click
    const card = e.target.closest('.member-card');
    if (card) {
      const idStr = card.id.split('-')[1];
      openPanel(parseInt(idStr));
      return;
    }

    // 2. Check for close button
    if (e.target.id === 'close-x' || e.target.classList.contains('close-btn')) {
      document.getElementById('lab-layout').classList.remove('panel-open');
      document.querySelectorAll('.member-card').forEach(c => c.classList.remove('active'));
      return;
    }

    // 3. Check for accordion
    const accBtn = e.target.closest('.accordion-btn');
    if (accBtn) {
      const content = accBtn.nextElementSibling;
      content.classList.toggle('open');
      accBtn.querySelector('.acc-arrow').textContent = content.classList.contains('open') ? '▾' : '▸';
    }
  });
});
</script>