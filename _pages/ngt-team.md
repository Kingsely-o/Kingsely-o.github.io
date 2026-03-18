---
layout: archive
title: "NGT Team"
permalink: /ngt-team/
author_profile: false
---

{% include base_path %}

<style>
/* ========== NGT Team Page Styles ========== */

/* Hide default page title since we have hero */
.page__title { display: none; }

/* Remove sidebar for full-width layout */
.sidebar { display: none !important; }
#main { max-width: 100%; padding: 0; float: none; }
.archive { max-width: 100%; padding: 0; }

/* CSS Variables */
:root {
  --ngt-primary: #0d47a1;
  --ngt-primary-light: #1565c0;
  --ngt-primary-dark: #0a3680;
  --ngt-accent: #00bcd4;
  --ngt-accent-light: #4dd0e1;
  --ngt-gradient: linear-gradient(135deg, #0d47a1 0%, #1976d2 50%, #00bcd4 100%);
  --ngt-gradient-soft: linear-gradient(135deg, #e3f2fd 0%, #e0f7fa 100%);
  --ngt-text: #263238;
  --ngt-text-light: #546e7a;
  --ngt-bg-light: #f8fafe;
  --ngt-card-shadow: 0 8px 30px rgba(13, 71, 161, 0.08);
  --ngt-card-hover: 0 16px 40px rgba(13, 71, 161, 0.15);
  --ngt-radius: 16px;
  --ngt-section-gap: 80px;
}

/* ---- Hero Section ---- */
.ngt-hero {
  background: var(--ngt-gradient);
  color: white;
  padding: 80px 40px 60px;
  text-align: center;
  position: relative;
  overflow: hidden;
  margin: -20px -40px 0;
}
.ngt-hero::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle at 30% 70%, rgba(255,255,255,0.06) 0%, transparent 50%),
              radial-gradient(circle at 70% 30%, rgba(0,188,212,0.1) 0%, transparent 50%);
  animation: heroFloat 20s ease-in-out infinite;
}
@keyframes heroFloat {
  0%, 100% { transform: translate(0, 0) rotate(0deg); }
  33% { transform: translate(20px, -20px) rotate(1deg); }
  66% { transform: translate(-15px, 15px) rotate(-1deg); }
}
.ngt-hero-content {
  position: relative;
  z-index: 2;
  max-width: 900px;
  margin: 0 auto;
}
.ngt-hero-logo {
  width: 140px;
  height: auto;
  margin-bottom: 24px;
  filter: drop-shadow(0 4px 20px rgba(0,0,0,0.3));
  animation: logoGlow 3s ease-in-out infinite alternate;
}
@keyframes logoGlow {
  from { filter: drop-shadow(0 4px 20px rgba(0,0,0,0.3)); }
  to { filter: drop-shadow(0 4px 30px rgba(0,188,212,0.5)); }
}
.ngt-hero h1 {
  font-size: 2.8em;
  font-weight: 800;
  margin: 0 0 12px;
  letter-spacing: -0.5px;
  text-shadow: 0 2px 10px rgba(0,0,0,0.2);
}
.ngt-hero .subtitle {
  font-size: 1.2em;
  opacity: 0.9;
  font-weight: 300;
  max-width: 700px;
  margin: 0 auto 32px;
  line-height: 1.6;
}
.ngt-hero-photo {
  width: 100%;
  max-width: 800px;
  border-radius: var(--ngt-radius);
  box-shadow: 0 20px 60px rgba(0,0,0,0.3);
  margin-top: 10px;
}
.ngt-hero-caption {
  font-size: 0.85em;
  opacity: 0.7;
  margin-top: 12px;
}

/* ---- Container ---- */
.ngt-container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 24px;
}

/* ---- Section ---- */
.ngt-section {
  padding: 60px 0;
}
.ngt-section:nth-child(even) {
  background: var(--ngt-bg-light);
  margin: 0 -40px;
  padding: 60px 40px;
}
.ngt-section-header {
  text-align: center;
  margin-bottom: 48px;
}
.ngt-section-header h2 {
  font-size: 2em;
  font-weight: 700;
  color: var(--ngt-primary);
  margin: 0 0 12px;
  position: relative;
  display: inline-block;
}
.ngt-section-header h2::after {
  content: '';
  position: absolute;
  bottom: -8px;
  left: 50%;
  transform: translateX(-50%);
  width: 60px;
  height: 3px;
  background: var(--ngt-accent);
  border-radius: 2px;
}
.ngt-section-header p {
  color: var(--ngt-text-light);
  font-size: 1.1em;
  max-width: 600px;
  margin: 20px auto 0;
  line-height: 1.6;
}

