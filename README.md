
# DSCI 554 Data Visualization Dashboard

This project is a data visualization dashboard built using React, D3.js, and Bootstrap. It was developed as part of the DSCI 554 course assignment. The dashboard displays comparative data visualizations for different datasets and has been deployed using GitHub Pages.

## Table of Contents
- [Project Setup](#project-setup)
- [Development](#development)
- [Deployment](#deployment)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)

## Project Setup

To get started with this project, you'll need to follow these setup instructions:

### Prerequisites

Make sure you have the following installed on your local machine:
- [Node.js](https://nodejs.org/) (v14 or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### Installation

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
   This command installs all the necessary packages and dependencies listed in package.json.

### Configuration
No additional configuration is required for this project.

## Development
To start the development server and view the dashboard locally:

1. **Run the development server:**
   ```bash
   npm start
   ```
   
2. Open your browser and go to [http://localhost:3000](http://localhost:3000) to view the dashboard.

This command will start the Webpack dev server, allowing you to make changes to your code and see the updates in real-time.

## Deployment
The project is configured to deploy to GitHub Pages automatically using the gh-pages package.

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

Your dashboard will be deployed to GitHub Pages and can be accessed at: [https://nguyenlamvu88.github.io/dsci_554_a6_dashboard/](https://nguyenlamvu88.github.io/dsci_554_a6_dashboard/)

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

- **public/index.html** - The main HTML file.
- **src/index.js** - Entry point for the React app.
- **src/components/** - Contains individual visualization components.
- **webpack.config.js** - Webpack configuration file for building the project.
- **.babelrc** - Babel configuration file for transpiling JSX and ES6+ code.

## Technologies Used
- **React** - Front-end JavaScript library for building user interfaces.
- **D3.js** - Library for creating dynamic and interactive data visualizations.
- **Bootstrap** - CSS framework for building responsive layouts.
- **Webpack** - Module bundler for packaging JavaScript and assets.
- **Babel** - JavaScript compiler for using the latest JavaScript features.
- **GitHub Pages** - Service for hosting static websites directly from a GitHub repository.
