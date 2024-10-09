
# DSCI 554 Data Visualization Dashboard

This project is a data visualization dashboard built using React, D3.js, and Bootstrap. It was developed as part of the DSCI 554 course assignment. The dashboard displays comparative data visualizations for different datasets and has been deployed using GitHub Pages.

## Table of Contents
- [Project Setup](#project-setup)
- [Development](#development)
- [Deployment](#deployment)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)

## Project Setup

### Prerequisites

Before you begin, make sure you have the following software installed on your local machine:
1. **Node.js**: Download and install Node.js from [https://nodejs.org/](https://nodejs.org/). Make sure you install the LTS version, which comes with npm (Node Package Manager).
   - To verify if Node.js and npm are installed, open your terminal or command prompt and run:
     ```bash
     node -v
     npm -v
     ```
   - You should see version numbers for both if they are correctly installed.

2. **Git**: Download and install Git from [https://git-scm.com/](https://git-scm.com/). This will allow you to clone the project repository.
   - To verify if Git is installed, open your terminal or command prompt and run:
     ```bash
     git --version
     ```

### Installation

Follow these steps to set up the project:

1. **Clone the repository to your local machine:**
   - Open your terminal or command prompt.
   - Run the following command to clone the project repository:
     ```bash
     git clone https://github.com/nguyenlamvu88/dsci_554_a6_dashboard.git
     ```

2. **Navigate into the project directory:**
   - Change into the project's directory by running:
     ```bash
     cd dsci_554_a6_dashboard
     ```

3. **Install the project dependencies:**
   - Run the following command to install all the necessary packages and dependencies:
     ```bash
     npm install
     ```
   - This command installs all the packages specified in the `package.json` file, including React, D3.js, Bootstrap, and others.

## Development

### Running the Development Server

To run the project on your local machine, follow these steps:

1. **Start the development server:**
   - Run the following command to start the Webpack development server:
     ```bash
     npm start
     ```
   - This command will automatically open your default web browser and navigate to `http://localhost:3000`. This is where you can view your dashboard locally.

2. **Making Changes:**
   - Any changes you make to the code will automatically be reflected in the browser without restarting the server, thanks to hot-reloading.

## Deployment

### Deploying to GitHub Pages

The project is configured to be easily deployed to GitHub Pages. Follow these steps to publish your dashboard:

1. **Build the project for production:**
   - Run the following command to generate a production build of your dashboard:
     ```bash
     npm run build
     ```

2. **Deploy to GitHub Pages:**
   - Run the following command to deploy your project to GitHub Pages:
     ```bash
     npm run deploy
     ```
   - Your dashboard will be published to GitHub Pages. You can access it at the URL:
     ```
     https://nguyenlamvu88.github.io/dsci_554_a6_dashboard/
     ```

## Project Structure

Below is an overview of the project's file structure:

```
├── node_modules
├── public
│   └── index.html         # The main HTML file.
├── src
│   ├── components         # Contains individual visualization components.
│   │   ├── Visualization1.js
│   │   ├── Visualization2.js
│   │   └── ...
│   ├── index.css          # CSS file for styling.
│   └── index.js           # Entry point for the React app.
├── .babelrc               # Babel configuration file.
├── .gitignore             # Git ignore file.
├── package.json           # Project's dependencies and scripts.
├── package-lock.json      # Lock file for installed npm dependencies.
├── webpack.config.js      # Webpack configuration for bundling.
└── README.md              # Project documentation.
```

## Technologies Used

This project utilizes the following technologies:

- **React**: Front-end JavaScript library for building user interfaces.
- **D3.js**: Library for creating dynamic and interactive data visualizations.
- **Bootstrap**: CSS framework for building responsive layouts.
- **Webpack**: Module bundler for packaging JavaScript and assets.
- **Babel**: JavaScript compiler for using the latest JavaScript features.
- **GitHub Pages**: Service for hosting static websites directly from a GitHub repository.

## Additional Notes

- Make sure to keep your `package.json` file updated with the latest dependencies.
- Regularly check for updates to your dependencies using the command:
  ```bash
  npm update
  ```
