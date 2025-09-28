# Blogging Platform

A full-stack blogging application built with React.js and Node.js featuring rich-text editing, authentication, and modern UI.

## Features

- ✅ User authentication (JWT)
- ✅ Create, edit, delete blog posts
- ✅ Rich-text editor (React Quill)
- ✅ Responsive design with Tailwind CSS
- ✅ Toast notifications (Sonner)
- ✅ Redux state management
- 🔄 Image upload (Cloudinary integration ready)
- 🔄 Comments system
- 🔄 Likes functionality
- 🔄 Search and filtering
- 🔄 Admin dashboard

## Tech Stack

**Frontend:**
- React.js with Vite
- Redux Toolkit
- React Router
- React Quill
- Tailwind CSS
- Sonner (toasts)
- Axios

**Backend:**
- Node.js + Express
- MongoDB + Mongoose
- JWT authentication
- bcryptjs
- CORS

## Project Structure

```
blogging_web/
├── Frontend/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Page components
│   │   ├── features/       # Redux slices
│   │   ├── store/          # Redux store
│   │   └── utils/          # API utilities
│   └── package.json
├── server/                 # Node.js backend
│   ├── src/
│   │   ├── controllers/    # Route handlers
│   │   ├── models/         # Mongoose models
│   │   ├── routes/         # API routes
│   │   ├── middlewares/    # Custom middleware
│   │   └── utils/          # Utilities
│   └── package.json
└── README.md
```

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or Atlas)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd blogging_web
   ```

2. **Setup Backend**
   ```bash
   cd server
   npm install
   cp .env.example .env
   # Edit .env with your MongoDB URI and JWT secret
   npm run dev
   ```

3. **Setup Frontend**
   ```bash
   cd client
   npm install
   cp .env.example .env
   # Edit .env with your API URL
   npm run dev
   ```

### Environment Variables

**Server (.env):**
```
PORT=4000
MONGO_URI=mongodb://localhost:27017/blogging_platform
JWT_SECRET=your_jwt_secret_here
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

**Client (.env):**
```
VITE_API_URL=http://localhost:4000
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register user
- `POST /api/auth/login` - Login user
- `GET /api/auth/me` - Get current user

### Posts
- `GET /api/posts` - Get all posts (with pagination, search, filters)
- `GET /api/posts/:id` - Get single post
- `POST /api/posts` - Create post (auth required)
- `PUT /api/posts/:id` - Update post (auth required)
- `DELETE /api/posts/:id` - Delete post (auth required)

### Upload
- `POST /api/upload` - Upload image (auth required)

## Usage

1. **Register/Login** - Create an account or login
2. **Create Posts** - Use the rich-text editor to create blog posts
3. **View Posts** - Browse all posts on the homepage
4. **Edit Posts** - Authors can edit their own posts
5. **Categories** - Organize posts with categories

## Development

### Running Tests
```bash
# Backend tests
cd server
npm test

# Frontend tests
cd client
npm test
```

### Building for Production
```bash
# Build frontend
cd client
npm run build

# Start production server
cd server
npm start
```

## Deployment

### Frontend (Vercel)
1. Connect your GitHub repository to Vercel
2. Set environment variables in Vercel dashboard
3. Deploy automatically on push

### Backend (Railway/Render)
1. Connect your GitHub repository
2. Set environment variables
3. Deploy automatically on push

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request
