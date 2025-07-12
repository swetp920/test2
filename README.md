# 🚀 React Portfolio Project Viewer

A clean, responsive front-end React project to showcase GitHub repositories using modern tools like TailwindCSS, shadcn/ui, and lucide-react. Ideal for portfolio displays, personal GitHub homepages, and professional profiles.

---

## 🧠 Why This Project?

As a front-end developer with over 15 years of experience, I (Swet Prakash) wanted to create something that:

- Shows off projects in a professional way
- Uses modern React + Tailwind stack
- Is super easy for others to copy and run

---

## 🔧 Tech Used

- ⚛️ React (Vite)
- 💨 TailwindCSS
- 🧩 shadcn/ui (component library)
- 🎯 lucide-react (icons)
- 🧠 Clean & modular code

---

## 📂 Setup Instructions

### 1. 🧱 Create the Project with Vite

bash
npm create vite@latest react-portfolio-viewer -- --template react
cd react-portfolio-viewer
npm install

2. 🎨 Install Styling Libraries
bash
Copy
Edit
npm install lucide-react
npx shadcn-ui@latest init
npx shadcn-ui@latest add card button
3. ✏️ Replace Code in src/App.jsx
jsx
Copy
Edit
import PortfolioViewer from './PortfolioViewer';

function App() {
  return <PortfolioViewer />;
}

export default App;
4. 💻 Create src/PortfolioViewer.jsx and Paste This Code
jsx
Copy
Edit
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Github } from "lucide-react";

const projects = [
  {
    title: "DevDashboard",
    description:
      "A professional developer dashboard with task tracking, GitHub integration, and productivity stats.",
    link: "https://github.com/swetp920/devdashboard",
  },
  {
    title: "ReactUI-Kit",
    description:
      "A sleek and reusable front-end component library built with TailwindCSS and ShadCN.",
    link: "https://github.com/swetp920/reactui-kit",
  },
  {
    title: "API Visualizer",
    description:
      "Visual tool for REST API endpoints. See responses, test queries, and debug easily.",
    link: "https://github.com/swetp920/api-visualizer",
  },
];

export default function PortfolioViewer() {
  return (
    <main className="min-h-screen bg-gray-100 py-10 px-4 md:px-20">
      <h1 className="text-4xl font-bold mb-8 text-center text-gray-800">
        📁 My GitHub Projects
      </h1>
      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        {projects.map((project, index) => (
          <Card key={index} className="rounded-2xl shadow-md p-4">
            <CardContent>
              <h2 className="text-xl font-semibold mb-2">{project.title}</h2>
              <p className="text-gray-600 mb-4">{project.description}</p>
              <Button
                variant="outline"
                className="w-full flex items-center justify-center gap-2"
                onClick={() => window.open(project.link, "_blank")}
              >
                <Github className="h-4 w-4" /> View on GitHub
              </Button>
            </CardContent>
          </Card>
        ))}
      </div>
    </main>
  );
}
5. ▶️ Start the Dev Server
bash
Copy
Edit
npm run dev
Open http://localhost:5173 in your browser!

🧑‍💻 Author: Swet Prakash
Software Dev | Software Engineer  
📍 GitHub Profile → swetp920

💫 Like this project?
Give it a ⭐️ or share it. Fork it. Build your own version. Use it in your portfolio.

yaml
Copy
Edit

---

### ✅ Want Me to:

- Add Dark Mode?
- Add Search/Filter to projects?
- Deploy to Vercel and generate live link?

Just say the word, Swet 💻💘