/* ---- Stats Bar ---- */
.ngt-stats {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
  padding: 50px 0;
}
.ngt-stat-card {
  text-align: center;
  padding: 32px 20px;
  background: white;
  border-radius: var(--ngt-radius);
  box-shadow: var(--ngt-card-shadow);
  transition: all 0.3s ease;
}
.ngt-stat-card:hover {
  transform: translateY(-6px);
  box-shadow: var(--ngt-card-hover);
}
.ngt-stat-icon {
  font-size: 2.2em;
  margin-bottom: 12px;
}
.ngt-stat-number {
  font-size: 2em;
  font-weight: 800;
  color: var(--ngt-primary);
  margin: 0;
  line-height: 1.2;
}
.ngt-stat-label {
  font-size: 0.85em;
  color: var(--ngt-text-light);
  margin: 6px 0 0;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  font-weight: 500;
}

/* ---- Research Cards ---- */
.ngt-research-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}
.ngt-research-card {
  background: white;
  border-radius: var(--ngt-radius);
  padding: 36px 28px;
  box-shadow: var(--ngt-card-shadow);
  transition: all 0.35s ease;
  border-top: 4px solid transparent;
  position: relative;
  overflow: hidden;
}
.ngt-research-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: var(--ngt-gradient);
  transition: height 0.3s ease;
}
.ngt-research-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--ngt-card-hover);
}
.ngt-research-card:hover::before {
  height: 6px;
}
.ngt-research-card .card-icon {
  font-size: 2.5em;
  margin-bottom: 16px;
}
.ngt-research-card h3 {
  font-size: 1.2em;
  font-weight: 700;
  color: var(--ngt-primary);
  margin: 0 0 14px;
}
.ngt-research-card ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
.ngt-research-card li {
  padding: 8px 0;
  color: var(--ngt-text-light);
  font-size: 0.92em;
  line-height: 1.5;
  border-bottom: 1px solid #f0f4f8;
  position: relative;
  padding-left: 18px;
}
.ngt-research-card li:last-child { border-bottom: none; }
.ngt-research-card li::before {
  content: '';
  position: absolute;
  left: 0;
  top: 14px;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: var(--ngt-accent);
}

/* ---- Photo Gallery ---- */
.ngt-gallery {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
  margin: 32px 0;
}
.ngt-gallery-item {
  position: relative;
  border-radius: var(--ngt-radius);
  overflow: hidden;
  box-shadow: var(--ngt-card-shadow);
  transition: all 0.35s ease;
}
.ngt-gallery-item:hover {
  transform: scale(1.02);
  box-shadow: var(--ngt-card-hover);
}
.ngt-gallery-item img {
  width: 100%;
  height: 280px;
  object-fit: cover;
  display: block;
  transition: transform 0.5s ease;
}
.ngt-gallery-item:hover img {
  transform: scale(1.08);
}
.ngt-gallery-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(transparent, rgba(0,0,0,0.7));
  padding: 40px 20px 18px;
  color: white;
}
.ngt-gallery-overlay h4 {
  margin: 0 0 4px;
  font-size: 1.05em;
  font-weight: 600;
}
.ngt-gallery-overlay p {
  margin: 0;
  font-size: 0.82em;
  opacity: 0.85;
}
.ngt-gallery-full {
  grid-column: 1 / -1;
}
.ngt-gallery-full img {
  height: 360px;
}

