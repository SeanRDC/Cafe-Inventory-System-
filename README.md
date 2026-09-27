<a id="readme-top"></a>

<!-- PROJECT SHIELDS -->
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h3 align="center">Cafe Inventory System</h3>

  <p align="center">
    A command-line interface (CLI) inventory management system built with Node.js and MongoDB. Designed to manage cafe items, track batches, monitor spoilage in real-time, and generate inventory reports.
    <br />
    <br />
    <strong>Tags:</strong> <code>javascript</code>, <code>node.js</code>, <code>mongodb</code>, <code>cli-app</code>, <code>oop</code>, <code>inventory-management</code>, <code>college-project</code>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#database-access-mongodb-compass">Database Access</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#project-structure">Project Structure</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

This is a 1st-year college project demonstrating Object-Oriented Programming (OOP), database integration, and asynchronous programming in JavaScript. The Cafe Inventory System allows users to easily add items, restock by batches, dynamically check for expiring or spoiled goods using parallel processing, and calculate overall inventory statistics.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

**JavaScript:** The primary programming language used to build the core application logic, asynchronous operations, and object-oriented classes. <br />
**Node.js:** The backend runtime environment used to execute the command-line interface (CLI) and manage the parallel background monitor. <br />
**MongoDB:** The NoSQL cloud database (via MongoDB Atlas) utilized for persisting inventory records, item details, and batch-specific data.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running, follow these steps.

### Prerequisites

* [Node.js](https://nodejs.org/) installed on your machine.
* npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

1. Clone the repository
   ```sh
   git clone https://github.com/your_username/cafe-inventory-system.git
   ```
2. Navigate to the project directory
   ```sh
   cd cafe-inventory-system
   ```
3. Install the required MongoDB driver
   ```sh
   npm install mongodb
   ```

### Database Access (MongoDB Compass)

If you want to view the database visually, you can connect using MongoDB Compass:

1. Open your web browser and go to: [MongoDB Compass Download](https://www.mongodb.com/try/download/compass)
2. Download and install the latest version.
3. Open Compass and click **"Add new connection"**.
4. Paste the following URI provided for the project:
   ```text
   mongodb://cafeUser:cafe123@ac-cnbwmgr-shard-00-00.e1k8bqx.mongodb.net:27017,ac-cnbwmgr-shard-00-01.e1k8bqx.mongodb.net:27017,ac-cnbwmgr-shard-00-02.e1k8bqx.mongodb.net:27017/?ssl=true&replicaSet=atlas-p1q274-shard-0&authSource=admin&appName=CafeInventory
   ```
5. Click **Connect**.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->
## Usage

To launch the application, run the main menu script in your terminal:

```sh
node MainMenu.js
```

From the CLI menu, you can:
* **Add**: Register a new cafe item.
* **Restock**: Add new quantities/batches to existing items.
* **Delete**: Remove a specific batch or entirely delete an item.
* **Show**: Display current inventory with batch tracking and spoilage status.
* **Compute**: Generate a report showing total quantities, restocks, spoiled units, and the overall spoilage rate.

*Note: The system features an automatic parallel checker that actively monitors and alerts you if any item batches spoil while the program is running.*

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- PROJECT STRUCTURE -->
## Project Structure

```text
cafe-inventory-system/
├── CafeInventory.js     # Core logic and database operations for items
├── InventoryItem.js     # OOP Class definition for individual items
├── MainMenu.js          # CLI interface and user input handling
├── ParallelChecker.js   # Background monitor for checking item spoilage
├── db.js                # MongoDB Atlas connection configuration
└── README.txt           # Raw database connection instructions
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>
