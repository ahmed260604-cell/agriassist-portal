<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AgriAssist - Farmer Assistant & Crop Advisory Portal</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

:root {
            --primary: #2d8659;
            --secondary: #f4a460;
            --accent: #228b22;
            --dark: #1a5c3a;
            --light: #f0f7f4;
            --white: #ffffff;
            --text: #2c3e50;
            --shadow: rgba(0, 0, 0, 0.1);
        }

body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text);
            background: linear-gradient(135deg, #f0f7f4 0%, #e8f5e9 100%);
        }

.header {
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
            color: var(--white);
            padding: 1rem 0;
            box-shadow: 0 2px 10px var(--shadow);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

.nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

.logo {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-size: 1.5rem;
            font-weight: bold;
        }

.nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

.nav-links a {
            color: var(--white);
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }

.nav-links a:hover {
            color: var(--secondary);
        }

.container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 2rem;
        }

.hero {
            text-align: center;
            padding: 3rem 0;
            background: var(--white);
            border-radius: 15px;
            box-shadow: 0 5px 20px var(--shadow);
            margin-bottom: 3rem;
        }

.hero h1 {
            color: var(--primary);
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

.hero p {
            font-size: 1.2rem;
            color: var(--text);
            max-width: 600px;
            margin: 0 auto 2rem;
        }

.features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

.feature-card {
            background: var(--white);
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 3px 15px var(--shadow);
            transition: transform 0.3s, box-shadow 0.3s;
            cursor: pointer;
        }

.feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 25px var(--shadow);
        }

.feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

.feature-card h3 {
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

.dashboard {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

.stat-card {
            background: var(--white);
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 2px 10px var(--shadow);
            border-left: 4px solid var(--primary);
        }

.stat-value {
            font-size: 2rem;
            font-weight: bold;
            color: var(--primary);
            margin: 0.5rem 0;
        }

.stat-label {
            color: #666;
            font-size: 0.9rem;
        }

.section {
            background: var(--white);
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 3px 15px var(--shadow);
            margin-bottom: 2rem;
        }

.section h2 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            border-bottom: 3px solid var(--accent);
            padding-bottom: 0.5rem;
        }

.form-group {
            margin-bottom: 1.5rem;
        }

label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--dark);
        }

