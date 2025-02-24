# 🚀 Tech Conference Website
 

A modern, fully responsive tech conference website built using SvelteKit and Sveltestrap.

## 🔗 Live Demo

[View Live Site](https://tech-web-woad.vercel.app/)


## 📂 Project Structure

📦 tech-conference
 ┣ 📂 src
 ┃ ┣ 📂 routes   # Svelte pages
 ┃ ┣ 📂 components  # Reusable UI components
 ┃ ┣ 📂 styles   # Global styles
 ┃ ┗ 📜 app.html   # Main HTML template
 ┣ 📜 package.json  # Dependencies and scripts
 ┣ 📜 svelte.config.js  # SvelteKit configuration
 ┣ 📜 README.md  # Project documentation
┗ 📜 .gitignore  # Files to ignore in version control



## 🛠 Technologies Used

- **SvelteKit** – Frontend framework  
- **Sveltestrap** – Bootstrap components for Svelte  
- **HTML, CSS, JavaScript** – Core web technologies  
- **Vite** – Build tool for fast development  
- **Node.js** – JavaScript runtime  
- **npm** – Package manager  
- **Google Maps API** – Location integration 


## 📦 Installation & Setup

Clone the repository and install dependencies
sh
git clone https://github.com/kavanamalli/tech-conference.git
cd tech-conference
npm install


## 🚀 Running Locally

Start the development server:
npm run dev
Then, open http://localhost:5173 in your browser.

## 🔨 Build for Production
npm run build

Preview the production build:
npm run preview

## 🌍 Deployment
### Vercel (Recommended)
Install Vercel CLI: npm install -g vercel
Deploy: vercel

### Netlify
Connect your GitHub repo to Netlify
Set the build command: npm run build
Publish the build directory

### GitHub Pages (requires adapter-static)
1. Install the static adapter:
npm install @sveltejs/adapter-static

2.Update svelte.config.js:
import adapter from '@sveltejs/adapter-static';
export default {
  kit: { adapter: adapter() }
};

3.Build and preview:
npm run build && npm run preview

4.Deploy to GitHub Pages following GitHub Actions or manual upload.
[
1️⃣ Open VS Code and Initialize Git
Open your project folder in VS Code.
Open the terminal (Ctrl + ~) and run:
sh
git init
git add .
git commit -m "Initial commit"

2️⃣ Connect to GitHub
Go to GitHub → Create a new repository (without a README).
Copy the repo URL and run in VS Code terminal:
sh
git remote add origin https://github.com/your-username/your-repo.git
git branch -M main
git push -u origin main

3️⃣ Install GitHub Pages Adapter
In VS Code terminal, run:
sh
npm install --save-dev @sveltejs/adapter-static

4️⃣ Modify svelte.config.js
Edit your svelte.config.js:
import adapter from '@sveltejs/adapter-auto';

/** @type {import('@sveltejs/kit').Config} */
const config = {
	kit: {
		// adapter-auto only supports some environments, see https://svelte.dev/docs/kit/adapter-auto for a list.
		// If your environment is not supported, or you settled on a specific environment, switch out the adapter.
		// See https://svelte.dev/docs/kit/adapters for more information about adapters.
		adapter: adapter()
	}
};

export default config;

5️⃣ Build and Push Again
Run:
sh
npm run build
git add .
git commit -m "Build for deployment"
git push origin main

6️⃣ Enable GitHub Pages
Go to GitHub Repo → Settings → Pages
Under Branch, select main, set /build as the folder
Click Save]

## 🤝 Contribution
Kavana B M

## 📄 License
This project is licensed under the MIT License.



