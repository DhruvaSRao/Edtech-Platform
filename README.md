# StudyNotion Edtech Project

StudyNotion is a fully functional MERN-stack based Ed-Tech platform that enables users to create, consume, and rate educational content.
It provides an interactive learning experience for students and a platform for instructors to showcase their expertise globally.

Features

🎓 For Students:
1. Browse and enroll in courses
2. View course content (videos, notes, PDFs)
3. Wishlist and cart functionality
4. Rate and review courses
5. Manage personal profile and course history

🧑‍🏫 For Instructors

1. Create, update, and delete courses
2. Manage course content and pricing
3. View student feedback and insights
4. Dashboard analytics for engagement tracking

🛠️ For Admin (Future Scope)

1. Manage instructors, students, and courses
2. Monitor platform analytics (users, revenue, etc.)
3. Approve or remove courses

System Architecture:

The platform follows a client–server architecture:

Front-End: ReactJS

Back-End: Node.js + Express.js

Database: MongoDB (NoSQL)

Media Management: Cloudinary

Hosting:
Front-end → Vercel
Back-end → Render/Railway

Database → MongoDB Atlas

Tech Stack:

Layer	Technology Used
Front-End:	ReactJS, Redux, Tailwind CSS
Back-End:	NodeJS, ExpressJS
Database:	MongoDB, Mongoose
Authentication:	JWT, Bcrypt
Media Handling:	Cloudinary
Payments:	Razorpay Integration
Deployment:	Vercel (frontend), Render/Railway (backend), MongoDB Atlas (database).

Structure of the Project:

```
STUDYNOTION-EDTECH-PROJECT-MAIN/
│
├── build/                                  # Production build files (auto-generated)
│
├── node_modules/                           # Installed dependencies (auto-generated)
│
├── public/                                 # Static frontend assets (HTML, icons, etc.)
│
├── server/                                 # Backend source code (Node.js + Express)
│   ├── config/
│   │   └── cloudinary.js                   # Cloudinary configuration for media uploads
│   │   └── dbConfig.js                     # (Optional) MongoDB connection configuration
│   │
│   ├── controllers/                        # Request handlers for backend routes
│   │   └── Auth.js                         # Handles user authentication (login, signup)
│   │   └── RatingAndReview.js              # Handles course ratings & reviews
│   │   └── Course.js                       # CRUD operations for courses
│   │
│   ├── models/                             # MongoDB schemas
│   │   └── User.js                         # User schema (students & instructors)
│   │   └── Course.js                       # Course schema (details, pricing, instructor)
│   │   └── RatingAndReview.js              # Stores ratings and comments for courses
│   │
│   ├── routes/                             # Express route definitions
│   │   └── authRoutes.js                   # Authentication routes
│   │   └── courseRoutes.js                 # Course CRUD routes
│   │   └── reviewRoutes.js                 # Rating & review routes
│   │
│   ├── middleware/                         # Middleware for request validation & auth
│   │   └── authMiddleware.js               # Verifies JWT and user permissions
│   │
│   ├── utils/                              # Utility functions
│   │   └── mailSender.js                   # Sends verification & reset password emails
│   │
│   └── index.js                            # Entry point for the backend server
│
├── src/                                    # Frontend (React) source code
│   ├── App.js                              # Root React component
│   ├── components/                         # Reusable React UI components
│   │   └── Navbar.jsx                      # Navigation bar for app
│   │   └── Footer.jsx                      # Footer section
│   │   └── CourseCard.jsx                  # Component displaying course info
│   │
│   ├── pages/                              # Main pages (routed via React Router)
│   │   └── Home.jsx                        # Landing page
│   │   └── CoursePage.jsx                  # Course listing and details page
│   │   └── Dashboard.jsx                   # Student/Instructor dashboard
│   │   └── Login.jsx                       # Login form
│   │   └── Signup.jsx                      # Registration form
│   │
│   ├── assets/                             # Static images, icons, styles
│   ├── styles/                             # Tailwind & CSS files
│   └── index.js                            # Frontend entry point (ReactDOM.render)
│
├── .env                                    # Environment variables (API keys, DB URIs, secrets)
├── .gitignore                              # Files & folders ignored by Git
├── package.json                            # Backend dependencies & scripts
├── package-lock.json                       # Dependency lock file
├── README.md                               # Project documentation
├── prettier.config.js                      # Prettier configuration for consistent code style
├── tailwind.config.js                      # Tailwind CSS configuration
└── .editorconfig                           # Code editor configuration for uniform formatting
```

You can check it out here: 
https://edtech-platform-frontend-rho.vercel.app/

