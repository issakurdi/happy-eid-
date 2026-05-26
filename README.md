<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Eid Al-Adha Kurdistan - Elegant Edition</title>

<style>
/* --- Reset & Base Styles --- */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    height: 100vh;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    background: radial-gradient(circle at center, #0a3d30 0%, #051c16 50%, #010b08 100%);
    color: white;
    text-align: center;
    position: relative;
}

/* --- Elegant Background Elements --- */
/* Glowing Crescent Moon & Star */
.moon-container {
    position: absolute;
    top: 5%;
    right: 8%;
    width: 150px;
    height: 150px;
    filter: drop-shadow(0 0 20px rgba(255, 215, 0, 0.6));
}
.crescent {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    box-shadow: 25px 25px 0 0 #ffd700;
}

/* Kurdistan Flag Badge */
.flag-badge {
    position: absolute;
    top: 40px;
    left: 40px;
    width: 120px;
    height: 80px;
    border-radius: 12px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.5);
    display: flex;
    flex-direction: column;
    overflow: hidden;
    border: 2px solid rgba(255, 255, 255, 0.2);
}
.stripe { height: 33.33%; width: 100%; }
.red { background: #e61919; }
.white { 
    background: #ffffff; 
    position: relative; 
    display: flex; 
    justify-content: center; 
    align-items: center; 
}
.green { background: #138808; }

/* CSS Kurdish Sun */
.kurdish-sun {
    width: 24px;
    height: 24px;
    background: #febd11;
    border-radius: 50%;
    position: relative;
    animation: spin 12s linear infinite;
}
.kurdish-sun::before, .kurdish-sun::after {
    content: "";
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 0;
    background: inherit;
    border-radius: 3px;
}
.kurdish-sun::before { transform: rotate(30deg); }
.kurdish-sun::after { transform: rotate(60deg); }

@keyframes spin { 100% { transform: rotate(360deg); } }

/* Minimalist Mountain Silhouette */
.mountain-peaks {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 25vh;
    background: linear-gradient(to top, #010b08 40%, transparent);
    z-index: 1;
}
.mountain-peaks::before {
    content: "";
    position: absolute;
    bottom: 0; width: 100%; height: 100%;
    background: url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=1200&auto=format&fit=crop') center/cover;
    opacity: 0.15;
    mix-blend-mode: lighting;
}

/* --- Main Card Layout --- */
.main-card {
    z-index: 5;
    background: rgba(255, 255, 255, 0.06);
    padding: 40px 50px;
    border-radius: 24px;
    backdrop-filter: blur(15px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4);
    max-width: 90%;
    width: 550px;
    animation: fadeIn 1.2s ease-out;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

.main-card h1 {
    font-size: 48px;
    font-family: 'Traditional Arabic', Georgia, serif;
    background: linear-gradient(45deg, #ffe066, #f5b041);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 10px;
}

.main-card h2 {
    font-size: 30px;
    color: #ffffff;
    font-weight: 500;
    margin-bottom: 15px;
}

.main-card h3 {
    font-size: 20px;
    color: #a3e4d7;
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-bottom: 30px;
}

/* Modernized Button */
.cta-btn {
    background: linear-gradient(135deg, #febd11 0%, #f5b041 100%);
    color: #051c16;
    border: none;
    padding: 16px 35px;
    font-size: 18px;
    font-weight: bold;
    border-radius: 50px;
    cursor: pointer;
    box-shadow: 0 8px 25px rgba(254, 189, 17, 0.4);
    transition: all 0.3s ease;
}
.cta-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 12px 30px rgba(254, 189, 17, 0.6);
}

/* --- Stylized Overlay Form --- */
.modal-overlay {
    display: none;
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(1, 11, 8, 0.85);
    backdrop-filter: blur(8px);
    justify-content: center;
    align-items: center;
    z-index: 100;
}

.modal-content {
    background: #ffffff;
    color: #2c3e50;
    padding: 40px;
    border-radius: 24px;
    width: 360px;
    text-align: right; /* RTL friendly for Kurdish text */
    box-shadow: 0 25px 60px rgba(0,0,0,0.4);
    position: relative;
    animation: scaleUp 0.3s ease;
}

/* Close Button (X) */
.close-btn {
    position: absolute;
    top: 15px;
    left: 15px; /* Left side since the text direction is right-aligned */
    font-size: 22px;
    font-weight: bold;
    color: #95a5a6;
    cursor: pointer;
    background: none;
    border: none;
    transition: color 0.2s ease;
    line-height: 1;
}
.close-btn:hover {
    color: #e74c3c;
}

@keyframes scaleUp {
    from { transform: scale(0.8); opacity: 0; }
    to { transform: scale(1); opacity: 1; }
}

.modal-content h2 {
    font-size: 24px;
    color: #0a3d30;
    margin-bottom: 20px;
    text-align: center;
}

.gift-options {
    margin: 20px 0;
}

.gift-checkbox {
    display: flex;
    align-items: center;
    margin-bottom: 12px;
    cursor: pointer;
    background: #f4f6f6;
    padding: 12px;
    border-radius: 12px;
    transition: background 0.2s;
}
.gift-checkbox:hover { background: #eaeded; }
.gift-checkbox input { margin-left: 10px; width: 18px; height: 18px; accent-color: #0a3d30; }

.modal-content input[type="text"] {
    width: 100%;
    padding: 14px;
    border: 2px solid #d5dbdb;
    border-radius: 12px;
    font-size: 16px;
    text-align: right;
    outline: none;
    transition: border-color 0.3s;
}
.modal-content input[type="text"]:focus { border-color: #0a3d30; }

.submit-btn {
    width: 100%;
    background: #0a3d30;
    color: white;
    padding: 14px;
    border: none;
    border-radius: 12px;
    font-size: 18px;
    font-weight: bold;
    cursor: pointer;
    margin-top: 15px;
    transition: background 0.2s;
}
.submit-btn:hover { background: #115745; }

/* Stars & Confetti Particles */
.particle {
    position: absolute;
    border-radius: 50%;
    pointer-events: none;
}
</style>
</head>
<body>

<!-- Flag -->
<div class="flag-badge">
    <div class="stripe red"></div>
    <div class="white"><div class="kurdish-sun"></div></div>
    <div class="stripe green"></div>
</div>

<!-- Moon -->
<div class="moon-container">
    <div class="crescent"></div>
</div>

<!-- Main Display Card -->
<div class="main-card">
    <h1>عيد الأضحى مبارك</h1>
    <h2>جه‌ژنا قوربانێ پیرۆز بیت</h2>
    <h3>Happy Eid Al-Adha</h3>
    
    <button class="cta-btn" onclick="openForm()">
        🎁  جەژنانە
    </button>
</div>

<!-- Interactive Modal -->
<div id="giftForm" class="modal-overlay" onclick="closeForm()">
    <div class="modal-content" onclick="event.stopPropagation()">
        <!-- Close (X) button added here -->
        <button class="close-btn" onclick="closeForm()">&times;</button>

        <h2>🎉 جەژنی قوربان پیرۆز بێت</h2>
        <p style="text-align: center; color: #7f8c8d;">دیارییەک هەڵبژێرە بۆ جەژنانە:</p>
        
        <div class="gift-options">
            <label class="gift-checkbox">
                <input type="checkbox" value="💰 پارە">
                <span>💰 جەژنانە (پارە)</span>
            </label>
            <label class="gift-checkbox">
                <input type="checkbox" value="🍫 چۆکلێت">
                <span>🍫 چۆکڵێت و شیرینی</span>
            </label>
            
        </div>

        <input type="text" id="userName" placeholder="ناوەکەت بنووسە...">
        <button class="submit-btn" onclick="submitForm()">ناردنی داواکاری</button>
    </div>
</div>

<!-- Mountains Base -->
<div class="mountain-peaks"></div>

<script>
// Ambient Night Stars Generation
function generateStars() {
    for (let i = 0; i < 80; i++) {
        let star = document.createElement("div");
        star.className = "particle";
        star.style.width = Math.random() * 3 + 1 + "px";
        star.style.height = star.style.width;
        star.style.background = "rgba(255, 255, 255, " + Math.random() + ")";
        star.style.left = Math.random() * 100 + "%";
        star.style.top = Math.random() * 70 + "%";
        
        if(Math.random() > 0.7) {
            star.style.boxShadow = "0 0 10px white";
        }
        document.body.appendChild(star);
    }
}
generateStars();

// Modal Functions
function openForm() {
    document.getElementById("giftForm").style.display = "flex";
}

function closeForm() {
    document.getElementById("giftForm").style.display = "none";
}

function submitForm() {
    const name = document.getElementById("userName").value;
    if(name.trim() === "") {
        alert("تکایە سەرەتا ناوەکەت بنووسە!");
        return;
    }
    alert(`🎉 جەژنت پیرۆز بێت ${name}! داواکارییەکەت بە سەرکەوتوویی نێردرا.`);
    closeForm();
    document.getElementById("userName").value = ""; 
}
</script>

</body>
</html>