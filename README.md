## How to Run the Application

### Prerequisites

- Node.js (v16 or higher recommended)
- npm (comes with Node.js)

### 1. Install Dependencies

From the root of the project, run:

```bash
cd StarterCode/backend
npm install
cd ../frontend
npm install
```

### 2. Start the Backend

In a terminal, run:

```bash
cd StarterCode/backend
node index.js
```

The backend will start on [http://localhost:5001](http://localhost:5001)

### 3. Start the Frontend

Open a new terminal and run:

```bash
cd StarterCode/frontend
npm start
```

The frontend will start on [http://localhost:3001](http://localhost:3001)

### 4. Open the App

Visit [http://localhost:3001](http://localhost:3001) in your browser. You should see the product list UI.

---

**Note:**

- The backend must be running before the frontend for the app to work correctly.
- If you change ports, update the API URL in `StarterCode/frontend/src/App/Page/ProductList.jsx` accordingly.