/* ---- Team Section ---- */
.ngt-team-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 28px;
}
.ngt-team-card {
  background: white;
  border-radius: var(--ngt-radius);
  padding: 28px;
  box-shadow: var(--ngt-card-shadow);
  display: flex;
  align-items: flex-start;
  gap: 20px;
  transition: all 0.3s ease;
}
.ngt-team-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--ngt-card-hover);
}
.ngt-team-card.director {
  grid-column: 1 / -1;
  background: var(--ngt-gradient-soft);
  border: 2px solid rgba(13, 71, 161, 0.1);
}
.ngt-team-avatar {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: var(--ngt-gradient);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  color: white;
  flex-shrink: 0;
}
.ngt-team-info h4 {
  margin: 0 0 4px;
  font-size: 1.1em;
  font-weight: 700;
  color: var(--ngt-primary-dark);
}
.ngt-team-info .role {
  font-size: 0.85em;
  color: var(--ngt-accent);
  font-weight: 600;
  margin-bottom: 8px;
}
.ngt-team-info p {
  margin: 0;
  font-size: 0.9em;
  color: var(--ngt-text-light);
  line-height: 1.5;
}

/* ---- Project Timeline ---- */
.ngt-projects {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 28px;
}
.ngt-project-card {
  background: white;
  border-radius: var(--ngt-radius);
  overflow: hidden;
  box-shadow: var(--ngt-card-shadow);
  transition: all 0.35s ease;
}
.ngt-project-card:hover {
  transform: translateY(-6px);
  box-shadow: var(--ngt-card-hover);
}
.ngt-project-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}
.ngt-project-body {
  padding: 24px;
}
.ngt-project-tag {
  display: inline-block;
  background: var(--ngt-gradient-soft);
  color: var(--ngt-primary);
  padding: 4px 12px;
  border-radius: 20px;
  font-size: 0.75em;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  margin-bottom: 10px;
}
.ngt-project-body h4 {
  margin: 0 0 8px;
  font-size: 1.15em;
  font-weight: 700;
  color: var(--ngt-text);
}
.ngt-project-body p {
  margin: 0;
  font-size: 0.9em;
  color: var(--ngt-text-light);
  line-height: 1.6;
}

/* ---- Awards ---- */
.ngt-awards-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  margin-bottom: 36px;
}
.ngt-award-item {
  background: white;
  border-radius: 12px;
  padding: 24px;
  box-shadow: var(--ngt-card-shadow);
  display: flex;
  align-items: flex-start;
  gap: 16px;
  transition: all 0.3s ease;
}
.ngt-award-item:hover {
  transform: translateX(6px);
  box-shadow: var(--ngt-card-hover);
}
.ngt-award-badge {
  width: 48px;
  height: 48px;
  border-radius: 12px;
  background: linear-gradient(135deg, #ffd700 0%, #ff8f00 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.4em;
  flex-shrink: 0;
}
.ngt-award-info h4 {
  margin: 0 0 4px;
  font-size: 0.95em;
  font-weight: 700;
  color: var(--ngt-text);
}
.ngt-award-info p {
  margin: 0;
  font-size: 0.82em;
  color: var(--ngt-text-light);
  line-height: 1.4;
}

/* ---- Values / CTA ---- */
.ngt-values-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 20px;
  margin: 36px 0;
}
.ngt-value-item {
  text-align: center;
  padding: 28px 16px;
  border-radius: var(--ngt-radius);
  background: white;
  box-shadow: var(--ngt-card-shadow);
  transition: all 0.3s ease;
}
.ngt-value-item:hover {
  transform: translateY(-6px);
  box-shadow: var(--ngt-card-hover);
}
.ngt-value-icon {
  font-size: 2em;
  margin-bottom: 12px;
}
.ngt-value-item h4 {
  margin: 0 0 8px;
  font-size: 0.95em;
  font-weight: 700;
  color: var(--ngt-primary);
}
.ngt-value-item p {
  margin: 0;
  font-size: 0.78em;
  color: var(--ngt-text-light);
  line-height: 1.4;
}

