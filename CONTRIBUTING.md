# Contributing to ABC Docusaurus Site

Thank you for your interest in contributing to our documentation site! This guide will help you get started.

## 🚀 Quick Start

1. **Fork the repository** on GitHub
2. **Clone your fork**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/abc-docusaurus-site.git
   cd abc-docusaurus-site
   ```
3. **Install dependencies**:
   ```bash
   npm install
   ```
4. **Start development server**:
   ```bash
   npm start
   ```

## 📝 Making Changes

### 1. Create a Feature Branch
```bash
git checkout -b feature/your-feature-name
```

### 2. Make Your Changes
- Edit documentation in the `docs/` folder
- Add new pages as needed
- Test your changes locally

### 3. Commit Your Changes
```bash
git add .
git commit -m "Add: description of your changes"
```

### 4. Push and Create Pull Request
```bash
git push origin feature/your-feature-name
```
Then create a Pull Request on GitHub.

## 📁 Project Structure

```
├── docs/                    # Documentation files (.md)
├── src/
│   ├── components/         # React components
│   ├── css/               # Custom CSS
│   └── pages/             # Custom pages
├── static/                # Static assets (images, etc.)
├── docusaurus.config.js   # Site configuration
└── sidebars.js           # Sidebar navigation
```

## ✍️ Writing Guidelines

### Documentation Style
- Use clear, concise language
- Include code examples where helpful
- Add screenshots for UI instructions
- Follow the existing document structure

### Commit Messages
- `Add:` for new features/content
- `Fix:` for bug fixes
- `Update:` for content updates
- `Docs:` for documentation changes

### File Naming
- Use kebab-case for file names: `my-new-document.md`
- Place images in appropriate folders under `static/img/`

## 🔍 Review Process

1. **Automatic Checks**: Your PR will be automatically checked
2. **Team Review**: A team member will review your changes
3. **Feedback**: Address any requested changes
4. **Merge**: Once approved, your changes will be merged

## 🆘 Getting Help

- Check existing documentation first
- Search existing issues on GitHub
- Create a new issue if you need help
- Ask questions in pull request comments

## 📋 Checklist Before Submitting

- [ ] Changes tested locally (`npm start`)
- [ ] No broken links or images
- [ ] Follows existing style and structure
- [ ] Commit messages are clear
- [ ] Documentation is up to date

Thank you for contributing! 🎉