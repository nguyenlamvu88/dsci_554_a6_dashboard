# DSCI 554 Data Visualization Dashboard - Step-by-Step Beginner's Guide

This project is a data visualization dashboard built using React, D3.js, and Bootstrap. It was developed as part of the DSCI 554 course assignment. The dashboard displays comparative data visualizations for different datasets and has been deployed using GitHub Pages.

## Table of Contents
- [Project Setup](#project-setup)
- [Deployment](#deployment)
- [Development](#development)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)

## Project Setup

### Step-by-Step Setup Instructions

Follow these steps to set up your project environment from scratch:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/DSCI-554/a6-nguyenlamvu88.git
   ```

2. **Navigate into the project directory:**
   ```bash
   cd a6-nguyenlamvu88
   ```

3. **Install the project dependencies:**
   ```bash
   npm install
   ```
   This command installs all the necessary packages and dependencies listed in `package.json`.

### Installation of Required Loaders and Plugins

To ensure everything works correctly, install the necessary loaders and plugins:
```bash
npm install webpack webpack-cli webpack-dev-server babel-loader @babel/core @babel/preset-env @babel/preset-react html-webpack-plugin style-loader css-loader html-loader gh-pages --save-dev
```

### Creating Configuration Files

#### 1. **Create `webpack.config.js`**

Create a file named `webpack.config.js` in the root of your project directory with the following content:
```javascript
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
  entry: './src/index.js',
  output: {
    path: path.resolve(__dirname, 'build'),
    filename: 'bundle.js',
  },
  module: {
    rules: [
      {
        test: /\.(js|jsx)$/,
        exclude: /node_modules/,
        use: {
          loader: 'babel-loader',
        },
      },
      {
        test: /\.css$/i,
        use: ['style-loader', 'css-loader'],
      },
      {
        test: /\.html$/,
        use: [
          {
            loader: 'html-loader',
          },
        ],
      },
    ],
  },
  resolve: {
    extensions: ['.js', '.jsx'],
  },
  plugins: [
    new HtmlWebpackPlugin({
      template: './public/index.html',
      filename: './index.html',
    }),
  ],
  devServer: {
    static: {
      directory: path.join(__dirname, 'build'),
    },
    compress: true,
    port: 3000,
  },
};
```

#### 2. **Create `.babelrc` File**

Create a `.babelrc` file in the root of your project directory with the following content:
```json
{
  "presets": ["@babel/preset-env", "@babel/preset-react"]
}
```

#### 3. **Update `package.json`**

Open the `package.json` file in your project and make sure it has the following `scripts` section to enable building and deploying the project:
```json
"scripts": {
  "start": "webpack serve --mode development",
  "build": "webpack --mode production",
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}
```

## Deployment

### Deployment Steps

To deploy the latest version of your project to GitHub Pages, follow these steps:

1. **Build the project:**
   ```bash
   npm run build
   ```

2. **Deploy to GitHub Pages:**
   ```bash
   npm run deploy
   ```

After running this command, your dashboard will be deployed to GitHub Pages. Once the deployment is complete, you can access your live dashboard at the following URL:

`https://nguyenlamvu88.github.io/dsci_554_a6_dashboard/`

### Running the Development Server

To start the development server and view the dashboard locally:
```bash
npm start
```
Open your browser and go to `http://localhost:3000` to view the dashboard.

This command will start the Webpack dev server, allowing you to make changes to your code and see the updates in real-time.

## Project Structure
```plaintext
a6-nguyenlamvu88
├── .github
├── build
├── node_modules
├── public
│   └── index.html
├── src
│   ├── components
│   │   ├── GDPGrowthChart.js
│   │   ├── HealthExpenditureChart.js
│   │   ├── ImportExportChart.js
│   │   ├── KPI.js
│   │   ├── LifeExpectancyChart.js
│   │   └── PopulationDemographicsChart.js
│   ├── index.css
│   └── index.js
├── .babelrc
├── .gitignore
├── ASSIGNMENT.md
├── index.html
├── package-lock.json
├── package.json
├── README.md
└── webpack.config.js
```

## Technologies Used
- **React** - Front-end JavaScript library for building user interfaces.
- **D3.js** - Library for creating dynamic and interactive data visualizations.
- **Bootstrap** - CSS framework for building responsive layouts.
- **Webpack** - Module bundler for packaging JavaScript and assets.
- **Babel** - JavaScript compiler for using the latest JavaScript features.
- **GitHub Pages** - Service for hosting static websites directly from a GitHub repository.