/* ---- CTA Section ---- */
.ngt-cta {
  background: var(--ngt-gradient);
  color: white;
  text-align: center;
  padding: 60px 40px;
  border-radius: var(--ngt-radius);
  margin: 40px 0;
  position: relative;
  overflow: hidden;
}
.ngt-cta::before {
  content: '';
  position: absolute;
  top: -30px;
  right: -30px;
  width: 200px;
  height: 200px;
  background: rgba(255,255,255,0.05);
  border-radius: 50%;
}
.ngt-cta h2 {
  font-size: 1.8em;
  margin: 0 0 16px;
  font-weight: 700;
  color: white !important;
}
.ngt-cta h2::after { display: none; }
.ngt-cta p {
  font-size: 1.05em;
  opacity: 0.9;
  max-width: 600px;
  margin: 0 auto 28px;
  line-height: 1.6;
}
.ngt-cta-buttons {
  display: flex;
  justify-content: center;
  gap: 16px;
  flex-wrap: wrap;
}
.ngt-cta-btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 12px 28px;
  border-radius: 50px;
  font-size: 0.95em;
  font-weight: 600;
  text-decoration: none !important;
  transition: all 0.3s ease;
}
.ngt-cta-btn.primary {
  background: white;
  color: var(--ngt-primary);
}
.ngt-cta-btn.primary:hover {
  background: #e3f2fd;
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(0,0,0,0.2);
}
.ngt-cta-btn.secondary {
  background: rgba(255,255,255,0.15);
  color: white;
  border: 2px solid rgba(255,255,255,0.4);
}
.ngt-cta-btn.secondary:hover {
  background: rgba(255,255,255,0.25);
  transform: translateY(-2px);
}

/* ---- Collab Cards ---- */
.ngt-collab-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
}
.ngt-collab-card {
  text-align: center;
  padding: 32px 20px;
  border-radius: var(--ngt-radius);
  background: white;
  box-shadow: var(--ngt-card-shadow);
  transition: all 0.3s ease;
  border: 2px solid transparent;
}
.ngt-collab-card:hover {
  transform: translateY(-6px);
  box-shadow: var(--ngt-card-hover);
  border-color: var(--ngt-accent-light);
}
.ngt-collab-icon {
  font-size: 2.4em;
  margin-bottom: 14px;
}
.ngt-collab-card h4 {
  font-size: 0.95em;
  font-weight: 700;
  color: var(--ngt-text);
  margin: 0 0 8px;
}
.ngt-collab-card p {
  font-size: 0.8em;
  color: var(--ngt-text-light);
  margin: 0;
  line-height: 1.4;
}

/* ---- Footer Banner ---- */
.ngt-footer-banner {
  text-align: center;
  padding: 40px 20px;
  margin-top: 20px;
}
.ngt-footer-logo {
  width: 100px;
  opacity: 0.6;
  margin-bottom: 16px;
}
.ngt-footer-text {
  font-size: 0.9em;
  color: var(--ngt-text-light);
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
  font-style: italic;
}

/* ---- Scroll Animations ---- */
.ngt-fade-up {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.7s ease, transform 0.7s ease;
}
.ngt-fade-up.visible {
  opacity: 1;
  transform: translateY(0);
}

/* ---- Responsive ---- */
@media (max-width: 900px) {
  .ngt-hero { padding: 50px 20px 40px; }
  .ngt-hero h1 { font-size: 2em; }
  .ngt-stats { grid-template-columns: repeat(2, 1fr); }
  .ngt-research-grid { grid-template-columns: 1fr; }
  .ngt-team-grid { grid-template-columns: 1fr; }
  .ngt-projects { grid-template-columns: 1fr; }
  .ngt-awards-grid { grid-template-columns: 1fr; }
  .ngt-values-grid { grid-template-columns: repeat(2, 1fr); }
  .ngt-collab-grid { grid-template-columns: repeat(2, 1fr); }
  .ngt-gallery { grid-template-columns: 1fr; }
  .ngt-gallery-item img, .ngt-gallery-full img { height: 220px; }
}
@media (max-width: 500px) {
  .ngt-stats { grid-template-columns: 1fr; }
  .ngt-values-grid { grid-template-columns: 1fr; }
  .ngt-collab-grid { grid-template-columns: 1fr; }
  .ngt-hero h1 { font-size: 1.6em; }
}
</style>

<!-- ==================== HERO SECTION ==================== -->
<div class="ngt-hero">
  <div class="ngt-hero-content">
    <img src="/images/ngt-logo.png" alt="NGT Logo" class="ngt-hero-logo">
    <h1>Next Generation Transportation</h1>
    <p class="subtitle">A cutting-edge research group advancing intelligent transportation systems and traffic safety through AI, computer vision, and data-driven innovation.</p>
    <img src="/images/team-photo-1.jpg" alt="NGT Team Group Photo" class="ngt-hero-photo">
    <p class="ngt-hero-caption">NGT Research Team</p>
  </div>
</div>