input, select, textarea {
            width: 100%;
            padding: 0.8rem;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

.btn {
            background: var(--primary);
            color: var(--white);
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: background 0.3s, transform 0.2s;
        }

.btn:hover {
            background: var(--dark);
            transform: translateY(-2px);
        }

.btn-secondary {
            background: var(--secondary);
        }

.btn-secondary:hover {
            background: #d4834d;
        }

.weather-widget {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

.weather-day {
            background: linear-gradient(135deg, #4a90e2 0%, #357abd 100%);
            color: var(--white);
            padding: 1rem;
            border-radius: 10px;
            text-align: center;
        }

.temp {
            font-size: 2rem;
            font-weight: bold;
        }

.crop-recommendation {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

.crop-card {
            background: linear-gradient(135deg, var(--accent) 0%, var(--primary) 100%);
            color: var(--white);
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
        }

.crop-icon {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

.alert {
            padding: 1rem;
            border-radius: 8px;
            margin-bottom: 1rem;
            border-left: 4px solid;
        }

.alert-success {
            background: #d4edda;
            border-color: #28a745;
            color: #155724;
        }

.alert-warning {
            background: #fff3cd;
            border-color: #ffc107;
            color: #856404;
        }

.alert-info {
            background: #d1ecf1;
            border-color: #17a2b8;
            color: #0c5460;
        }

table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 1rem;
        }

th, td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }

th {
            background: var(--primary);
            color: var(--white);
            font-weight: 600;
        }

tr:hover {
            background: var(--light);
        }

.chart-container {
            margin-top: 1rem;
            padding: 1rem;
            background: #fafafa;
            border-radius: 8px;
        }

footer {
            background: var(--dark);
            color: var(--white);
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
        }

@media (max-width: 768px) {
            .nav-links {
                flex-direction: column;
                gap: 1rem;
            }

.hero h1 {
                font-size: 2rem;
            }

.features-grid {
                grid-template-columns: 1fr;
            }
        }

.modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }

.modal-content {
            background: var(--white);
            padding: 2rem;
            border-radius: 12px;
            max-width: 500px;
            width: 90%;
            max-height: 80vh;
            overflow-y: auto;
        }

.close-modal {
            float: right;
            font-size: 2rem;
            cursor: pointer;
            color: #999;
        }

.close-modal:hover {
            color: var(--primary);
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="nav-container">
            <div class="logo">
                🌾 AgriAssist
            </div>
            <nav>
                <ul class="nav-links">
                    <li><a href="#dashboard">Dashboard</a></li>
                    <li><a href="#weather">Weather</a></li>
                    <li><a href="#crops">Crop Advisory</a></li>
                    <li><a href="#market">Market Prices</a></li>
                    <li><a href="#expert">Expert Help</a></li>
                </ul>
            </nav>
        </div>
    </header>

<div class="container">
        <div class="hero">
            <h1>🌱 Welcome to AgriAssist</h1>
            <p>Your intelligent farming companion for better crop management, weather insights, and market intelligence</p>
            <button class="btn" onclick="scrollToSection('dashboard')">Get Started</button>
        </div>

<!-- Dashboard Stats -->
        <div id="dashboard" class="dashboard">
            <div class="stat-card">
                <div class="stat-label">Total Farm Area</div>
                <div class="stat-value">25 Acres</div>
                <small>📍 Maharashtra, India</small>
            </div>
            <div class="stat-card">
                <div class="stat-label">Current Season</div>
                <div class="stat-value">Kharif</div>
                <small>🌦️ Monsoon Season</small>
            </div>
            <div class="stat-card">
                <div class="stat-label">Active Crops</div>
                <div class="stat-value">3</div>
                <small>🌾 Rice, Cotton, Soybean</small>
            </div>
            <div class="stat-card">
                <div class="stat-label">Weather Alert</div>
                <div class="stat-value">Good</div>
                <small>☀️ Clear conditions</small>
            </div>
        </div>

<!-- Features Grid -->
        <div class="features-grid">
            <div class="feature-card" onclick="openModal('weatherModal')">
                <div class="feature-icon">🌤️</div>
                <h3>Weather Forecast</h3>
                <p>7-day accurate weather predictions with alerts for extreme conditions</p>
            </div>
            <div class="feature-card" onclick="openModal('cropModal')">
                <div class="feature-icon">🌾</div>
                <h3>Crop Advisory</h3>
                <p>AI-powered recommendations for crop selection and management</p>
            </div>
            <div class="feature-card" onclick="openModal('soilModal')">
                <div class="feature-icon">🌱</div>
                <h3>Soil Health</h3>
                <p>Soil testing analysis and fertilizer recommendations</p>
            </div>
            <div class="feature-card" onclick="openModal('marketModal')">
                <div class="feature-icon">💰</div>
                <h3>Market Prices</h3>
                <p>Real-time mandi prices and market trends</p>
            </div>
            <div class="feature-card" onclick="openModal('pestModal')">
                <div class="feature-icon">🐛</div>
                <h3>Pest Management</h3>
                <p>Disease detection and treatment recommendations</p>
            </div>
            <div class="feature-card" onclick="openModal('expertModal')">
                <div class="feature-icon">👨🌾</div>
                <h3>Expert Consultation</h3>
                <p>Connect with agricultural experts and advisors</p>
            </div>
        </div>

<!-- Weather Section -->
        <section id="weather" class="section">
            <h2>🌤️ 7-Day Weather Forecast</h2>
            <div class="alert alert-info">
                <strong>Weather Alert:</strong> Light rainfall expected on Day 4. Plan irrigation accordingly.
            </div>
            <div class="weather-widget">
                <div class="weather-day">
                    <div>Mon</div>
                    <div class="temp">32°C</div>
                    <div>☀️ Sunny</div>
                    <small>Humidity: 65%</small>
                </div>
                <div class="weather-day">
                    <div>Tue</div>
                    <div class="temp">31°C</div>
                    <div>⛅ Partly Cloudy</div>
                    <small>Humidity: 70%</small>
                </div>
                <div class="weather-day">
                    <div>Wed</div>
                    <div class="temp">30°C</div>
                    <div>☁️ Cloudy</div>
                    <small>Humidity: 75%</small>
                </div>
                <div class="weather-day">
                    <div>Thu</div>
                    <div class="temp">28°C</div>
                    <div>🌧️ Rain</div>
                    <small>Humidity: 85%</small>
                </div>
                <div class="weather-day">
                    <div>Fri</div>
                    <div class="temp">29°C</div>
                    <div>⛅ Partly Cloudy</div>
                    <small>Humidity: 72%</small>
                </div>
                <div class="weather-day">
                    <div>Sat</div>
                    <div class="temp">31°C</div>
                    <div>☀️ Sunny</div>
                    <small>Humidity: 68%</small>
                </div>
                <div class="weather-day">
                    <div>Sun</div>
                    <div class="temp">33°C</div>
                    <div>☀️ Sunny</div>
                    <small>Humidity: 62%</small>
                </div>
            </div>
        </section>

<!-- Crop Recommendations -->
        <section id="crops" class="section">
            <h2>🌾 Recommended Crops for Your Region</h2>
            <div class="alert alert-success">
                <strong>Best Season:</strong> Current conditions are ideal for Kharif crops
            </div>
            <div class="crop-recommendation">
                <div class="crop-card">
                    <div class="crop-icon">🌾</div>
                    <h3>Rice</h3>
                    <p>High Yield</p>
                    <small>Expected: 25 quintals/acre</small>
                </div>
                <div class="crop-card">
                    <div class="crop-icon">🌽</div>
                    <h3>Maize</h3>
                    <p>Good Market</p>
                    <small>Expected: 30 quintals/acre</small>
                </div>
                <div class="crop-card">
                    <div class="crop-icon">🥜</div>
                    <h3>Groundnut</h3>
                    <p>Suitable Soil</p>
                    <small>Expected: 18 quintals/acre</small>
                </div>
                <div class="crop-card">
                    <div class="crop-icon">🌿</div>
                    <h3>Cotton</h3>
                    <p>Premium Price</p>
                    <small>Expected: 15 quintals/acre</small>
                </div>
            </div>

<div style="margin-top: 2rem;">
                <h3>Crop Selection Tool</h3>
                <form onsubmit="event.preventDefault(); analyzeCrop();">
                    <div class="form-group">
                        <label for="soilType">Soil Type</label>
                        <select id="soilType">
                            <option value="black">Black Soil</option>
                            <option value="red">Red Soil</option>
                            <option value="alluvial">Alluvial Soil</option>
                            <option value="sandy">Sandy Soil</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="rainfall">Average Rainfall (mm)</label>
                        <input type="number" id="rainfall" placeholder="e.g., 800" required>
                    </div>
                    <div class="form-group">
                        <label for="temperature">Average Temperature (°C)</label>
                        <input type="number" id="temperature" placeholder="e.g., 28" required>
                    </div>
                    <button type="submit" class="btn">Get Crop Recommendations</button>
                </form>
                <div id="cropResult" style="margin-top: 1rem;"></div>
            </div>
        </section>

<!-- Market Prices -->
        <section id="market" class="section">
            <h2>💰 Today's Market Prices (Mandi Rates)</h2>
            <div class="alert alert-warning">
                <strong>Market Update:</strong> Wheat prices increased by 5% this week
            </div>
            <table>
                <thead>
                    <tr>
                        <th>Crop</th>
                        <th>Price (₹/Quintal)</th>
                        <th>Change</th>
                        <th>Mandi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>🌾 Wheat</td>
                        <td>₹2,150</td>
                        <td style="color: green;">+5.2% ↑</td>
                        <td>Pune APMC</td>
                    </tr>
                    <tr>
                        <td>🌾 Rice</td>
                        <td>₹1,890</td>
                        <td style="color: green;">+2.1% ↑</td>
                        <td>Mumbai Mandi</td>
                    </tr>
                    <tr>
                        <td>🥜 Groundnut</td>
                        <td>₹5,200</td>
                        <td style="color: red;">-1.5% ↓</td>
                        <td>Nashik Market</td>
                    </tr>
                    <tr>
                        <td>🌿 Cotton</td>
                        <td>₹6,800</td>
                        <td style="color: green;">+3.8% ↑</td>
                        <td>Aurangabad</td>
                    </tr>
                    <tr>
                        <td>🌽 Maize</td>
                        <td>₹1,650</td>
                        <td style="color: gray;">0.0% →</td>
                        <td>Solapur APMC</td>
                    </tr>
                </tbody>
            </table>

<div class="chart-container">
                <canvas id="priceChart"></canvas>
            </div>
        </section>

<!-- Expert Consultation -->
        <section id="expert" class="section">
            <h2>👨🌾 Expert Consultation</h2>
            <div class="alert alert-info">
                <strong>Quick Tip:</strong> Connect with verified agricultural experts for personalized advice
            </div>
            <form onsubmit="event.preventDefault(); submitQuery();">
                <div class="form-group">
                    <label for="expertName">Your Name</label>
                    <input type="text" id="expertName" placeholder="Enter your name" required>
                </div>
                <div class="form-group">
                    <label for="farmLocation">Farm Location</label>
                    <input type="text" id="farmLocation" placeholder="Village, District" required>
                </div>
                <div class="form-group">
                    <label for="queryType">Query Type</label>
                    <select id="queryType">
                        <option value="crop">Crop Selection</option>
                        <option value="pest">Pest/Disease</option>
                        <option value="irrigation">Irrigation</option>
                        <option value="fertilizer">Fertilizer</option>
                        <option value="market">Market Advisory</option>
                        <option value="other">Other</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="expertQuery">Describe Your Query</label>
                    <textarea id="expertQuery" rows="4" placeholder="Describe your problem or question in detail..." required></textarea>
                </div>
                <button type="submit" class="btn">Submit Query</button>
                <button type="button" class="btn btn-secondary" onclick="callExpert()" style="margin-left: 1rem;">📞 Call Expert</button>
            </form>
        </section>

<!-- Soil Health Section -->
        <section class="section">
            <h2>🌱 Soil Health Management</h2>
            <div class="form-group">
                <label for="soilPH">Soil pH Level</label>
                <input type="number" id="soilPH" step="0.1" placeholder="e.g., 6.5">
            </div>
            <div class="form-group">
                <label for="nitrogen">Nitrogen (N) - kg/ha</label>
                <input type="number" id="nitrogen" placeholder="e.g., 120">
            </div>
            <div class="form-group">
                <label for="phosphorus">Phosphorus (P) - kg/ha</label>
                <input type="number" id="phosphorus" placeholder="e.g., 60">
            </div>
            <div class="form-group">
                <label for="potassium">Potassium (K) - kg/ha</label>
                <input type="number" id="potassium" placeholder="e.g., 40">
            </div>
            <button class="btn" onclick="analyzeSoil()">Analyze Soil Health</button>
            <div id="soilResult" style="margin-top: 1rem;"></div>
        </section>
    </div>

<footer>
        <p>&copy; 2026 AgriAssist - Farmer Assistant & Crop Advisory Portal</p>
        <p>College Project | Empowering Farmers with Technology</p>
    </footer>

<!-- Modals -->
    <div id="weatherModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal('weatherModal')">&times;</span>
            <h2>🌤️ Detailed Weather Information</h2>
            <p><strong>Real-time Weather Features:</strong></p>
            <ul>
                <li>Hourly weather updates</li>
                <li>7-day advanced forecast</li>
                <li>Rainfall predictions with accuracy</li>
                <li>Wind speed and direction</li>
                <li>UV index and humidity levels</li>
                <li>SMS/WhatsApp weather alerts</li>
            </ul>
        </div>
    </div>

<div id="cropModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal('cropModal')">&times;</span>
            <h2>🌾 Crop Advisory Services</h2>
            <p><strong>AI-Powered Recommendations:</strong></p>
            <ul>
                <li>Crop selection based on soil & climate</li>
                <li>Optimal sowing and harvesting dates</li>
                <li>Seed variety recommendations</li>
                <li>Crop rotation planning</li>
                <li>Yield prediction models</li>
                <li>Government scheme information</li>
            </ul>
        </div>
    </div>

<div id="soilModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal('soilModal')">&times;</span>
            <h2>🌱 Soil Health Testing</h2>
            <p><strong>Comprehensive Soil Analysis:</strong></p>
            <ul>
                <li>NPK (Nitrogen, Phosphorus, Potassium) levels</li>
                <li>pH and EC testing</li>
                <li>Micronutrient analysis</li>
                <li>Organic carbon content</li>
                <li>Customized fertilizer recommendations</li>
                <li>Soil improvement strategies</li>
            </ul>
        </div>
    </div>

<div id="marketModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal('marketModal')">&times;</span>
            <h2>💰 Market Intelligence</h2>
            <p><strong>Real-Time Market Data:</strong></p>
            <ul>
                <li>Daily mandi prices (APMC rates)</li>
                <li>Historical price trends</li>
                <li>Demand-supply analysis</li>
                <li>Best selling locations</li>
                <li>Transportation cost estimates</li>
                <li>Price alerts and notifications</li>
            </ul>
        </div>
    </div>

<div id="pestModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal('pestModal')">&times;</span>
            <h2>🐛 Pest & Disease Management</h2>
            <p><strong>Early Detection & Prevention:</strong></p>
            <ul>
                <li>Image-based disease identification</li>
                <li>Pest life cycle information</li>
                <li>Organic and chemical treatments</li>
                <li>Preventive measures</li>
                <li>Integrated Pest Management (IPM)</li>
                <li>Emergency helpline access</li>
            </ul>
        </div>
    </div>

<div id="expertModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal('expertModal')">&times;</span>
            <h2>👨🌾 Expert Network</h2>
            <p><strong>Professional Agricultural Support:</strong></p>
            <ul>
                <li>Verified agricultural scientists</li>
                <li>Experienced farmers as mentors</li>
                <li>Video consultation options</li>
                <li>Multilingual support</li>
                <li>Community forums</li>
                <li>24/7 helpline service</li>
            </ul>
        </div>
    </div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script>
        // Price Chart
        const ctx = document.getElementById('priceChart').getContext('2d');
        new Chart(ctx, {
            type: 'line',
            data: {
                labels: ['Week 1', 'Week 2', 'Week 3', 'Week 4', 'Current'],
                datasets: [{
                    label: 'Wheat Price (₹/Quintal)',
                    data: [1950, 2000, 2050, 2100, 2150],
                    borderColor: '#2d8659',
                    backgroundColor: 'rgba(45, 134, 89, 0.1)',
                    tension: 0.4,
                    fill: true
                }, {
                    label: 'Rice Price (₹/Quintal)',
                    data: [1800, 1820, 1850, 1870, 1890],
                    borderColor: '#f4a460',
                    backgroundColor: 'rgba(244, 164, 96, 0.1)',
                    tension: 0.4,
                    fill: true
                }]
            },
            options: {
                responsive: true,
                plugins: {
                    title: {
                        display: true,
                        text: 'Market Price Trends (Last 5 Weeks)'
                    },
                    legend: {
                        position: 'top'
                    }
                },
                scales: {
                    y: {
                        beginAtZero: false,
                        title: {
                            display: true,
                            text: 'Price (₹)'
                        }
                    }
                }
            }
        });

// Modal Functions
        function openModal(modalId) {
            document.getElementById(modalId).style.display = 'flex';
        }

function closeModal(modalId) {
            document.getElementById(modalId).style.display = 'none';
        }

// Close modal on outside click
        window.onclick = function(event) {
            if (event.target.classList.contains('modal')) {
                event.target.style.display = 'none';
            }
        }

// Smooth Scroll
        function scrollToSection(sectionId) {
            document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
        }

// Crop Analysis
        function analyzeCrop() {
            const soil = document.getElementById('soilType').value;
            const rainfall = document.getElementById('rainfall').value;
            const temp = document.getElementById('temperature').value;

let recommendations = [];
            
            if (soil === 'black' && rainfall > 600) {
                recommendations = ['Cotton', 'Soybean', 'Wheat', 'Jowar'];
            } else if (soil === 'alluvial') {
                recommendations = ['Rice', 'Wheat', 'Sugarcane', 'Maize'];
            } else if (rainfall < 500) {
                recommendations = ['Bajra', 'Groundnut', 'Sesame', 'Pulses'];
            } else {
                recommendations = ['Maize', 'Cotton', 'Sorghum', 'Sunflower'];
            }

document.getElementById('cropResult').innerHTML = `
                <div class="alert alert-success">
                    <strong>Recommended Crops:</strong><br>
                    ${recommendations.map(crop => `✅ ${crop}`).join('<br>')}
                    <br><br>
                    <small>Based on: ${soil.charAt(0).toUpperCase() + soil.slice(1)} soil, 
                    ${rainfall}mm rainfall, ${temp}°C temperature</small>
                </div>
            `;
        }

// Soil Analysis
        function analyzeSoil() {
            const ph = document.getElementById('soilPH').value;
            const n = document.getElementById('nitrogen').value;
            const p = document.getElementById('phosphorus').value;
            const k = document.getElementById('potassium').value;

let recommendations = [];
            
            if (ph < 6.0) {
                recommendations.push('Add lime to increase pH (acidic soil)');
            } else if (ph > 7.5) {
                recommendations.push('Add sulfur to decrease pH (alkaline soil)');
            } else {
                recommendations.push('pH level is optimal');
            }

if (n < 100) recommendations.push('Apply Urea or DAP for Nitrogen');
            if (p < 50) recommendations.push('Apply Single Super Phosphate (SSP)');
            if (k < 30) recommendations.push('Apply Muriate of Potash (MOP)');

if (recommendations.length === 1 && recommendations[0] === 'pH level is optimal') {
                recommendations.push('Soil nutrient levels are good');
                recommendations.push('Maintain current fertilizer schedule');
            }

document.getElementById('soilResult').innerHTML = `
                <div class="alert alert-info">
                    <strong>Soil Health Report:</strong><br>
                    ${recommendations.map(rec => `🌱 ${rec}`).join('<br>')}
                </div>
            `;
        }

// Expert Query Submission
        function submitQuery() {
            const name = document.getElementById('expertName').value;
            const location = document.getElementById('farmLocation').value;
            const queryType = document.getElementById('queryType').value;
            const query = document.getElementById('expertQuery').value;

alert(`Thank you, ${name}! Your query regarding "${queryType}" from ${location} has been submitted.\n\nAn expert will contact you within 24 hours.\n\nQuery ID: AE-${Date.now().toString().slice(-6)}`);
            
            // Reset form
            document.getElementById('expertName').value = '';
            document.getElementById('farmLocation').value = '';
            document.getElementById('expertQuery').value = '';
        }

// Call Expert
        function callExpert() {
            alert('📞 Connecting to Expert Helpline: 1800-XXX-XXXX\n\nAvailable: 9 AM - 6 PM (Mon-Sat)\n\nFor immediate assistance, press the call button.');
        }

// Add smooth loading animation
        document.addEventListener('DOMContentLoaded', function() {
            document.body.style.opacity = '0';
            setTimeout(() => {
                document.body.style.transition = 'opacity 0.5s';
                document.body.style.opacity = '1';
            }, 100);
        });
    </script>
</body>
</html>
