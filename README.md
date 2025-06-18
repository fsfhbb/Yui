<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ESP UI - Purple Theme</title>
  <style>
    body {
      background-color: #d966ff;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .hidden {
      display: none;
    }
    .panel, .login {
      background: #1e1e2f;
      color: white;
      padding: 20px;
      border-radius: 15px;
      width: 300px;
      box-shadow: 0 0 20px rgba(0,0,0,0.5);
    }
    .panel h2, .login h2 {
      text-align: center;
      color: #b266ff;
      margin-bottom: 20px;
    }
    .section {
      margin-bottom: 15px;
    }
    .label {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 10px;
    }
    select, input[type="checkbox"] {
      transform: scale(1.2);
    }
    .toggle {
      position: relative;
      display: inline-block;
      width: 40px;
      height: 20px;
    }
    .toggle input {
      opacity: 0;
      width: 0;
      height: 0;
    }
    .slider {
      position: absolute;
      cursor: pointer;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background-color: #ccc;
      transition: .4s;
      border-radius: 20px;
    }
    .slider:before {
      position: absolute;
      content: "";
      height: 14px;
      width: 14px;
      left: 3px;
      bottom: 3px;
      background-color: white;
      transition: .4s;
      border-radius: 50%;
    }
    input:checked + .slider {
      background-color: #b266ff;
    }
    input:checked + .slider:before {
      transform: translateX(20px);
    }
    .color-options label {
      display: block;
      margin-bottom: 5px;
    }
    .login input[type="password"] {
      width: 100%;
      padding: 8px;
      margin-bottom: 15px;
      border-radius: 5px;
      border: none;
    }
    .login button {
      width: 100%;
      padding: 10px;
      background-color: #b266ff;
      border: none;
      border-radius: 5px;
      color: white;
      font-weight: bold;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="login" id="login">
    <h2>ZEUS FREE PANEL</h2>
    <input type="password" id="password" placeholder="Enter password">
    <button onclick="checkLogin()">Login</button>
  </div>

  <div class="panel hidden" id="panel">
    <h2>ของกากจัดโดนกูเจาะกาก</h2>
    <div class="section">
      <div class="label">
        <span>ดูดหัว</span>
        <select>
          <option>ปกติ</option>
          <option>ต่ำ</option>
          <option>กลาง</option>
          <option>สูง</option>
        </select>
      </div>
      <div class="label">
        <span>ช่วยลาก 88%</span>
        <label class="toggle"><input type="checkbox"><span class="slider"></span></label>
      </div>
      <div class="label">
        <span>DPI 4990</span>
        <label class="toggle"><input type="checkbox"><span class="slider"></span></label>
      </div>
      <div class="label">
        <span>FPS 140</span>
        <label class="toggle"><input type="checkbox"><span class="slider"></span></label>
      </div>
      <div class="label">
        <span>144 Hz</span>
        <label class="toggle"><input type="checkbox"><span class="slider"></span></label>
      </div>
      <div class="label">
        <span>จอสมูท</span>
        <label class="toggle"><input type="checkbox"><span class="slider"></span></label>
      </div>
    </div>
    <div class="section color-options">
      <label><input type="checkbox"> กันรายงาน</label>
      <label><input type="checkbox"> กันแบน</label>
      <label><input type="checkbox"> กันติดดำ</label>
      <label><input type="checkbox"> ลบประวัติการรายงาน</label>
    </div>
    <div class="section">
      <div class="label">
        <span>เปิดใช้งานพาแนล</span>
        <label class="toggle"><input type="checkbox"><span class="slider"></span></label>
      </div>
    </div>
  </div>

  <script>
    function checkLogin() {
      const password = document.getElementById('password').value;
      if (password === 'zeusshop') {
        document.getElementById('login').classList.add('hidden');
        document.getElementById('panel').classList.remove('hidden');
      } else {
        alert('Incorrect password!');
      }
    }
  </script>
</body>
</html>