<!-- ==================== STATS BAR ==================== -->
<div class="ngt-container">
  <div class="ngt-stats ngt-fade-up">
    <div class="ngt-stat-card">
      <div class="ngt-stat-icon">&#127919;</div>
      <p class="ngt-stat-number">98.5%</p>
      <p class="ngt-stat-label">Detection Accuracy</p>
    </div>
    <div class="ngt-stat-card">
      <div class="ngt-stat-icon">&#128176;</div>
      <p class="ngt-stat-number">$100K+</p>
      <p class="ngt-stat-label">Research Funding</p>
    </div>
    <div class="ngt-stat-card">
      <div class="ngt-stat-icon">&#128218;</div>
      <p class="ngt-stat-number">5+</p>
      <p class="ngt-stat-label">SCI Publications</p>
    </div>
    <div class="ngt-stat-card">
      <div class="ngt-stat-icon">&#129309;</div>
      <p class="ngt-stat-number">8</p>
      <p class="ngt-stat-label">Institutional Partners</p>
    </div>
  </div>
</div>

<!-- ==================== MISSION ==================== -->
<div class="ngt-section" style="background: var(--ngt-bg-light); margin: 0 -40px; padding: 60px 40px;">
  <div class="ngt-container">
    <div class="ngt-section-header ngt-fade-up">
      <h2>Our Mission</h2>
      <p>Developing next-generation solutions for transportation challenges by combining artificial intelligence, computer vision, and advanced analytics to create safer and more efficient traffic systems.</p>
    </div>
  </div>
</div>

<!-- ==================== RESEARCH AREAS ==================== -->
<div class="ngt-section">
  <div class="ngt-container">
    <div class="ngt-section-header ngt-fade-up">
      <h2>Research Focus Areas</h2>
    </div>
    <div class="ngt-research-grid ngt-fade-up">
      <div class="ngt-research-card">
        <div class="card-icon">&#128663;</div>
        <h3>Traffic Safety Analysis</h3>
        <ul>
          <li><strong>Mixed Traffic Flow Analysis</strong> &mdash; trajectory extraction &amp; behavior prediction</li>
          <li><strong>Collision Risk Assessment</strong> &mdash; AI-powered safety evaluation</li>
          <li><strong>Vulnerable Road Users</strong> &mdash; cyclist &amp; pedestrian protection</li>
        </ul>
      </div>
      <div class="ngt-research-card">
        <div class="card-icon">&#129302;</div>
        <h3>Computer Vision &amp; AI</h3>
        <ul>
          <li><strong>AT-YOLOv8 Framework</strong> &mdash; 98.5% accuracy from UAV footage</li>
          <li><strong>Real-time Detection</strong> &mdash; multi-target tracking in traffic</li>
          <li><strong>Deep Learning Models</strong> &mdash; vehicle-VRU interaction modeling</li>
        </ul>
      </div>
      <div class="ngt-research-card">
        <div class="card-icon">&#127961;</div>
        <h3>Smart Transportation</h3>
        <ul>
          <li><strong>Intelligent Management</strong> &mdash; real-time optimization &amp; control</li>
          <li><strong>Edge Computing</strong> &mdash; efficient AI for traffic monitoring</li>
          <li><strong>IoT Integration</strong> &mdash; connected smart city infrastructure</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<!-- ==================== CURRENT PROJECTS ==================== -->
<div class="ngt-section" style="background: var(--ngt-bg-light); margin: 0 -40px; padding: 60px 40px;">
  <div class="ngt-container">
    <div class="ngt-section-header ngt-fade-up">
      <h2>Current Projects</h2>
    </div>
    <div class="ngt-projects ngt-fade-up">
      <div class="ngt-project-card">
        <img src="/images/research-work-1.jpg" alt="Traffic Flow Analysis">
        <div class="ngt-project-body">
          <span class="ngt-project-tag">Computer Vision</span>
          <h4>Enhanced Traffic Flow Analysis</h4>
          <p>Advanced computer vision frameworks for mixed traffic trajectory extraction with unprecedented 98.5% accuracy rates.</p>
        </div>
      </div>
      <div class="ngt-project-card">
        <img src="/images/research-work-2.jpg" alt="LLM Edge Deployment">
        <div class="ngt-project-body">
          <span class="ngt-project-tag">Edge AI</span>
          <h4>LLM Edge Deployment</h4>
          <p>Optimizing Large Language Models for educational AI PC deployment using QLoRA and PEFT techniques across 8 institutions.</p>
        </div>
      </div>
      <div class="ngt-project-card">
        <img src="/images/research-work-3.jpg" alt="Intersection Safety">
        <div class="ngt-project-body">
          <span class="ngt-project-tag">Deep Learning</span>
          <h4>Intelligent Intersection Safety</h4>
          <p>Deep learning models for predicting vehicle-bicycle interaction behaviors at complex urban intersections.</p>
        </div>
      </div>
      <div class="ngt-project-card">
        <img src="/images/lab-work-1.jpg" alt="Environmental AI">
        <div class="ngt-project-body">
          <span class="ngt-project-tag">Environmental AI</span>
          <h4>Environmental AI Applications</h4>
          <p>Machine learning applied to environmental engineering challenges, including microbial activity prediction in paddy soils.</p>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ==================== KEY ACHIEVEMENTS ==================== -->
