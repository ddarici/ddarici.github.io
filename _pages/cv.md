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
      <img src="/images/darici.jpg" class="member-photo" alt="Dogus Darici">
      <span class="member-name">Dogus Darici</span>
      <span class="member-role">Principal Investigator</span>
    </div>
    <div class="member-card" id="card-1">
      <img src="/images/bellstedt.jpg" class="member-photo" alt="Michelle Bellstedt">
      <span class="member-name">Michelle Bellstedt</span>
      <span class="member-role">Master student</span>
    </div>
    <div class="member-card" id="card-2">
      <img src="/images/samoukina.jpg" class="member-photo" alt="Anastasia Samoukina">
      <span class="member-name">Anastasia Samoukina</span>
      <span class="member-role">Doctoral Researcher</span>
    </div>
    <div class="member-card" id="card-3">
      <img src="/images/bieber.jpg" class="member-photo" alt="René Bieber">
      <span class="member-name">René Bieber</span>
      <span class="member-role">Technician</span>
      <span class="member-title"></span>
    </div>
        <div class="member-card" id="card-4">
      <img src="/images/burmeister.jpg" class="member-photo" alt="Lara Burmeister">
      <span class="member-name">Lara Burmeister</span>
      <span class="member-role">Doctoral Researcher</span>
      <span class="member-title"></span>
    </div>
            <div class="member-card" id="card-5">
      <img src="/images/schmeink.jpg" class="member-photo" alt="Finja Schmeink">
      <span class="member-name">Finja Schmeink</span>
      <span class="member-role">Research Assistant</span>
      <span class="member-title"></span>
    </div>
    <div class="member-card" id="card-6">
      <img src="/images/kruse.jpg" class="member-photo" alt="Devin Kruse">
      <span class="member-name">Devin Kruse</span>
      <span class="member-role">Master student</span>
      <span class="member-title"></span>
    </div>
        <div class="member-card" id="card-7">
      <img src="/images/debel.jpg" class="member-photo" alt="Jana Debel">
      <span class="member-name">Jana Debel</span>
      <span class="member-role">Research Assistant</span>
      <span class="member-title"></span>
    </div>
            <div class="member-card" id="card-8">
      <img src="/images/kuemmel.jpg" class="member-photo" alt="Marie Kümmel">
      <span class="member-name">Marie Kümmel</span>
      <span class="member-role">Postdoctoral Researcher</span>
      <span class="member-title"></span>
    </div>
  </div>

  <div class="side-panel" id="side-panel">
    <div class="panel-inner" id="panel-inner"></div>
  </div>
</div>