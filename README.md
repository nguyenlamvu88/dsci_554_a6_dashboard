
# DSCI 554 Dashboard Project Setup

This README provides a detailed guide for setting up, building, and deploying a React-based dashboard project using Webpack and GitHub Pages.

## Prerequisites

Ensure you have the following installed:
- Node.js (https://nodejs.org/)
- npm (Node package manager, which comes with Node.js)

## Project Setup Steps

1. **Clone the repository**: 
   ```bash
   git clone https://github.com/nguyenlamvu88/dsci_554_a6_dashboard.git
   cd dsci_554_a6_dashboard
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

## Project Structure

- `/public`: Contains the `index.html` file.
- `/src`: Contains React components and other source files.
- `/src/components`: Contains the JavaScript files converted from HTML visualizations.

## Development

### Creating React Components

- If you have HTML files for visualizations, convert each visualization into a React component and place them in the `/src/components` directory.

### Webpack Configuration

- Ensure your `webpack.config.js` is set up properly to bundle JavaScript files and handle styles.
- Key configuration includes setting the entry point, output file, loaders for CSS and JS, and plugins for HTML generation.

## Build and Deploy

### Build the Project

Run the following command to bundle your application:
```bash
npm run build
```

### Deploy to GitHub Pages

1. Ensure the `homepage` field in `package.json` is set to your repository's URL.
2. Deploy the project to GitHub Pages:
   ```bash
   npm run deploy
   ```

## Viewing the Dashboard

After deployment, you can view the dashboard at:
- `https://<your-username>.github.io/dsci_554_a6_dashboard`

Replace `<your-username>` with your GitHub username.

## Additional Notes

- **React and Webpack Integration**: The project integrates React with Webpack for modular and efficient builds.
- **Deployment**: Uses `gh-pages` to deploy the built project to GitHub Pages.
- **Customization**: You can modify the components inside `/src/components` to suit your data visualization needs.

## Troubleshooting

- Ensure that all dependencies are correctly installed with `npm install`.
- If you encounter issues with the build, try clearing the npm cache and reinstalling the modules:
   ```bash
   npm cache clean --force
   npm install
   ```

- For errors related to `webpack` or missing loaders, install them as follows:
   ```bash
   npm install style-loader css-loader html-loader --save-dev
   ```

## License

This project is licensed under the MIT License.
