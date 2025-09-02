<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <title>คู่มือ Kali Linux เบื้องต้น</title>
  <style>
    body {
      margin: 0;
      font-family: "Segoe UI", Tahoma, sans-serif;
      background-color: #0d1117;
      color: #e6edf3;
      line-height: 1.7;
    }
    header {
      text-align: center;
      padding: 40px 20px;
      background: linear-gradient(135deg, #0d1117, #161b22);
      border-bottom: 2px solid #30363d;
    }
    header img {
      width: 180px;
      margin-bottom: 20px;
    }
    header h1 {
      color: #58a6ff;
      font-size: 2.2em;
      margin: 0;
    }
    section {
      max-width: 850px;
      margin: auto;
      padding: 30px;
      border-bottom: 1px solid #30363d;
    }
    h2 {
      color: #3fb950;
      font-size: 1.6em;
      margin-bottom: 10px;
    }
    p {
      font-size: 1.05em;
      margin-bottom: 12px;
    }
    ul {
      padding-left: 20px;
    }
    ul li {
      margin-bottom: 8px;
    }
    footer {
      text-align: center;
      padding: 20px;
      color: #8b949e;
      font-size: 0.9em;
      background: #161b22;
    }
    code {
      background: #30363d;
      color: #f0f6fc;
      padding: 2px 6px;
      border-radius: 4px;
    }
  </style>
</head>
<body>
  <header>
    <img src="https://www.kali.org/images/kali-dragon-icon.svg" alt="Kali Linux Logo">
    <h1>คู่มือ Kali Linux เบื้องต้น</h1>
  </header>

  <section>
    <h2>1. ทำความรู้จัก Kali Linux</h2>
    <p>
      Kali Linux คือดิสโทรที่ออกแบบมาสำหรับงานทดสอบเจาะระบบ (Penetration Testing) 
      และงานด้าน Security โดยเฉพาะ มาพร้อมเครื่องมือมากกว่า <b>600+</b> รายการ เช่น Nmap, Wireshark, Burp Suite
      และ Metasploit
    </p>
  </section>

  <section>
    <h2>2. การติดตั้ง</h2>
    <p>สามารถติดตั้งได้หลายวิธี:</p>
    <ul>
      <li>Boot ผ่าน USB/DVD</li>
      <li>ติดตั้งลงเครื่องจริง (Dual Boot / Single Boot)</li>
      <li>ใช้ Virtual Machine (เช่น VirtualBox, VMware)</li>
      <li>WSL (Windows Subsystem for Linux)</li>
    </ul>
    <p><b>คำแนะนำ:</b> มือใหม่แนะนำให้ใช้ <code>VirtualBox</code> หรือ <code>VMware</code> เพื่อความปลอดภัย</p>
  </section>

  <section>
    <h2>3. เริ่มต้นใช้งาน</h2>
    <ul>
      <li>Username เริ่มต้น: <code>kali</code></li>
      <li>Password เริ่มต้น: <code>kali</code></li>
      <li>อัปเดตระบบหลังติดตั้งด้วยคำสั่ง: <code>sudo apt update && sudo apt upgrade</code></li>
    </ul>
  </section>

  <section>
    <h2>4. Desktop Environment</h2>
    <p>
      Kali มาพร้อม Desktop หลายแบบ เช่น Xfce (ค่าเริ่มต้น), GNOME, KDE Plasma  
      <br>เลือกได้ตามความชอบ → Xfce เน้นเบาและเร็ว
    </p>
  </section>

  <section>
    <h2>5. การจัดการระบบ</h2>
    <ul>
      <li>ติดตั้งเครื่องมือเพิ่ม: <code>sudo apt install [ชื่อโปรแกรม]</code></li>
      <li>ตรวจสอบ IP: <code>ip a</code></li>
      <li>ตรวจสอบเส้นทาง: <code>ip route</code></li>
      <li>เชื่อมต่อ Wi-Fi ผ่าน Network Manager (ด้านขวาบน)</li>
      <li>ตรวจสอบ service ที่กำลังรัน: <code>systemctl status</code></li>
    </ul>
  </section>

  <section>
    <h2>6. คำสั่งพื้นฐานที่ใช้บ่อย</h2>
    <ul>
      <li>ดูไฟล์/โฟลเดอร์: <code>ls -la</code></li>
      <li>เปลี่ยนไดเรกทอรี: <code>cd [path]</code></li>
      <li>เช็คสิทธิ์ไฟล์: <code>ls -l</code></li>
      <li>แก้ไขไฟล์: <code>nano filename.txt</code></li>
      <li>ตรวจสอบพอร์ตที่เปิด: <code>netstat -tulnp</code></li>
    </ul>
  </section>

  <section>
    <h2>7. เครื่องมือยอดนิยม</h2>
    <ul>
      <li><b>Nmap</b> → สแกนพอร์ตและเครือข่าย</li>
      <li><b>Wireshark</b> → วิเคราะห์ Packet</li>
      <li><b>Metasploit</b> → Framework สำหรับ Exploit</li>
      <li><b>Hydra</b> → Brute Force รหัสผ่าน</li>
      <li><b>Aircrack-ng</b> → เจาะระบบ Wi-Fi</li>
      <li><b>Burp Suite</b> → ทดสอบเว็บแอป</li>
    </ul>
  </section>

  <section>
    <h2>8. ข้อควรระวัง</h2>
    <p>
      ⚠️ <b>Kali Linux ไม่เหมาะสำหรับใช้เป็น OS หลัก</b>  
      ควรใช้ในสภาพแวดล้อมที่ปลอดภัย เช่น Virtual Machine  
      และควรใช้เพื่อการศึกษา ทดสอบ หรือวิจัยด้าน Security เท่านั้น
    </p>
  </section>

  <section>
    <h2>9. แหล่งเรียนรู้เพิ่มเติม</h2>
    <ul>
      <li>เว็บไซต์หลัก: <a href="https://www.kali.org" target="_blank">https://www.kali.org</a></li>
      <li>Kali Tools: <a href="https://www.kali.org/tools/" target="_blank">https://www.kali.org/tools/</a></li>
      <li>Offensive Security Training: <a href="https://www.offsec.com/courses/" target="_blank">https://www.offsec.com/courses/</a></li>
      <li>YouTube: ช่องเกี่ยวกับ Cyber Security, Ethical Hacking</li>
      <li>หนังสือ: “Kali Linux Revealed” (ฟรีจาก Kali.org)</li>
    </ul>
  </section>

  <footer>
    © 2025 คู่มือ Kali Linux เบื้องต้น | สำหรับการศึกษาและการเรียนรู้ด้านความปลอดภัยทางไซเบอร์
  </footer>
</body>
</html>



