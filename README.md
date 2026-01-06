<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>AWS Auto-Scalable Application | DevOps Project</title>

  <!-- Premium Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg-main: #0b1220;
      --bg-card: #111827;
      --accent: #38bdf8;
      --accent-dark: #0284c7;
      --text-main: #e5e7eb;
      --text-muted: #9ca3af;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: radial-gradient(circle at top, #0f172a, #020617);
      color: var(--text-main);
      font-family: 'Inter', sans-serif;
      line-height: 1.7;
    }

    /* ---------- HEADER ---------- */
    header {
      padding: 80px 20px;
      text-align: center;
      background: linear-gradient(135deg, #0ea5e9, #1e40af);
    }

    header h1 {
      font-size: 3rem;
      font-weight: 700;
      letter-spacing: -1px;
    }

    header p {
      margin-top: 12px;
      font-size: 1.15rem;
      opacity: 0.95;
    }

    /* ---------- SECTIONS ---------- */
    section {
      max-width: 1100px;
      margin: auto;
      padding: 60px 20px;
    }

    h2 {
      font-size: 1.8rem;
      color: var(--accent);
      margin-bottom: 25px;
      position: relative;
      padding-left: 15px;
    }

    h2::before {
      content: '';
      position: absolute;
      left: 0;
      top: 6px;
      height: 70%;
      width: 5px;
      background: var(--accent);
      border-radius: 4px;
    }

    /* ---------- CARD ---------- */
    .card {
      background: linear-gradient(145deg, #020617, #020617);
      border: 1px solid rgba(255,255,255,0.05);
      padding: 28px;
      border-radius: 16px;
      margin-bottom: 28px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.4);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .card:hover {
      transform: translateY(-6px);
      box-shadow: 0 30px 60px rgba(0,0,0,0.6);
    }

    /* ---------- SERVICES ---------- */
    .services span {
      display: inline-block;
      margin: 6px;
      padding: 10px 16px;
      border-radius: 999px;
      background: rgba(56,189,248,0.12);
      color: var(--accent);
      font-size: 0.9rem;
      font-weight: 500;
    }

    /* ---------- LIST ---------- */
    ul {
      margin-left: 20px;
    }

    ul li {
      margin-bottom: 10px;
      color: var(--text-muted);
    }

    /* ---------- CODE BLOCK ---------- */
    pre {
      margin-top: 18px;
      padding: 20px;
      border-radius: 12px;
      background: #020617;
      color: #7dd3fc;
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.9rem;
      overflow-x: auto;
    }

    /* ---------- FOOTER ---------- */
    footer {
      text-align: center;
      padding: 35px 15px;
      background: #020617;
      font-size: 0.9rem;
      color: var(--text-muted);
    }

    footer span {
      color: var(--accent);
      font-weight: 600;
    }

    @media (max-width: 768px) {
      header h1 { font-size: 2.2rem; }
      section { padding: 40px 18px; }
    }
  </style>
</head>
<body>

<header>
  <h1>🚀 AWS Auto-Scalable Application</h1>
  <p>Production-Style DevOps Project with Monitoring, Storage & Alerts</p>
</header>

<section>
  <h2>🧩 Services Used</h2>
  <div class="card services">
    <span>Elastic Beanstalk</span>
    <span>EC2</span>
    <span>Auto Scaling</span>
    <span>S3</span>
    <span>CloudWatch</span>
    <span>SNS</span>
    <span>IAM</span>
  </div>
</section>

<section>
  <h2>🎯 Project Objective</h2>
  <div class="card">
    <p>
      Deploy a web application using <strong>Elastic Beanstalk</strong>, enable
      automatic <strong>EC2 scaling</strong>, store files securely in
      <strong>S3</strong>, monitor system health via <strong>CloudWatch</strong>,
      and receive real-time alerts through <strong>SNS</strong>.
    </p>
  </div>
</section>

<section>
  <h2>🏗️ Architecture Flow</h2>
  <div class="card">
    <pre>User
  ↓
Elastic Beanstalk Environment
  ↓
EC2 (Auto Scaling Group)
  ↓
CloudWatch Monitoring
  ↓
SNS Notifications
  ↓
S3 Storage</pre>
  </div>
</section>

<section>
  <h2>⚙️ Key Implementation Steps</h2>

  <div class="card">
    <h3>1️⃣ S3 Storage Setup</h3>
    <ul>
      <li>Create bucket <strong>app-storage-demo</strong></li>
      <li>Upload application assets or logs</li>
      <li>Used as centralized object storage</li>
    </ul>
    <pre>aws s3 ls
aws s3 ls s3://app-storage-demo</pre>
  </div>

  <div class="card">
    <h3>2️⃣ SNS Alerts</h3>
    <ul>
      <li>Create SNS topic <strong>app-alerts</strong></li>
      <li>Email subscription for alerts</li>
      <li>Integrated with CloudWatch alarms</li>
    </ul>
  </div>

  <div class="card">
    <h3>3️⃣ Elastic Beanstalk Deployment</h3>
    <ul>
      <li>Platform: Python / Node.js</li>
      <li>Auto provisions EC2 & Auto Scaling</li>
      <li>Health monitored by CloudWatch</li>
    </ul>
  </div>
</section>

<section>
  <h2>📈 Key Outcomes</h2>
  <div class="card">
    <ul>
      <li>✔ Automatic scaling during traffic spikes</li>
      <li>✔ Centralized monitoring & alerting</li>
      <li>✔ Secure IAM-based access to S3</li>
      <li>✔ Real-world DevOps deployment experience</li>
    </ul>
  </div>
</section>

<footer>
  <p>Built by <span>Jhansy Lakshmi</span> | AWS DevOps Portfolio Project</p>
</footer>

</body>
</html>
