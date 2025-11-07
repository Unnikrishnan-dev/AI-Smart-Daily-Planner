
---

## Tech Stack Overview

| Layer | Technology | Description |
|--------|-------------|-------------|
| **Frontend** | Angular | SPA for UI and user interaction |
| **Backend** | Express.js (Node.js) | RESTful API server |
| **Database** | MongoDB | NoSQL database for data storage |

---


```bash
AI smart Planner/                    # Root project folder
├── backend/                         # Node.js / Express REST API
│   ├── config/                      # Database & environment configuration
│   │   └── db.js                    # MongoDB connection setup
│   ├── controllers/                 # Business logic and request handling
│   │   ├── userController.js
│   │   ├── taskController.js
│   ├── models/                      # Mongoose schemas (MongoDB models)
│   │   ├── userModel.js
│   │   ├── taskModel.js
│   ├── routes/                      # API endpoints
│   │   ├── userRoutes.js
│   │   ├── taskRoutes.js
│   ├── utils/                       # Helper functions or services
│   ├── server.js                    # Express app entry point
│   └── package.json                 # Backend dependencies
│
├── frontend/                        # Angular application
│   ├── src/
│   │   ├── app/                     # Main Angular app folder
│   │   │   ├── layout/              # Layouts like sidebar, header, footer
│   │   │   ├── pages/               # Application pages (views)
│   │   │   ├── services/            # API and data services
│   │   │   ├── guards/              # Route guards (auth protection)
│   │   │   ├── interceptors/        # HTTP interceptors (token injection, errors)
│   │   │   └── app.module.ts        # Root module
│   │   ├── assets/                  # Static assets (images, styles, etc.)
│   │   ├── environments/            # Environment configs (dev/prod)
│   │   │   ├── environment.ts
│   │   │   └── environment.prod.ts
│   │   └── main.ts                  # Angular app entry point
│   ├── angular.json                 # Angular project config
│   └── package.json                 # Frontend dependencies
│
└──README.md                        # Project documentation
```

Example code Snippet of the above architecure in server.js <br>

```json
// Server.js
const express = require("express");
const dotenv = require("dotenv");
const connectDB = require("./config/db");
const userRoutes = require("./routes/userRoutes");

dotenv.config();
connectDB();

const app = express();
app.use(express.json());

app.get("/", (req, res) => {
  res.send("API is running...");
});

app.use("/api/users", userRoutes);

const PORT = process.env.PORT || 5000;
app.listen(PORT, () => console.log(`🚀 Server running on port ${PORT}`));


```

