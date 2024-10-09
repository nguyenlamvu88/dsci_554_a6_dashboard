
# DSCI 554 Data Visualization Dashboard - Step-by-Step Beginner's Guide

This project is a data visualization dashboard built using React, D3.js, and Bootstrap. It was developed as part of the DSCI 554 course assignment. The dashboard displays comparative data visualizations for different datasets and has been deployed using GitHub Pages.

## Table of Contents
- [Project Setup](#project-setup)
- [Development](#development)
- [Deployment](#deployment)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)

## Project Setup

### Prerequisites

Make sure you have the following installed on your local machine:
- [Node.js](https://nodejs.org/) (v14 or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- Basic understanding of using terminal/command prompt.

### Step-by-Step Setup Instructions

Follow these steps to set up your project environment from scratch:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/nguyenlamvu88/dsci_554_a6_dashboard.git
   ```

2. **Navigate into the project directory:**
   ```bash
   cd dsci_554_a6_dashboard
   ```

3. **Install the project dependencies:**
   ```bash
   npm install
   ```
   This command installs all the necessary packages and dependencies listed in `package.json`.

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

### Installation of Required Loaders and Plugins

To ensure everything works correctly, install the necessary loaders and plugins:
```bash
npm install webpack webpack-cli webpack-dev-server babel-loader @babel/core @babel/preset-env @babel/preset-react html-webpack-plugin style-loader css-loader html-loader gh-pages --save-dev
```

## Development

### Running the Development Server

To start the development server and view the dashboard locally:
```bash
npm start
```
Open your browser and go to `http://localhost:3000` to view the dashboard.

This command will start the Webpack dev server, allowing you to make changes to your code and see the updates in real-time.

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

## Project Structure
```
├── node_modules
├── public
│   └── index.html
├── src
│   ├── components
│   │   ├── Visualization1.js
│   │   ├── Visualization2.js
│   │   └── ...
│   ├── index.css
│   └── index.js
├── .babelrc
├── .gitignore
├── package.json
├── package-lock.json
├── webpack.config.js
└── README.md
```

## Technologies Used
- **React** - Front-end JavaScript library for building user interfaces.
- **D3.js** - Library for creating dynamic and interactive data visualizations.
- **Bootstrap** - CSS framework for building responsive layouts.
- **Webpack** - Module bundler for packaging JavaScript and assets.
- **Babel** - JavaScript compiler for using the latest JavaScript features.
- **GitHub Pages** - Service for hosting static websites directly from a GitHub repository.