<div class="ngt-section">
  <div class="ngt-container">
    <div class="ngt-section-header ngt-fade-up">
      <h2>Key Achievements</h2>
    </div>

    <!-- Funded Projects -->
    <div class="ngt-research-grid ngt-fade-up" style="margin-bottom: 40px;">
      <div class="ngt-research-card">
        <div class="card-icon">&#128200;</div>
        <h3>TrafficSense</h3>
        <ul>
          <li>$100,000 funding from HKSTP</li>
          <li>Advanced traffic analysis in Hong Kong</li>
          <li>Real-world deployment</li>
        </ul>
      </div>
      <div class="ngt-research-card">
        <div class="card-icon">&#9889;</div>
        <h3>Smartflow</h3>
        <ul>
          <li>SGD $5,000 from NTU Singapore</li>
          <li>Smart traffic flow optimization</li>
          <li>Ongoing development</li>
        </ul>
      </div>
      <div class="ngt-research-card">
        <div class="card-icon">&#128187;</div>
        <h3>Edge AIPC</h3>
        <ul>
          <li>8 tertiary institutions in GBA</li>
          <li>LLM optimization for education</li>
          <li>QLoRA &amp; PEFT techniques</li>
        </ul>
      </div>
    </div>

    <!-- Awards -->
    <div class="ngt-awards-grid ngt-fade-up">
      <div class="ngt-award-item">
        <div class="ngt-award-badge">&#127942;</div>
        <div class="ngt-award-info">
          <h4>National Scholarship</h4>
          <p>Master's Degree Students (2023, 2024)</p>
        </div>
      </div>
      <div class="ngt-award-item">
        <div class="ngt-award-badge">&#127941;</div>
        <div class="ngt-award-info">
          <h4>Challenge Cup Grand Prize</h4>
          <p>17th Guangdong College Students' Competition</p>
        </div>
      </div>
      <div class="ngt-award-item">
        <div class="ngt-award-badge">&#127944;</div>
        <div class="ngt-award-info">
          <h4>APICTA Merit Award</h4>
          <p>Asia Pacific ICT Alliance Awards (2023)</p>
        </div>
      </div>
      <div class="ngt-award-item">
        <div class="ngt-award-badge">&#127775;</div>
        <div class="ngt-award-info">
          <h4>International Competition</h4>
          <p>Intelligent Simulation of Transport Infrastructure &mdash; 2nd Prize</p>
        </div>
      </div>
    </div>

    <div class="ngt-gallery ngt-fade-up">
      <div class="ngt-gallery-item ngt-gallery-full">
        <img src="/images/award-ceremony.jpg" alt="Award Ceremony">
        <div class="ngt-gallery-overlay">
          <h4>Award Ceremony</h4>
          <p>Recognizing excellence in research and innovation</p>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ==================== TEAM ==================== -->
