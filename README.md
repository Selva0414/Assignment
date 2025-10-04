# Book Review Backend

Simple Express + MongoDB backend for the Book Review assignment.

Set environment variables in a `.env` file (example provided in `.env.example`).

Install dependencies:

  npm install


Run locally:

  npm run dev

By default the server listens on port 4023 (or set PORT in your `.env`).

Using MongoDB Compass / Local MongoDB
- The project defaults to a local MongoDB URI: `mongodb://127.0.0.1:27017/book_review_app` when `MONGO_URI` isn't provided.
- To use MongoDB Compass, start a local `mongod` (or run the MongoDB service) and then open Compass and connect to:

  mongodb://127.0.0.1:27017

  Then open the `book_review_app` database (it will appear after the app creates documents).

API endpoints:
- POST /api/auth/signup
- POST /api/auth/login
- GET /api/books?page=1
- GET /api/books/:id
- POST /api/books (protected)
- PUT /api/books/:id (protected, owner only)
- DELETE /api/books/:id (protected, owner only)
- POST /api/reviews (protected)
- PUT /api/reviews/:id (protected, owner only)
- DELETE /api/reviews/:id (protected, owner only)
- GET /api/reviews/book/:bookId
