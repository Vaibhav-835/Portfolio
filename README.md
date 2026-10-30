# Portfolio
# 💻 Vaibhav | Developer Portfolio

A personal portfolio website built to showcase my projects, with a searchable project board and an AI chatbot that answers questions about me.

🌐 **Live website:** [https://portfolio-vaibhav-8cd0.vercel.app/](https://portfolio-vaibhav-8cd0.vercel.app/)

---

## 🎯 About

I'm Vaibhav, a student developer learning Python and web development by building real projects. My goal is to grow into a strong developer who ships useful things.

## 🛠 Technologies

- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Vercel Serverless Function (Node.js)
- **AI Chatbot:** Groq API (`openai/gpt-oss-20b`, with `openai/gpt-oss-120b` as fallback)
- **Tools:** Git, GitHub, Vercel

## ✨ Features

- Sections: **Home, Projects, Skills, About, Ask AI, Contact**
- **Project search** by name or technology (try "Python", "Quiz" or "Weather")
- **Tag filters** to narrow projects by technology
- **Light / Dark mode toggle**, saved between visits
- **Responsive design** for desktop and mobile, with a mobile menu
- **AI chatbot** that answers questions about my skills and projects using my portfolio data
- Clear **error message** in the chat if the API request fails
- API key stored in **Vercel environment variables**, never in the code or GitHub

## 📂 Projects

| # | Project                       | GitHub                                                                | Live                                                |
|---|-------------------------------|-----------------------------------------------------------------------|-----------------------------------------------------|
| 1 | Interactive Quiz App          | [quiz-app](https://github.com/Vaibhav-835/quiz-app)                   | [Open](https://quiz-app-alpha-ten-56.vercel.app/)   |
| 2 | Little Library (Reading List) | [reading-list](https://github.com/Vaibhav-835/reading-list)           | [Open](https://reading-list-mu-rust.vercel.app/) |
| 3 | Weather API                   | [weather-API](https://github.com/Vaibhav-835/weather-API)             | -                                                   |
| 4 | Python Programs Collection    | [python-programs](https://github.com/Vaibhav-835/python-programs)     | -                                                   |
| 5 | Messy Python Code Improvement | [messy-code](https://github.com/Vaibhav-835/messy-code)               | -                                                   |
| 6 | Bug Fixing Using Cursor AI    | [bug-fixing](https://github.com/Vaibhav-835/bug-fixing)               | -                                                   |

## 📁 Project Structure

```
├── index.html        # Website (HTML, CSS, JS)
├── api/
│   └── chat.js       # Serverless function that calls the Groq API
├── avatar.svg        # Profile avatar
├── package.json
├── .gitignore
└── README.md
```

## 🚀 Setup Instructions

1. **Clone the repo**

   ```
   git clone <your-repository-url>
   cd <repository-folder>
   ```
2. **Get a Groq API key** from [console.groq.com](https://console.groq.com).
3. **Run locally** (needed for the chatbot to work):

   ```
   npm i -g vercel
   echo "GROQ_API_KEY=your_key_here" > .env.local
   vercel dev
   ```

   Open the local URL shown in the terminal.
4. **Deploy on Vercel**

   - Import the GitHub repo in Vercel.
   - Go to **Settings → Environment Variables** and add `GROQ_API_KEY`.
   - Click **Deploy** (redeploy if you added the key afterwards).

> ⚠️ Never commit your API key. `.env` files are listed in `.gitignore`.

## 🤖 How the Chatbot Works

1. The visitor types a question in the chat box.
2. `index.html` sends the conversation to `/api/chat`.
3. The serverless function in `api/chat.js` adds my portfolio data and the secret key from the environment variable, then calls the Groq API.
4. The reply comes back and is shown in the chat. If anything fails, an error message is shown instead.

## 📬 Contact

- 💻 [github.com/Vaibhav-835](https://github.com/Vaibhav-835)

---

*Built one project at a time.* 🚀
