# PingUp Social Media

PingUp is a full-stack social media application designed to connect people globally. It offers features like creating posts, sharing stories, real-time messaging, and managing connections.

**Live Link:** [https://ping-up-appfront.vercel.app/](https://ping-up-appfront.vercel.app/)

---

## Features ✨

* **Authentication:** Secure user login and registration handled by Clerk.
* **Feed:** View posts from users you follow and are connected with.
* **Create Posts:** Share text updates, images, or a combination of both.
* **Stories:** Share temporary updates (text, image, or video) that disappear after 24 hours.
* **User Profiles:** View and edit user profiles including profile picture, cover photo, bio, and location.
* **Discover Users:** Find new people by searching based on name, username, bio, or location.
* **Connections:**
    * Follow and unfollow users.
    * Send, receive, and accept connection requests.
    * View followers, following, pending requests, and established connections.
* **Notifications:** Receive email reminders for pending connection requests and unseen messages. Receive real-time toast notifications for new messages.
* **Image Handling:** Uploads managed via Multer, optimized and served by ImageKit.

---

## Tech Stack 🛠️

### Frontend (Client)

* **Framework:** React
* **Build Tool:** Vite
* **Styling:** Tailwind CSS
* **State Management:** Redux Toolkit
* **Routing:** React Router DOM
* **Authentication:** Clerk React
* **API Client:** Axios
* **UI/Icons:** Lucide React
* **Date Formatting:** Moment.js
* **Notifications:** React Hot Toast

### Backend (Server)

* **Framework:** Node.js, Express
* **Database:** MongoDB with Mongoose
* **Authentication:** Clerk Express
* **Image Hosting:** ImageKit
* **File Uploads:** Multer
* **Background Jobs/Events:** Inngest
* **Email:** Nodemailer with Brevo SMTP
* **Environment Variables:** dotenv

---

## Getting Started 🚀

### Prerequisites

* Node.js (>=18 recommended for server)
* npm or yarn
* MongoDB instance (local or cloud like MongoDB Atlas)
* Clerk Account ([https://clerk.com/](https://clerk.com/))
* ImageKit Account ([https://imagekit.io/](https://imagekit.io/))
* Brevo (or other SMTP provider) Account ([https://www.brevo.com/](https://www.brevo.com/))
* Inngest Account ([https://www.inngest.com/](https://www.inngest.com/))

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd pingup_social_media
    ```

2.  **Server Setup:**
    * Navigate to the server directory: `cd server`
    * Install dependencies: `npm install` (or `yarn install`)
    * Create a `.env` file in the `server` directory. See the Environment Variables section below for required variables.
    * Run the server: `npm run server` (for development with nodemon) or `npm start`

3.  **Client Setup:**
    * Navigate to the client directory: `cd ../client`
    * Install dependencies: `npm install` (or `yarn install`)
    * Create a `.env` file in the `client` directory. See the Environment Variables section below.
    * Run the client: `npm run dev`

### Running Locally

* Start the backend server first (`cd server && npm run server`).
* Then start the frontend client (`cd client && npm run dev`).
* Open your browser and navigate to the local URL provided by Vite (usually `http://localhost:5173` or similar).

---

## Environment Variables ⚙️

### Server (`server/.env`)

```env
MONGODB_URL=your_mongodb_connection_string
PORT=4000 # Or any port you prefer
CLERK_SECRET_KEY=your_clerk_secret_key

# ImageKit Credentials
IMAGEKIT_PUBLIC_KEY=your_imagekit_public_key
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
IMAGEKIT_URL_ENDPOINT=your_imagekit_url_endpoint

# Nodemailer / Brevo Credentials
SMTP_USER=your_smtp_user_email
SMTP_PASS=your_smtp_password
SENDER_EMAIL=your_sender_email # Email address emails will be sent from

# Inngest Key
INNGEST_EVENT_KEY=your_inngest_event_key

# Frontend URL (for email links)
FRONTEND_URL=http://localhost:5173 # Or your deployed frontend URL