<div class="ngt-section" style="background: var(--ngt-bg-light); margin: 0 -40px; padding: 60px 40px;">
  <div class="ngt-container">
    <div class="ngt-section-header ngt-fade-up">
      <h2>Team &amp; Collaborators</h2>
    </div>
    <div class="ngt-team-grid ngt-fade-up">
      <div class="ngt-team-card director">
        <div class="ngt-team-avatar">&#128100;</div>
        <div class="ngt-team-info">
          <h4>Jiajun Ou</h4>
          <div class="role">Research Director &middot; PhD Student</div>
          <p>Nanyang Technological University, Singapore<br>Supervisor: Prof. Zhu Feng<br>Traffic Safety Analysis &amp; Machine Learning</p>
        </div>
      </div>
      <div class="ngt-team-card">
        <div class="ngt-team-avatar">&#127891;</div>
        <div class="ngt-team-info">
          <h4>Prof. Zhu Feng</h4>
          <div class="role">PhD Supervisor</div>
          <p>Nanyang Technological University</p>
        </div>
      </div>
      <div class="ngt-team-card">
        <div class="ngt-team-avatar">&#127891;</div>
        <div class="ngt-team-info">
          <h4>Prof. Weiliang Zeng</h4>
          <div class="role">Academic Collaborator</div>
          <p>Guangdong University of Technology</p>
        </div>
      </div>
      <div class="ngt-team-card">
        <div class="ngt-team-avatar">&#11088;</div>
        <div class="ngt-team-info">
          <h4>Prof. Rong Yu</h4>
          <div class="role">Academic Collaborator</div>
          <p>Top 2% Scientists Worldwide</p>
        </div>
      </div>
      <div class="ngt-team-card">
        <div class="ngt-team-avatar">&#11088;</div>
        <div class="ngt-team-info">
          <h4>Prof. Yuan Yong</h4>
          <div class="role">Academic Collaborator</div>
          <p>Top 2% Scientists Worldwide</p>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ==================== RESEARCH ENVIRONMENT ==================== -->
<div class="ngt-section">
  <div class="ngt-container">
    <div class="ngt-section-header ngt-fade-up">
      <h2>Research Environment</h2>
      <p>State-of-the-art facilities combining theoretical innovation with practical implementation.</p>
    </div>
    <div class="ngt-gallery ngt-fade-up">
      <div class="ngt-gallery-item">
        <img src="/images/lab-work-1.jpg" alt="Laboratory Research">
        <div class="ngt-gallery-overlay">
          <h4>Laboratory Research</h4>
          <p>Advanced research environment</p>
        </div>
      </div>
      <div class="ngt-gallery-item">
        <img src="/images/lab-work-2.jpg" alt="Technical Development">
        <div class="ngt-gallery-overlay">
          <h4>Technical Development</h4>
          <p>Development and testing</p>
        </div>
      </div>
      <div class="ngt-gallery-item ngt-gallery-full">
        <img src="/images/team-meeting-2.jpg" alt="Team Collaboration">
        <div class="ngt-gallery-overlay">
          <h4>Team Collaboration</h4>
          <p>Knowledge sharing and collective problem-solving</p>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ==================== ACADEMIC ACTIVITIES ==================== -->
<div class="ngt-section" style="background: var(--ngt-bg-light); margin: 0 -40px; padding: 60px 40px;">
  <div class="ngt-container">
    <div class="ngt-section-header ngt-fade-up">
      <h2>Academic Activities</h2>
      <p>Active participation in conferences, presentations, and scholarly discourse.</p>
    </div>
    <div class="ngt-gallery ngt-fade-up">
      <div class="ngt-gallery-item">
        <img src="/images/new-presentation-1.jpg" alt="Academic Excellence">
        <div class="ngt-gallery-overlay">
          <h4>Academic Excellence</h4>
          <p>Research presentations and scholarly achievements</p>
        </div>
      </div>
      <div class="ngt-gallery-item">
        <img src="/images/new-presentation-2.jpg" alt="Knowledge Exchange">
        <div class="ngt-gallery-overlay">
          <h4>Knowledge Exchange</h4>
          <p>International collaboration and networking</p>
        </div>
      </div>
      <div class="ngt-gallery-item">
        <img src="/images/new-team-activity-1.jpg" alt="Innovation Hub">
        <div class="ngt-gallery-overlay">
          <h4>Innovation Hub</h4>
          <p>Fostering creativity and breakthrough research</p>
        </div>
      </div>
      <div class="ngt-gallery-item">
        <img src="/images/new-team-activity-2.jpg" alt="Collaborative Excellence">
        <div class="ngt-gallery-overlay">
          <h4>Collaborative Excellence</h4>
          <p>Building bridges across disciplines</p>
        </div>
      </div>
    </div>

    <div class="ngt-gallery ngt-fade-up" style="margin-top: 24px;">
      <div class="ngt-gallery-item ngt-gallery-full">
        <img src="/images/team-photo-2.jpg" alt="Team Collaboration">
        <div class="ngt-gallery-overlay">
          <h4>Our Growing Team</h4>
          <p>Academic collaboration and teamwork across institutions</p>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ==================== COLLABORATION ==================== -->
