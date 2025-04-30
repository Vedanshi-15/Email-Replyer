
# 📧 Gmail AI Reply Chrome Extension

A Chrome Extension that integrates with Gmail to automatically generate professional email replies using the Gemini AI API. The project uses a React-based frontend and a Spring Boot backend to handle email content, generate replies, and inject them into Gmail's compose window.

## 🚀 Features

- 🔘 Adds an **"AI Reply"** button inside the Gmail interface
- ✨ Generates AI-powered responses using **Gemini API**
- 🔧 Backend built with **Spring Boot**
- 🧪 Tested with **Postman**
- 🧩 Frontend built with **React** and injected into Gmail
- 🛡️ Secure, fast, and easy to use

---

## 🧰 Tech Stack

| Layer        | Technology Used         |
|--------------|--------------------------|
| Frontend     | React, JavaScript, HTML, CSS |
| Backend      | Java, Spring Boot, REST API |
| AI Integration | Gemini API (Google AI)   |
| Testing Tool | Postman                  |
| Browser      | Google Chrome (Extension API) |

---

## 🗂️ Project Category

**Web Application** + **AIML**

---

## 🖼️ How It Works

1. The extension adds a custom **"AI Reply"** button in Gmail's reply toolbar.
2. When clicked, it:
   - Extracts the email content from the Gmail DOM.
   - Sends the content to the Spring Boot backend via a POST request.
   - The backend forwards the request to the **Gemini API**, asking for a professional reply.
   - The generated reply is returned to the frontend.
   - It is then inserted directly into the Gmail compose box using JavaScript.

---

## 🔍 Folder Structure

```
project-root/
├── backend/                # Spring Boot backend
│   └── src/                # Java controller and Gemini integration
├── extension/              # Chrome extension source
│   ├── public/
│   └── src/
│       ├── content.js      # Main logic injected into Gmail
│       └── popup.js        # (Optional) UI popup if needed
├── README.md
├── package.json
└── manifest.json           # Chrome extension configuration
```

---

## 🧪 API Testing with Postman

- ✅ API Endpoint: `POST http://localhost:8080/api/email/generate`
- ✅ Sample Body:
```json
{
  "emailContent": "Hi, can we schedule a meeting next week?",
  "tone": "professional"
}
```
- ✅ Postman used to test Gemini integration and validate backend response.

---

## 🔐 Gemini API Integration

- Used **Google Gemini API** to generate AI-based email replies.
- Backend code makes HTTP POST requests to the Gemini API with prompt and context.
- The Gemini response is parsed and returned to the extension.

---

## 🧑‍💻 Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/gmail-ai-reply-extension.git
cd gmail-ai-reply-extension
```

### 2. Start the Backend (Spring Boot)
- Open the `backend/` folder in your IDE.
- Update Gemini API key in `application.properties`.
- Run the application.

### 3. Setup the Chrome Extension
- Go to `chrome://extensions/`
- Enable **Developer Mode**
- Click **Load Unpacked**
- Select the `extension/` directory

### 4. Run Frontend (React)
```bash
cd extension
npm install
npm run build
```

---

## 🧠 Future Improvements

- Add tone customization (casual, friendly, assertive)
- Support for multi-language replies
- Integration with other email platforms (e.g., Outlook)

---

## 👤 Author

**Your Name**  
B.Tech (AI & DS)  
GitHub: [@your-username](https://github.com/your-username)

---

## 📜 License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it.
