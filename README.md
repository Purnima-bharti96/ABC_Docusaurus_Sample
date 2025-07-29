# Website

This website is built using [Docusaurus](https://docusaurus.io/), a modern static website generator.

## 🚀 Quick Start

### Prerequisites
- Node.js (version 18 or higher)
- npm or yarn package manager
- Git

### Team Setup
1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd <project-name>
   ```

2. **Install dependencies**:
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Start development server**:
   ```bash
   npm start
   # or
   yarn start
   ```

4. **Open your browser**:
   Navigate to `http://localhost:3000`

## Installation

```bash
yarn
```

## Local Development

```bash
yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

## Build

```bash
yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

## Deployment

Using SSH:

```bash
USE_SSH=true yarn deploy
```

Not using SSH:

```bash
GIT_USER=<Your GitHub username> yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.

## 🤝 Contributing

### Development Workflow
1. **Create a feature branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes** and test locally

3. **Commit your changes**:
   ```bash
   git add .
   git commit -m "Add: description of your changes"
   ```

4. **Push to repository**:
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Create a Pull Request** on GitHub/GitLab

### Commit Message Guidelines
- `Add:` for new features
- `Fix:` for bug fixes
- `Update:` for content updates
- `Docs:` for documentation changes

## 📁 Project Structure

```
├── docs/                    # Documentation files
├── src/
│   ├── components/         # React components
│   ├── css/               # Custom CSS
│   └── pages/             # Custom pages
├── static/                # Static assets
├── docusaurus.config.js   # Docusaurus configuration
└── sidebars.js           # Sidebar configuration
```

## 🛠️ Available Scripts

- `npm start` - Start development server
- `npm run build` - Build for production
- `npm run serve` - Serve production build locally
- `npm run clear` - Clear Docusaurus cache

## 📝 Adding Content

### Adding New Documentation
1. Create a new `.md` file in the `docs/` directory
2. Add frontmatter with `sidebar_position`
3. The file will automatically appear in the sidebar

### Editing Existing Content
- Edit `.md` files in the `docs/` directory
- Changes will be reflected immediately in development mode

## 🎨 Customization

- **Colors**: Edit `src/css/custom.css`
- **Logo**: Replace files in `static/img/`
- **Site Config**: Edit `docusaurus.config.js`
- **Navigation**: Edit `docusaurus.config.js` navbar section

## 🚀 Deployment

The site can be deployed to various platforms:
- GitHub Pages
- Netlify
- Vercel
- AWS S3

## 📞 Support

If you encounter any issues:
1. Check the [Docusaurus documentation](https://docusaurus.io/docs)
2. Search existing issues in the repository
3. Create a new issue with detailed information

## 📄 License

This project is licensed under the MIT License.