# Blogging App

This is a blogging application built with the following tech stack:

- *Frontend*: React
- *Backend*: Cloudflare Workers
- *Validation*: Zod
- *Language*: TypeScript
- *ORM*: Prisma
- *Database*: PostgreSQL
- *Authentication*: JWT (using cookies)

## Features

- User authentication with JWT tokens stored in cookies
- Full CRUD (Create, Read, Update, Delete) functionality for blog posts
- Type-safe API with Zod for input validation
- Real-time updates and efficient data fetching
- Connection pooling with Prisma and PostgreSQL for optimized database performance

## Tech Stack

### Frontend

- *React*: The UI is built with React, allowing users to interact with the app efficiently and dynamically.
- *TypeScript*: Provides static typing to ensure reliable and scalable code.

### Backend

- *Cloudflare Workers*: Serverless functions running at the edge, providing fast and scalable backend services.
- *Prisma ORM*: Used to interact with the PostgreSQL database, providing an easy-to-use and type-safe interface for database operations.
- *PostgreSQL*: A relational database used to store blog data, user accounts, and other application data.
  
### Authentication

- *JWT Authentication*: JSON Web Tokens (JWT) are used to authenticate users. The tokens are stored in cookies for secure, persistent sessions.
  
  ### Cookie Authentication Flow
  1. Upon successful login, a JWT is generated on the server and sent as an HTTP-only cookie to the client.
  2. On subsequent requests, the JWT is automatically sent by the browser in the cookie header, allowing the server to authenticate the user.
  3. The JWT is verified on the backend with Cloudflare Workers, ensuring that only authenticated users can access protected routes.

### Validation

- *Zod*: Zod is used for schema validation in both the frontend and backend. It provides a seamless way to ensure the integrity and correctness of data passed between the client and server.
  
## Setup and Installation

### Prerequisites

- Node.js (version >=14)
- PostgreSQL installed and running locally or a PostgreSQL cloud service like Heroku or ElephantSQL.
- Cloudflare Workers account setup.

### Backend Setup

1. Install Cloudflare Workers CLI:
   bash
   npm install -g wrangler
   

2. Clone the repository:
   bash
   git clone https://github.com/your-repo/blogging-app.git
   cd blogging-app
   

3. Install backend dependencies:
   bash
   npm install
   

4. Set up environment variables for the database connection:
   Create a .env file in the root directory and add the following:
   bash
   DATABASE_URL=your_postgresql_database_url
   JWT_SECRET=your_jwt_secret_key
   

5. Deploy Cloudflare Worker:
   bash
   wrangler publish
   

### Frontend Setup

1. Navigate to the frontend directory:
   bash
   cd frontend
   

2. Install frontend dependencies:
   bash
   npm install
   

3. Start the development server:
   bash
   npm run dev
   

### Database Setup

1. Make sure PostgreSQL is running and accessible.
2. Use Prisma to create and migrate the database schema:
   bash
   npx prisma migrate dev
   

### Running the App

1. Start the backend and frontend services as mentioned in the setup.
2. Open the app in your browser (typically http://localhost:3000 for the frontend).

## Contributing

1. Fork the repository.
2. Create a new branch for your feature.
3. Make your changes and commit them.
4. Push your changes to your fork.
5. Open a pull request.

## License

This project is licensed under the MIT License.
