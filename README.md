# Simple Card List Application

A web application that displays a list of products in card format with the ability to delete products.

## Features

- **Frontend**: React with Material-UI components
- **Backend**: Node.js with Express.js
- **Product Display**: Cards showing product name, description, price, and image
- **Delete Functionality**: Remove products from the list
- **Responsive Design**: Cards wrap appropriately on different screen sizes
- **Centered Layout**: Container is always centered on the screen
- **Real-time Updates**: Product information persists and is fetched from backend

## Tech Stack

- **Frontend**: React, Material-UI, Axios
- **Backend**: Node.js, Express.js, CORS

## Installation and Setup

### Prerequisites

- Node.js (v16 or higher recommended)
- npm (comes with Node.js)

### 1. Install Dependencies

First, install the backend dependencies:

```bash
cd StarterCode/backend
npm install
```

Then, install the frontend dependencies:

```bash
cd ../frontend
npm install
```

### 2. Start the Backend Server

In a terminal, navigate to the backend directory and start the server:

```bash
cd StarterCode/backend
npm start
```

Or run directly with Node.js:

```bash
cd StarterCode/backend
node index.js
```

The backend will run on `http://localhost:5001`

### 3. Start the Frontend Server

Open a new terminal, navigate to the frontend directory and start the development server:

```bash
cd StarterCode/frontend
npm start
```

The frontend will run on `http://localhost:3000`

### 4. Open the Application

Visit `http://localhost:3000` in your browser. You should see the product list with cards displaying products.

## API Endpoints

### GET /api/products

- Fetches the list of products
- Each product includes a randomly fetched image URL from Picsum
- **URL**: `http://localhost:5001/api/products`

### DELETE /api/products/:id

- Deletes a product by its ID
- Returns success message or 404 if product not found
- **URL**: `http://localhost:5001/api/products/:id`

## Implementation Details

### Backend Features

- ✅ CORS configuration for seamless frontend-backend communication
- ✅ GET endpoint that returns products with random images
- ✅ DELETE endpoint that removes products from the data
- ✅ Proper error handling

### Frontend Features

- ✅ Fetches products from backend API
- ✅ Displays products in Material-UI card format
- ✅ Each card shows: name, description, price, and image
- ✅ Delete icon button on each card
- ✅ Responsive grid layout that wraps appropriately
- ✅ Centered container layout
- ✅ Real-time updates when products are deleted
- ✅ Data persistence (fetched from backend on page refresh)

## Project Structure

```
StarterCode/
├── backend/
│   ├── index.js          # Express server with API endpoints
│   ├── package.json      # Backend dependencies
│   └── package-lock.json
└── frontend/
    ├── src/
    │   ├── App/
    │   │   └── Page/
    │   │       └── ProductList.jsx  # Main product list component
    │   ├── App.js                   # Root component
    │   └── index.js                 # Entry point
    ├── package.json                 # Frontend dependencies
    └── README.md
```

## Usage

1. **Start both servers** (backend first, then frontend)
2. **Open** `http://localhost:3000` in your browser
3. **View** the product cards displayed in a responsive grid
4. **Click** the delete icon on any card to remove it from the list
5. **Refresh** the page to see that the deleted products remain removed (data persists in backend)

## Troubleshooting

### Common Issues

1. **"Cannot find module 'express'" error**

   - Solution: Run `npm install` in the backend directory

2. **"react-scripts: command not found" error**

   - Solution: Run `npm install` in the frontend directory

3. **Port 5000 already in use**

   - The backend is configured to use port 5001 by default
   - If you need to change ports, update both the backend `index.js` and frontend `ProductList.jsx` files

4. **CORS errors**
   - The backend includes CORS configuration, but make sure both servers are running

### Verification Steps

To verify everything is working:

1. **Test Backend API**:

   ```bash
   curl http://localhost:5001/api/products
   ```

   Should return a JSON array of products

2. **Test Frontend**:
   - Open `http://localhost:3000` in browser
   - Should see product cards with images, names, descriptions, and prices
   - Delete buttons should be visible on each card

The application demonstrates a complete full-stack implementation with proper separation of concerns, responsive design, and real-time data management.
