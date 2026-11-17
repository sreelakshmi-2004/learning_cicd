# My DevOps Learning Journey - Website

A clean, responsive, and modern static portfolio website built using **HTML5**, **CSS3**, and **Vanilla JavaScript**. Designed with a light lavender and white aesthetic.

---

## 🚀 Features

- **Home Section**: Welcoming hero banner with title, summary, and action links.
- **About Section**: Concise introduction to DevOps philosophy, learning journey, and key focus areas.
- **Skills Section**: Highlights core DevOps tools:
  - Linux
  - Git
  - GitHub
  - AWS
  - Docker
  - Jenkins
  - Ansible
  - Terraform
- **Projects Section**: 3 practical DevOps project cards (CI/CD Pipeline, AWS IaC with Terraform, Ansible Automation).
- **Contact Section**: Simple, accessible Email and GitHub links.
- **Modern & Responsive Design**:
  - Light lavender (`#f8f6fc`) and crisp white (`#ffffff`) palette.
  - Subtle micro-interactions and hover effects.
  - Mobile-friendly responsive navigation menu.
  - Zero external frameworks or heavy libraries.

---

## 📁 Project Structure

```
portfolio/
├── index.html       # Semantic HTML5 structure
├── style.css        # Clean CSS3 with CSS variables and responsive rules
├── script.js        # Vanilla JavaScript (nav toggle, active spy, dynamic year)
├── Jenkinsfile      # Declarative CI/CD pipeline definition for Jenkins
└── README.md        # Documentation and deployment instructions
```

---

## 💻 Local Preview

Simply open `index.html` in any web browser:

- Double-click `index.html`, or
- Use VS Code Live Server, or
- Run a simple Python server:
  ```bash
  python -m http.server 8000
  ```
  Then visit `http://localhost:8000`.

---

## 🌐 Git & GitHub Setup

1. Initialize git and commit:
   ```bash
   git init
   git add .
   git commit -m "feat: Initial commit for My DevOps Journey website"
   ```
2. Link your remote GitHub repository:
   ```bash
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo-name>.git
   git push -u origin main
   ```

---

## 🤖 Jenkins CI/CD Pipeline Deployment

The repository includes a declarative `Jenkinsfile`.

1. In Jenkins, create a **New Item** &rarr; Select **Pipeline**.
2. Under **Pipeline Definition**, select **Pipeline script from SCM**.
3. Choose **Git** and enter your repository URL.
4. Set the script path to `Jenkinsfile`.
5. Run **Build Now** to execute the pipeline.
