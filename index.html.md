<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8">  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">  
  <title>Special Invitation 💕</title>  
  <style>  
    * {  
      box-sizing: border-box;  
      margin: 0;  
      padding: 0;  
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;  
    }  
  
    body {  
      background: linear-gradient(135deg, #fff5f5 0%, #ffe3e3 100%);  
      min-height: 100vh;  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      padding: 20px;  
      color: #2d3748;  
    }  
  
    .card {  
      background: #ffffff;  
      border-radius: 24px;  
      padding: 32px 24px;  
      width: 100%;  
      max-width: 380px;  
      box-shadow: 0 20px 40px rgba(229, 62, 62, 0.12);  
      text-align: center;  
      position: relative;  
      overflow: hidden;  
    }  
  
    .step {  
      display: none;  
      animation: fadeIn 0.4s ease-in-out forwards;  
    }  
  
    .step.active {  
      display: block;  
    }  
  
    @keyframes fadeIn {  
      from { opacity: 0; transform: translateY(10px); }  
      to { opacity: 1; transform: translateY(0); }  
    }  
  
    .icon {  
      font-size: 3rem;  
      margin-bottom: 12px;  
    }  
  
    h1 {  
      font-size: 1.5rem;  
      font-weight: 700;  
      color: #1a202c;  
      margin-bottom: 8px;  
    }  
  
    p {  
      color: #718096;  
      font-size: 0.95rem;  
      margin-bottom: 24px;  
    }  
  
    .btn-group {  
      display: flex;  
      gap: 12px;  
      justify-content: center;  
      align-items: center;  
      min-height: 50px;  
      position: relative;  
    }  
  
    .btn {  
      padding: 12px 24px;  
      border-radius: 50px;  
      border: none;  
      font-weight: 600;  
      font-size: 1rem;  
      cursor: pointer;  
      transition: all 0.2s ease;  
      text-decoration: none;  
      display: inline-block;  
    }  
  
    .btn-primary {  
      background-color: #e53e3e;  
      color: white;  
      box-shadow: 0 4px 12px rgba(229, 62, 62, 0.3);  
      width: 100%;  
    }  
  
    .btn-primary:active {  
      transform: scale(0.98);  
    }  
  
    .btn-yes {  
      background-color: #e53e3e;  
      color: white;  
      flex: 1;  
    }  
  
    .btn-no {  
      background-color: #edf2f7;  
      color: #4a5568;  
      position: relative;  
    }  
  
    .form-group {  
      text-align: left;  
      margin-bottom: 16px;  
    }  
  
    label {  
      display: block;  
      font-size: 0.85rem;  
      font-weight: 600;  
      color: #4a5568;  
      margin-bottom: 6px;  
    }  
  
    input {  
      width: 100%;  
      padding: 12px 16px;  
      border-radius: 12px;  
      border: 1.5px solid #e2e8f0;  
      font-size: 1rem;  
      outline: none;  
      background: #f7fafc;  
      transition: border 0.2s;  
    }  
  
    input:focus {  
      border-color: #e53e3e;  
      background: #fff;  
    }  
  
    .summary-box {  
      background: #fff5f5;  
      border: 1px dashed #feb2b2;  
      border-radius: 16px;  
      padding: 16px;  
      margin-bottom: 20px;  
      text-align: left;  
    }  
  
    .summary-item {  
      display: flex;  
      justify-content: space-between;  
      margin-bottom: 8px;  
      font-size: 0.95rem;  
    }  
  
    .summary-item:last-child {  
      margin-bottom: 0;  
    }  
  
    .summary-label {  
      color: #718096;  
    }  
  
    .summary-val {  
      font-weight: 600;  
      color: #2d3748;  
    }  
  </style>  
</head>  
<body>  
  
  <div class="card">  
    <!-- Step 1: Question -->  
    <div class="step active" id="step-1">  
      <div class="icon">🌹</div>  
      <h1>Will you go on a date with me?</h1>  
      <p>I promise good food, great company, and zero boring moments.</p>  
      <div class="btn-group">  
        <button class="btn btn-yes" id="yesBtn" onclick="nextStep(2)">Yes! ✨</button>  
        <button class="btn btn-no" id="noBtn" onclick="dodgeNo()">No</button>  
      </div>  
    </div>  
  
    <!-- Step 2: Pick Date & Time -->  
    <div class="step" id="step-2">  
      <div class="icon">📅</div>  
      <h1>Pick a Date & Time</h1>  
      <p>Choose whenever you're free!</p>  
  
      <form id="dateForm" onsubmit="submitForm(event)">  
        <div class="form-group">  
          <label for="dateInput">Date</label>  
          <input type="date" id="dateInput" required>  
        </div>  
  
        <div class="form-group">  
          <label for="timeInput">Time</label>  
          <input type="time" id="timeInput" required>  
        </div>  
  
        <div class="form-group">  
          <label for="placeInput">Anything special you want to do/eat?</label>  
          <input type="text" id="placeInput" placeholder="e.g., Matcha & Dinner 🍵">  
        </div>  
  
        <button type="submit" class="btn btn-primary" style="margin-top: 8px;">Lock It In! 💌</button>  
      </form>  
    </div>  
  
    <!-- Step 3: Confirmation -->  
    <div class="step" id="step-3">  
      <div class="icon">🎉</div>  
      <h1>It's a Date!</h1>  
      <p>Can't wait! Here are our details:</p>  
  
      <div class="summary-box">  
        <div class="summary-item">  
          <span class="summary-label">Date:</span>  
          <span class="summary-val" id="resDate">-</span>  
        </div>  
        <div class="summary-item">  
          <span class="summary-label">Time:</span>  
          <span class="summary-val" id="resTime">-</span>  
        </div>  
        <div class="summary-item">  
          <span class="summary-label">Plan:</span>  
          <span class="summary-val" id="resPlace">-</span>  
        </div>  
      </div>  
  
      <p style="font-size: 0.85rem; color: #a0aec0;">Take a screenshot and send it to me! 😉</p>  
    </div>  
  </div>  
  
  <script>  
    let yesScale = 1;  
  
    function dodgeNo() {  
      const noBtn = document.getElementById('noBtn');  
      const yesBtn = document.getElementById('yesBtn');  
        
      // Make "Yes" button bigger each time "No" is tapped  
      yesScale += 0.2;  
      yesBtn.style.transform = `scale(${yesScale})`;  
        
      // Move "No" button randomly  
      const x = (Math.random() - 0.5) * 120;  
      const y = (Math.random() - 0.5) * 60;  
      noBtn.style.transform = `translate(${x}px, ${y}px)`;  
    }  
  
    function nextStep(stepNumber) {  
      document.querySelectorAll('.step').forEach(step => step.classList.remove('active'));  
      document.getElementById(`step-${stepNumber}`).classList.add('active');  
    }  
  
    function submitForm(e) {  
      e.preventDefault();  
      const dateVal = document.getElementById('dateInput').value;  
      const timeVal = document.getElementById('timeInput').value;  
      const placeVal = document.getElementById('placeInput').value || 'Surprise Date';  
  
      document.getElementById('resDate').textContent = dateVal;  
      document.getElementById('resTime').textContent = timeVal;  
      document.getElementById('resPlace').textContent = placeVal;  
  
      nextStep(3);  
    }  
  </script>  
</body>  
</html>  
