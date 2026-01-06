<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>AWS Auto-Scalable Application Project</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background: #0f172a;
      color: #e5e7eb;
      line-height: 1.7;
    }

    header {
      background: linear-gradient(135deg, #2563eb, #1e40af);
      padding: 60px 20px;
      text-align: center;
    }

    header h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    header p {
      font-size: 1.1rem;
      opacity: 0.9;
    }

    section {
      padding: 50px 20px;
      max-width: 1100px;
      margin: auto;
    }

    h2 {
      color: #60a5fa;
      margin-bottom: 20px;
      border-left: 5px solid #2563eb;
      padding-left: 15px;
    }

    .card {
      background: #020617;
      padding: 25px;
      border-radius: 12px;
      margin-bottom: 25px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
    }

    ul {
      margin-left: 20px;
    }

    ul li {
      margin-bottom: 10px;
    }

    .services span {
      display: inline-block;
      background: #1e293b;
      padding: 8px 14px;
      border-radius: 20px;
      margin: 6px;
      font-size: 0.9rem;
      color: #93c5fd;
    }

    pre {
      background: #020617;
      padding: 20px;
      border-radius: 10px;
      overflow-x: auto;
      color: #93c5fd;
      margin-top: 15px;
    }

    footer {
      text-align: center;
      padding: 30px;
      background: #020617;
      font-size: 0.9rem;
      opacity: 0.8;
    }

    footer span {
      color: #60a5fa;
    }
  </style>
</head>
<body>

  <!-- HEADER -->
  <header>
    <h1>🚀 AWS Auto-Scalable Application</h1>
    <p>End-to-End Cloud Project with Monitoring, Storage & Notifications</p>
  </header>

  <!-- SERVICES -->
  <section>
    <h2>🧩 Services Used</h2>
    <div class="card services">
      <span>EC2</span>
      <span>Elastic Beanstalk</span>
      <span>Auto Scaling</span>
      <span>S3</span>
      <span>CloudWatch</span>
      <span>SNS</span>
      <span>IAM</span>
    </div>
  </section>

  <!-- OBJECTIVE -->
  <section>
    <h2>🎯 Project Objective</h2>
    <div class="card">
      <p>
        Deploy a web application using <strong>Elastic Beanstalk</strong>, enable
        <strong>automatic scaling</strong> of EC2 instances based on load, store
        application data securely in <strong>S3</strong>, monitor performance
        using <strong>CloudWatch</strong>, and receive real-time alerts through
        <strong>SNS</strong>.
      </p>
    </div>
  </section>

  <!-- ARCHITECTURE -->
  <section>
    <h2>🏗️ Architecture Flow</h2>
    <div class="card">
      <pre>
User
  ↓
Elastic Beanstalk Environment
  ↓
EC2 Instances (Auto Scaling Group)
  ↓
CloudWatch Monitoring
  ↓
SNS Notifications
  ↓
S3 Storage
      </pre>
    </div>
  </section>

  <!-- IMPLEMENTATION -->
  <section>
    <h2>⚙️ Step-by-Step Implementation</h2>

    <div class="card">
      <h3>1️⃣ Create S3 Bucket</h3>
      <ul>
        <li>Create bucket: <strong>app-storage-demo</strong></li>
        <li>Upload sample files</li>
        <li>Used for application storage & logs</li>
      </ul>
      <pre>aws s3 ls
aws s3 ls s3://app-storage-demo</pre>
    </div>

    <div class="card">
      <h3>2️⃣ Create SNS Topic</h3>
      <ul>
        <li>Topic name: <strong>app-alerts</strong></li>
        <li>Email subscription for alerts</li>
        <li>Used for alarm notifications</li>
      </ul>
    </div>

    <div class="card">
      <h3>3️⃣ Deploy with Elastic Beanstalk</h3>
      <ul>
        <li>Platform: Python / Node.js</li>
        <li>Web server environment</li>
        <li>Instance type: <strong>t2.micro</strong></li>
        <li>Auto provisions EC2, ASG & monitoring</li>
      </ul>
    </div>

    <div class="card">
      <h3>4️⃣ Auto Scaling Configuration</h3>
      <ul>
        <li>Minimum instances: 1</li>
        <li>Desired instances: 2</li>
        <li>Maximum instances: 3</li>
      </ul>
    </div>

    <div class="card">
      <h3>5️⃣ CloudWatch Alarm</h3>
      <ul>
        <li>Metric: CPUUtilization</li>
        <li>Threshold: &gt; 70%</li>
        <li>Action: SNS email alert</li>
      </ul>
    </div>

    <div class="card">
      <h3>6️⃣ Secure S3 Access (IAM Role)</h3>
      <ul>
        <li>IAM role attached to EC2</li>
        <li>Policy: AmazonS3ReadOnlyAccess</li>
        <li>No access keys used</li>
      </ul>
    </div>
  </section>

  <!-- OUTCOMES -->
  <section>
    <h2>📈 Key Outcomes</h2>
    <div class="card">
      <ul>
        <li>✔ Auto-scaled EC2 instances based on load</li>
        <li>✔ Centralized monitoring & alerts</li>
        <li>✔ Secure and scalable application setup</li>
        <li>✔ Production-like AWS deployment</li>
      </ul>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <p>Built by <span>Jhansy Lakshmi</span> | AWS DevOps Project</p>
  </footer>

</body>
</html>