<div class="ngt-section">
  <div class="ngt-container">
    <div class="ngt-section-header ngt-fade-up">
      <h2>Collaboration Opportunities</h2>
      <p>We actively seek partnerships across academia, industry, and government.</p>
    </div>
    <div class="ngt-collab-grid ngt-fade-up">
      <div class="ngt-collab-card">
        <div class="ngt-collab-icon">&#127979;</div>
        <h4>Academic Institutions</h4>
        <p>Research partnerships and student exchanges</p>
      </div>
      <div class="ngt-collab-card">
        <div class="ngt-collab-icon">&#127981;</div>
        <h4>Industry Partners</h4>
        <p>Technology transfer and commercial applications</p>
      </div>
      <div class="ngt-collab-card">
        <div class="ngt-collab-icon">&#127963;</div>
        <h4>Government Agencies</h4>
        <p>Policy development and implementation</p>
      </div>
      <div class="ngt-collab-card">
        <div class="ngt-collab-icon">&#127760;</div>
        <h4>International Orgs</h4>
        <p>Global transportation safety initiatives</p>
      </div>
    </div>
  </div>
</div>

<!-- ==================== VISION & VALUES ==================== -->
<div class="ngt-section" style="background: var(--ngt-bg-light); margin: 0 -40px; padding: 60px 40px;">
  <div class="ngt-container">
    <div class="ngt-section-header ngt-fade-up">
      <h2>Our Vision &amp; Values</h2>
      <p>Pioneering the future of safe and intelligent transportation through cutting-edge AI, computer vision, and collaborative research.</p>
    </div>
    <div class="ngt-values-grid ngt-fade-up">
      <div class="ngt-value-item">
        <div class="ngt-value-icon">&#128161;</div>
        <h4>Innovation</h4>
        <p>Pushing the boundaries of transportation technology</p>
      </div>
      <div class="ngt-value-item">
        <div class="ngt-value-icon">&#128737;&#65039;</div>
        <h4>Safety</h4>
        <p>Protecting all road users</p>
      </div>
      <div class="ngt-value-item">
        <div class="ngt-value-icon">&#129309;</div>
        <h4>Collaboration</h4>
        <p>Bridging academia, industry &amp; government</p>
      </div>
      <div class="ngt-value-item">
        <div class="ngt-value-icon">&#127942;</div>
        <h4>Excellence</h4>
        <p>Highest standards in research</p>
      </div>
      <div class="ngt-value-item">
        <div class="ngt-value-icon">&#127758;</div>
        <h4>Impact</h4>
        <p>Solutions that benefit society</p>
      </div>
    </div>
  </div>
</div>

<!-- ==================== CTA ==================== -->
<div class="ngt-container">
  <div class="ngt-cta ngt-fade-up">
    <h2>Join Our Research Team</h2>
    <p>We welcome PhD students, Master's students, undergraduate interns, and post-doctoral researchers passionate about intelligent transportation.</p>
    <div class="ngt-cta-buttons">
      <a href="mailto:N2409279A@e.ntu.edu.sg" class="ngt-cta-btn primary">&#9993;&#65039; Contact Us</a>
      <a href="https://github.com/Kingsely-o" class="ngt-cta-btn secondary">&#128187; GitHub</a>
    </div>
  </div>
</div>

<!-- ==================== FOOTER BANNER ==================== -->
<div class="ngt-footer-banner">
  <img src="/images/ngt-logo-alt.png" alt="NGT Logo" class="ngt-footer-logo">
  <p class="ngt-footer-text">The NGT Team is committed to advancing transportation safety and efficiency through innovative research and collaborative partnerships.</p>
</div>

<!-- ==================== SCROLL ANIMATION JS ==================== -->
<script>
document.addEventListener('DOMContentLoaded', function() {
  var observer = new IntersectionObserver(function(entries) {
    entries.forEach(function(entry) {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
      }
    });
  }, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });

  document.querySelectorAll('.ngt-fade-up').forEach(function(el) {
    observer.observe(el);
  });
});
</script>
