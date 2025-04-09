# Code Review AI

Code Review AI is a web-based application that leverages AI to provide constructive feedback on code. It is designed to help developers, especially beginners, improve their coding skills by offering detailed reviews that focus on code quality, efficiency, readability, and scalability.

---

## Features

- **Interactive Code Editor**: Write or paste your code directly into the editor.
- **AI-Powered Code Review**: Get detailed feedback on your code, including suggestions for improvement.
- **Markdown Rendering**: Reviews are displayed in a clean, readable format with syntax highlighting.

---

## How It Works

1. **Frontend**: A React-based web application where users can input their code and view AI-generated reviews.
2. **Backend**: A Node.js server that processes the code and interacts with the AI model.
3. **AI Integration**: Uses Google Generative AI (Gemini 2.0 Flash model) to analyze the code and generate feedback.

---

## Technologies Used

### Frontend
- React
- `react-simple-code-editor` for the code editor
- `prismjs` for syntax highlighting
- `react-markdown` and `rehype-highlight` for rendering reviews

### Backend
- Node.js with Express.js
- `dotenv` for environment variable management
- Google Generative AI SDK for AI-powered reviews

---

## API Endpoints

### POST `/ai/get-review`
- **Description**: Sends the code to the AI model and retrieves the review.
- **Request Body**:
  ```json
  {
    "code": "string"
  }
  ```
- **Response**:
  ```json
  {
    "review": "string"
  }
  ```

---

## How to Run the Project

### Prerequisites
- Node.js installed
- A Google Generative AI API key

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/code_review_ai.git
   cd code_review_ai
   ```

2. Set up the backend:
   - Navigate to the backend directory:
     ```bash
     cd backend
     ```
   - Install dependencies:
     ```bash
     npm install
     ```
   - Create a `.env` file and add your Google Generative AI API key:
     ```
     GOOGLE_GEMNINI_API=your_api_key_here
     ```
   - Start the backend server:
     ```bash
     node server.js
     ```

3. Set up the frontend:
   - Navigate to the frontend directory:
     ```bash
     cd ../frontend
     ```
   - Install dependencies:
     ```bash
     npm install
     ```
   - Start the frontend development server:
     ```bash
     npm start
     ```

4. Open your browser and navigate to `http://localhost:3000`.

---

## Project Structure

```
code_review_ai/
├── backend/
│   ├── src/
│   │   ├── app.js
│   │   ├── controllers/
│   │   │   └── ai.controller.js
│   │   ├── routes/
│   │   │   └── ai.routes.js
│   │   ├── services/
│   │   │   └── ai.service.js
│   ├── server.js
│   └── .env
├── frontend/
│   ├── src/
│   │   ├── App.jsx
│   │   └── App.css
│   ├── public/
│   └── package.json
└── readme.md
```

---

## Summary

Code Review AI is a tool designed to make learning and improving coding skills fun and engaging. By providing detailed, constructive feedback, it helps developers write better, cleaner, and more efficient code.

---

## Conclusion

This project demonstrates the power of AI in assisting developers. Whether you're a beginner or an experienced coder, Code Review AI can help you refine your skills and adopt best practices. Contributions and feedback are welcome!

