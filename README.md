<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SecureAI Ambulance - Hedera Africa Hackathon 2025</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.7.0/styles/atom-one-dark.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.7.0/highlight.min.js"></script>
    <script>hljs.highlightAll();</script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #12CBC4;
            --secondary: #0A3D62;
            --accent: #FFC312;
            --dark: #1B1464;
            --light: #f8f9ff;
            --emergency: #e74c3c;
            --code-bg: #282c34;
        }
        
        body {
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: white;
            line-height: 1.6;
            min-height: 100vh;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        header {
            padding: 1.5rem 0;
            background: rgba(0, 0, 0, 0.3);
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(10px);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .logo-icon {
            font-size: 2rem;
            color: var(--primary);
        }
        
        .logo-text {
            font-size: 1.5rem;
            font-weight: 700;
        }
        
        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        .hero {
            padding: 5rem 0;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(to right, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .btn-accent {
            background: linear-gradient(to right, var(--accent), #ff9f43);
        }
        
        .btn-emergency {
            background: linear-gradient(to right, var(--emergency), #c0392b);
        }
        
        .app-showcase {
            padding: 5rem 0;
            background: rgba(0, 0, 0, 0.2);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.2rem;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: var(--primary);
            border-radius: 2px;
        }
        
        .problem-solution {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            margin-bottom: 5rem;
        }
        
        .problem, .solution {
            background: linear-gradient(135deg, rgba(10, 61, 98, 0.5), rgba(27, 20, 100, 0.5));
            padding: 2.5rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .problem h3, .solution h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--accent);
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .problem-list, .solution-list {
            list-style: none;
            margin: 2rem 0;
        }
        
        .problem-list li, .solution-list li {
            margin-bottom: 1rem;
            display: flex;
            align-items: flex-start;
            gap: 1rem;
        }
        
        .problem-list i {
            color: var(--emergency);
            font-size: 1.2rem;
            margin-top: 0.3rem;
        }
        
        .solution-list i {
            color: var(--primary);
            font-size: 1.2rem;
            margin-top: 0.3rem;
        }
        
        .contributions {
            background: linear-gradient(135deg, rgba(10, 61, 98, 0.5), rgba(27, 20, 100, 0.5));
            padding: 3rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            margin-bottom: 5rem;
        }
        
        .contribution-item {
            margin-bottom: 2rem;
            padding: 1.5rem;
            background: rgba(0, 0, 0, 0.2);
            border-radius: 10px;
        }
        
        .contribution-item h4 {
            font-size: 1.4rem;
            margin-bottom: 1rem;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin: 2rem 0;
        }
        
        .tech-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-size: 0.9rem;
        }
        
        .participant {
            padding: 5rem 0;
            text-align: center;
        }
        
        .participant-card {
            background: linear-gradient(135deg, rgba(10, 61, 98, 0.5), rgba(27, 20, 100, 0.5));
            padding: 3rem;
            border-radius: 15px;
            text-align: center;
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            max-width: 800px;
            margin: 0 auto;
        }
        
        .participant-icon {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 1.5rem;
            border: 5px solid var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            background: rgba(0, 0, 0, 0.3);
            color: var(--accent);
        }
        
        .participant-name {
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
            color: var(--accent);
        }
        
        .participant-role {
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .participant-details {
            text-align: left;
            margin: 2rem 0;
        }
        
        .participant-details p {
            margin-bottom: 1rem;
            line-height: 1.8;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        .demo-section {
            padding: 5rem 0;
            background: rgba(0, 0, 0, 0.2);
        }
        
        .demo-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .video-container {
            position: relative;
            width: 100%;
            padding-bottom: 56.25%; /* 16:9 aspect ratio */
            margin: 2rem 0;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .video-placeholder {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(10, 61, 98, 0.7), rgba(27, 20, 100, 0.7));
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: white;
            backdrop-filter: blur(5px);
            cursor: pointer;
        }
        
        .video-placeholder i {
            font-size: 4rem;
            margin-bottom: 1rem;
            color: var(--accent);
        }
        
        .demo-buttons {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }
        
        .code-section {
            padding: 5rem 0;
            background: rgba(0, 0, 0, 0.3);
        }
        
        .code-container {
            background: var(--code-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            margin: 2rem 0;
        }
        
        .code-header {
            background: rgba(0, 0, 0, 0.2);
            padding: 0.75rem 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .code-title {
            font-weight: 600;
            color: var(--accent);
        }
        
        .code-tabs {
            display: flex;
            gap: 0.5rem;
        }
        
        .code-tab {
            padding: 0.25rem 0.75rem;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            font-size: 0.8rem;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .code-tab.active {
            background: var(--primary);
        }
        
        .code-content {
            padding: 1.5rem;
            overflow-x: auto;
        }
        
        pre {
            margin: 0;
        }
        
        footer {
            background: rgba(0, 0, 0, 0.3);
            padding: 3rem 0;
            text-align: center;
            margin-top: 5rem;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 2rem;
        }
        
        .footer-logo {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .footer-links {
            display: flex;
            gap: 2rem;
            list-style: none;
            flex-wrap: wrap;
            justify-content: center;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--primary);
        }
        
        .copyright {
            margin-top: 2rem;
            opacity: 0.7;
        }
        
        .hosting-section {
            padding: 5rem 0;
            background: rgba(0, 0, 0, 0.2);
            text-align: center;
        }
        
        .hosting-options {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .hosting-option {
            background: linear-gradient(135deg, rgba(10, 61, 98, 0.5), rgba(27, 20, 100, 0.5));
            padding: 2rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .hosting-option h3 {
            color: var(--accent);
            margin-bottom: 1rem;
        }
        
        .hosting-option ul {
            list-style: none;
            text-align: left;
            margin: 1.5rem 0;
        }
        
        .hosting-option li {
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .hosting-option i {
            color: var(--primary);
        }
        
        @media (max-width: 768px) {
            .problem-solution {
                grid-template-columns: 1fr;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: rgba(0, 0, 0, 0.9);
                flex-direction: column;
                padding: 1rem;
                text-align: center;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .demo-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .hosting-options {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <i class="fas fa-ambulance logo-icon"></i>
                    <div class="logo-text">SecureAI Ambulance</div>
                </div>
                <button class="mobile-menu-btn">
                    <i class="fas fa-bars"></i>
                </button>
                <ul class="nav-links">
                    <li><a href="#problem">Problem</a></li>
                    <li><a href="#solution">Solution</a></li>
                    <li><a href="#contributions">Contributions</a></li>
                    <li><a href="#developer">Developer</a></li>
                    <li><a href="#code">Code</a></li>
                    <li><a href="#hosting">Hosting</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>SecureAI Ambulance</h1>
                <p>A Hedera Hashgraph-Based Framework for Privacy-Preserving Emergency Medical Vehicle Networks with Deep Learning Anomaly Detection</p>
                <a href="#problem" class="btn btn-accent">Learn More</a>
                <a href="#developer" class="btn">Meet the Developer</a>
            </div>
        </div>
    </section>

    <section class="app-showcase" id="problem">
        <div class="container">
            <h2 class="section-title">The Problem</h2>
            <div class="problem-solution">
                <div class="problem">
                    <h3><i class="fas fa-exclamation-triangle"></i> Critical Vulnerabilities</h3>
                    <p>Emergency Medical Services (EMS) networks face severe cybersecurity challenges that compromise patient safety and data integrity:</p>
                    <ul class="problem-list">
                        <li><i class="fas fa-shield-alt"></i> Unsecured IoT Medical Data Transmission - Ambulance telemetry (ECG, SpO2, GPS) is transmitted via vulnerable protocols exposing Personally Identifiable Health Information (PHI)</li>
                        <li><i class="fas fa-clock"></i> Latency in Life-Critical Systems - Centralized EMS dispatch systems exhibit mean response latencies of 28.7±12.3s (WHO, 2022), violating clinical golden-hour standards</li>
                        <li><i class="fas fa-user-secret"></i> Privacy Concerns - Patient data is exposed during transmission and processing</li>
                        <li><i class="fas fa-virus"></i> Vulnerability to Cyberattacks - Ambulance systems are vulnerable to GPS spoofing, ransomware, and data tampering</li>
                    </ul>
                </div>
                <div class="solution" id="solution">
                    <h3><i class="fas fa-lightbulb"></i> Our Solution</h3>
                    <p>SecureAI Ambulance addresses these critical issues with a comprehensive framework:</p>
                    <ul class="solution-list">
                        <li><i class="fas fa-lock"></i> End-to-end encryption via Hedera HCS (aBFT consensus) with homomorphic encryption for processing encrypted vitals</li>
                        <li><i class="fas fa-bolt"></i> Hedera smart contracts reduce dispatch latency to <1.5s through decentralized automation</li>
                        <li><i class="fas fa-eye-slash"></i> Zero-knowledge proofs (ZKPs) for privacy-preserving data sharing</li>
                        <li><i class="fas fa-brain"></i> Deep learning model (LSTM Autoencoders) detects anomalies in real-time</li>
                    </ul>
                </div>
            </div>

            <div class="contributions" id="contributions">
                <h2 class="section-title">Key Contributions</h2>
                <div class="contribution-item">
                    <h4><i class="fas fa-tachometer-alt"></i> Life-Saving Speed + Blockchain Efficiency</h4>
                    <p>Solves the problem of traditional blockchains being too slow for emergencies by using Hedera Hashgraph for near-instant, secure data sharing between ambulances, hospitals, and traffic systems without compromising decentralization.</p>
                </div>
                <div class="contribution-item">
                    <h4><i class="fas fa-user-shield"></i> Unhackable Patient Privacy</h4>
                    <p>Implements zero-knowledge proofs (ZKPs) and homomorphic encryption so hospitals receive critical patient data without exposing sensitive details to hackers.</p>
                </div>
                <div class="contribution-item">
                    <h4><i class="fas fa-robot"></i> AI That Predicts Cyberattacks</h4>
                    <p>Deep learning model (LSTM Autoencoders) detects anomalies (e.g., fake GPS signals, data tampering) in real time—stopping attacks before they disrupt rescue operations.</p>
                </div>
                <div class="contribution-item">
                    <h4><i class="fas fa-cogs"></i> Smart Contracts for Automated Emergencies</h4>
                    <p>Self-executing smart contracts automatically turn traffic lights green for ambulances, prioritize ER prep based on incoming patient data, and trigger backup if an ambulance is compromised.</p>
                </div>
                <div class="contribution-item">
                    <h4><i class="fas fa-blueprint"></i> A Blueprint for Future Critical Systems</h4>
                    <p>Beyond ambulances, the framework adapts to disaster response drones, military medevac networks, and smart city emergency protocols.</p>
                </div>

                <h3 style="margin-top: 3rem; color: var(--accent);">Technology Stack</h3>
                <div class="tech-stack">
                    <span class="tech-item">Hedera Hashgraph</span>
                    <span class="tech-item">Hedera Consensus Service (HCS)</span>
                    <span class="tech-item">Smart Contracts</span>
                    <span class="tech-item">Zero-Knowledge Proofs</span>
                    <span class="tech-item">Homomorphic Encryption</span>
                    <span class="tech-item">LSTM Autoencoders</span>
                    <span class="tech-item">Python</span>
                    <span class="tech-item">React.js</span>
                    <span class="tech-item">Node.js</span>
                </div>
            </div>
        </div>
    </section>

    <section class="participant" id="developer">
        <div class="container">
            <h2 class="section-title">Project Developer</h2>
            <div class="participant-card">
                <div class="participant-icon">
                    <i class="fas fa-user-md"></i>
                </div>
                <h3 class="participant-name">Imen Loussaief</h3>
                <p class="participant-role">Chief Engineer and Security Expert | PhD in Cybersecurity</p>
                
                <div class="participant-details">
                    <p>Chief Engineer and Security Expert with PhD from Tunisia Polytechnic School, specializing in cybersecurity with proven academic and practical expertise. Nine years of university-level teaching experience in software development and cybersecurity (ENIcarthage university), certified ethical hacker, and developer of proprietary security solutions.</p>
                    
                    <p>My comprehensive background combines deep technical knowledge in both defensive and offensive security practices, making me uniquely qualified to develop the SecureAI Ambulance solution for the critical healthcare sector.</p>
                    
                    <p><strong>Education:</strong> PhD in Cybersecurity, Tunisia Polytechnic School</p>
                    <p><strong>Position:</strong> Chief Engineer and Security Expert</p>
                    <p><strong>Teaching Experience:</strong> 9 years at ENIcarthage University</p>
                    <p><strong>Certifications:</strong> Certified Ethical Hacker (CEH)</p>
                    <p><strong>Specialization:</strong> Software Development and Cybersecurity</p>
                </div>

                <div class="social-links">
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-linkedin"></i></a>
                    <a href="#"><i class="fab fa-github"></i></a>
                    <a href="#"><i class="fab fa-dev"></i></a>
                </div>
            </div>
        </div>
    </section>

    <section class="demo-section">
        <div class="container">
            <h2 class="section-title">Project Demo</h2>
            <div class="demo-content">
                <p>Watch a demonstration of the SecureAI Ambulance system in action</p>
                
                <div class="video-container">
                    <div class="video-placeholder" id="video-placeholder">
                        <i class="fas fa-play-circle"></i>
                        <p>SecureAI Ambulance Demo Video</p>
                        <p class="btn" style="margin-top: 1rem;">Play Video</p>
                    </div>
                </div>
                
                <div class="demo-buttons">
                    <a href="https://dorahacks.io/buidl/27403" class="btn"><i class="fas fa-external-link-alt"></i> View on DoraHacks</a>
                    <a href="#" class="btn btn-accent"><i class="fab fa-github"></i> GitHub Repository</a>
                    <a href="#" class="btn"><i class="fas fa-file-pdf"></i> Technical White Paper</a>
                </div>
            </div>
        </div>
    </section>

    <section class="code-section" id="code">
        <div class="container">
            <h2 class="section-title">Code Implementation</h2>
            <div class="code-container">
                <div class="code-header">
                    <div class="code-title">Smart Contract Example</div>
                    <div class="code-tabs">
                        <div class="code-tab active">Solidity</div>
                        <div class="code-tab">Python</div>
                        <div class="code-tab">JavaScript</div>
                    </div>
                </div>
                <div class="code-content">
                    <pre><code class="language-javascript">
// Example Hedera Smart Contract for Emergency Dispatch
pragma solidity ^0.8.0;

contract SecureAmbulanceDispatch {
    struct Emergency {
        address reporter;
        string location;
        uint256 timestamp;
        string medicalData;
        bool resolved;
        uint256 priority;
    }
    
    mapping(uint256 => Emergency) public emergencies;
    uint256 public emergencyCount;
    
    event EmergencyReported(uint256 indexed emergencyId, address reporter, string location);
    event EmergencyResolved(uint256 indexed emergencyId);
    
    function reportEmergency(
        string memory _location,
        string memory _medicalData,
        uint256 _priority
    ) public returns (uint256) {
        emergencyCount++;
        emergencies[emergencyCount] = Emergency(
            msg.sender,
            _location,
            block.timestamp,
            _medicalData,
            false,
            _priority
        );
        
        emit EmergencyReported(emergencyCount, msg.sender, _location);
        return emergencyCount;
    }
    
    function resolveEmergency(uint256 _emergencyId) public {
        require(!emergencies[_emergencyId].resolved, "Emergency already resolved");
        emergencies[_emergencyId].resolved = true;
        emit EmergencyResolved(_emergencyId);
    }
    
    function getEmergency(uint256 _emergencyId) public view returns (
        address,
        string memory,
        uint256,
        string memory,
        bool,
        uint256
    ) {
        Emergency memory e = emergencies[_emergencyId];
        return (e.reporter, e.location, e.timestamp, e.medicalData, e.resolved, e.priority);
    }
}
                    </code></pre>
                </div>
            </div>
            
            <div class="code-container">
                <div class="code-header">
                    <div class="code-title">LSTM Anomaly Detection</div>
                    <div class="code-tabs">
                        <div class="code-tab">Solidity</div>
                        <div class="code-tab active">Python</div>
                        <div class="code-tab">JavaScript</div>
                    </div>
                </div>
                <div class="code-content">
                    <pre><code class="language-python">
# LSTM Autoencoder for Anomaly Detection in Medical Data
import numpy as np
import tensorflow as tf
from tensorflow.keras.models import Model
from tensorflow.keras.layers import LSTM, Dense, RepeatVector, TimeDistributed
from tensorflow.keras.callbacks import EarlyStopping

class AnomalyDetector(Model):
    def __init__(self, timesteps, features):
        super(AnomalyDetector, self).__init__()
        self.timesteps = timesteps
        self.features = features
        self.encoder = tf.keras.Sequential([
            LSTM(64, activation='relu', input_shape=(timesteps, features), return_sequences=True),
            LSTM(32, activation='relu', return_sequences=False),
            Dense(16, activation='relu')
        ])
        self.decoder = tf.keras.Sequential([
            RepeatVector(timesteps),
            LSTM(32, activation='relu', return_sequences=True),
            LSTM(64, activation='relu', return_sequences=True),
            TimeDistributed(Dense(features))
        ])

    def call(self, x):
        encoded = self.encoder(x)
        decoded = self.decoder(encoded)
        return decoded

    def detect_anomalies(self, data, threshold):
        reconstructions = self.predict(data)
        loss = tf.keras.losses.mse(reconstructions, data)
        return loss > threshold

# Example usage
def train_anomaly_detector():
    # Simulated medical data (ECG, SpO2, etc.)
    timesteps = 100
    features = 5
    model = AnomalyDetector(timesteps, features)
    model.compile(optimizer='adam', loss='mse')
    
    # Generate sample data
    x_train = np.random.randn(1000, timesteps, features)
    
    # Train the model
    history = model.fit(x_train, x_train, 
                       epochs=50, 
                       batch_size=32,
                       validation_split=0.1,
                       callbacks=[EarlyStopping(patience=3)])
    
    return model
                    </code></pre>
                </div>
            </div>
        </div>
    </section>

    <section class="hosting-section" id="hosting">
        <div class="container">
            <h2 class="section-title">How To Host This Website</h2>
            <p>You can easily host this website using several free options:</p>
            
            <div class="hosting-options">
                <div class="hosting-option">
                    <h3><i class="fab fa-github"></i> GitHub Pages</h3>
                    <ul>
                        <li><i class="fas fa-check"></i> Free hosting</li>
                        <li><i class="fas fa-check"></i> Easy setup for developers</li>
                        <li><i class="fas fa-check"></i> Custom domain support</li>
                        <li><i class="fas fa-check"></i> Version control integration</li>
                    </ul>
                    <a href="https://pages.github.com/" class="btn">Learn More</a>
                </div>
                
                <div class="hosting-option">
                    <h3><i class="fas fa-cloud"></i> Netlify</h3>
                    <ul>
                        <li><i class="fas fa-check"></i> Drag-and-drop deployment</li>
                        <li><i class="fas fa-check"></i> Free tier available</li>
                        <li><i class="fas fa-check"></i> Automatic SSL certificate</li>
                        <li><i class="fas fa-check"></i> Continuous deployment</li>
                    </ul>
                    <a href="https://www.netlify.com/" class="btn">Learn More</a>
                </div>
                
                
</body>
</html>
 
 
