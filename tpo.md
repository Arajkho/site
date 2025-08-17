---
layout: page
title: "TPO Desk"
permalink: /tpo/
---

# Training & Placement Officer (TPO) Desk

## Message from TPO
> At Hailakandi Polytechnic, we are deeply committed to preparing our students not only with strong academic foundations but also with the practical exposure and industry insights necessary for their professional growth. We believe that education goes beyond classrooms and textbooks; it is about building bridges between students and the dynamic world of work. That is why we continuously strive to establish collaborations with industry leaders, reputed organizations, and skill-development platforms to bring real-world opportunities to our learners. Through internships, industrial visits, placement drives, workshops, and interactive sessions with experts, our students gain first-hand knowledge of workplace requirements and emerging technologies. These engagements not only enhance their technical competencies but also help them develop communication, problem-solving, and teamwork skills that are vital in today’s competitive job market. By fostering such an environment, we aim to empower every student with the confidence, adaptability, and industry-ready skills needed to embark on a successful career path and contribute meaningfully to the growth of society and the nation.  

## Companies Visited
<section class="companies-visited">
  <div class="company-grid">
    <div class="company">
       <img src="https://static.cdnlogo.com/logos/c/94/cummins.svg" alt="Cummins Logo" width="200" height =" auto">
      <p>Cummins</p>
    </div>
    <div class="company">
      <img src="https://static.cdnlogo.com/logos/m/17/mahle.svg" alt="MAHLE Logo" width="200"; height="auto">
       <p>MAHLE Anand</p>
    </div>
    <div class="company">
      <img src="https://www.rdc.in/img/logo.png" alt="RDC Concrete Logo" width="200" height="auto">
     <p>RDC Concrete</p>
    </div>
    <div class="company">
      <img src="https://upload.wikimedia.org/wikipedia/commons/f/f1/Tata_Motors_Logo.svg" alt="Tata Motors Logo" width="250" height="auto">
      <p>Tata Motors</p>
    </div>
    <div class="company">
      <img src="https://www.quesscorp.com/assets/images/quess-logo.svg" alt="Quess Corp Logo">
      <p>Quess Corp</p>
    </div>
    <div class="company">
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/3a/Suzlon_logo.svg" alt="Suzlon Energy Logo">
      <p>Suzlon Energy</p>
    </div>
    <div class="company">
      <img src="https://krishnagroup.co.in/images/logo.png" alt="Krishna Maruti Logo">
      <p>Krishna Maruti</p>
    </div>
    <div class="company">
      <img src="https://www.haldex.com/globalassets/logos/haldex-logo.svg" alt="Haldex Logo">
      <p>Haldex</p>
    </div>
  </div>
</section>

## 📊 Placement Records


<!-- 📊 Placement Records Widget -->
<section id="placement-records" class="placement-section">
  <h2>📈 Placement Records</h2>
 <div class="placement-card">
    <canvas id="placementChart" aria-label="Placement records chart" role="img"></canvas>
    <div class="placement-total">
      <div class="total-number" id="totalCount">+0</div>
      <div class="total-label">placed so far</div>
    </div>
  </div>
</section>
<style>
.placement-section { max-width: 900px; margin: 24px auto; padding: 10px; }
.placement-section h2 { margin-bottom: 12px; color:#0b5cff; }

.placement-card {
  display: grid;
  grid-template-columns: 1fr 200px;
  gap: 18px;
  align-items: center;
  background: #ffffff;
  border: 1px solid #e6e9ef;
  padding: 16px;
  border-radius: 10px;
  box-shadow: 0 6px 18px rgba(8,20,50,0.04);
}
#placementChart { width: 100% !important; height: 260px !important; }

.placement-total { text-align: center; padding: 12px; border-left: 1px dashed #eee; }
.total-number { font-size: 36px; font-weight: 700; color: #1b5cff; }
.total-label { font-size: 13px; color: #666; margin-top: 6px; }

@media (max-width:720px) {
  .placement-card { grid-template-columns: 1fr; }
  .placement-total { border-left: none; border-top: 1px dashed #eee; margin-top: 8px; }
}
</style>

<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>

<script>
const placementData = {
  labels: ['2023', '2024', '2025'],
  values: [18, 34, 18]
};
const totalPlaced = placementData.values.reduce((a,b)=>a+b, 0);

document.addEventListener('DOMContentLoaded', function () {
  const ctx = document.getElementById('placementChart').getContext('2d');
  const grad = ctx.createLinearGradient(0,0,0,300);
  grad.addColorStop(0, 'rgba(27,92,255,0.85)');
  grad.addColorStop(1, 'rgba(27,92,255,0.35)');

  new Chart(ctx, {
    type: 'bar',
    data: {
      labels: placementData.labels,
      datasets: [{
        label: 'Students Placed',
        data: placementData.values,
        backgroundColor: grad,
        borderRadius: 8,
        barThickness: 40
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: { legend: { display: false } },
      scales: {
        x: { grid: { display: false } },
        y: { beginAtZero: true, ticks: { stepSize: 5 } }
      }
    }
  });

  const totalEl = document.getElementById('totalCount');
  animateCountUp(totalEl, totalPlaced, 900);
});

function animateCountUp(el, target, duration=800) {
  const start = 0;
  const range = target - start;
  const startTime = performance.now();
  function step(now) {
    const elapsed = now - startTime;
    const progress = Math.min(elapsed / duration, 1);
    const value = Math.floor(start + range * progress);
    el.textContent = '+' + value;
    if (progress < 1) requestAnimationFrame(step);
    else el.textContent = '+' + target;
  }
  requestAnimationFrame(step);
}
</script>


## Internship Opportunities
- Assam Power Development Corp – IT Internship  
- NIC Assam – Software Development Internship  

## Industry / Field Visits
- Oil India Ltd. – Field Visit (2025)  
- BSNL Guwahati – Telecom Lab Visit (2024)  
