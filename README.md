# Bazar Dor 🛒

**Bazar Dor** is a modern web application built with Next.js that aims to provide users with a convenient online shopping experience. The project focuses on a clean user interface, product browsing, category-based navigation, and secure user authentication.

## ✨ Features

- 🛍️ **Product Store:** Browse and explore products.
- 📂 **Category-Based Navigation:** Find products by category.
- 🔐 **User Authentication:** Sign up and sign in using Better Auth.
- 🔑 **Email & Password Authentication:** Authenticate using email and password.
- 🌐 **Google Sign-In:** Social authentication with Google.
- 👤 **User Profile:** Access user-related information.
- 📱 **Responsive UI:** Designed for different screen sizes.
- 🎨 **Modern Styling:** Built with Tailwind CSS and daisyUI.
- 🚀 **Deployment Ready:** Configured for deployment on Vercel.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Next.js | React framework for the application |
| React | Building interactive user interfaces |
| TypeScript | Application logic |
| Better Auth | Authentication and session management |
| MongoDB | Database |
| MongoDB Atlas | Cloud database hosting |
| Tailwind CSS | Utility-first styling |
| daisyUI | UI components and styling |
| Vercel | Deployment and hosting |
| Git & GitHub | Version control and source code management |

## 📁 Project Structure

```text
bazar-dor/
├── public/
│   └── images/
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   └── auth/
│   │   │       └── [...all]/
│   │   │           └── route.js
│   │   ├── category/
│   │   │   └── [id]/
│   │   ├── products/
│   │   │   └── [id]/
│   │   ├── sign-in/
│   │   ├── sign-up/
│   │   ├── profile/
│   │   ├── log-out/
│   │   ├── layout.js
│   │   └── page.js
│   ├── components/
│   ├── lib/
│   │   ├── auth.js
│   │   └── auth-client.js
│   └── proxy.js
├── .env.local
├── .gitignore
├── package.json
└── README.md
```

*Note: The structure above is a general overview. Your actual folders and filenames may differ.*

## ⚙️ Getting Started

Follow these steps to create and run the Bazar Dor project locally.

### 1. Create a Next.js Project

Make sure Node.js is installed on your computer. Open your terminal and run:

```bash
npx create-next-app@latest bazar-dor
```

During setup, configure the options according to your project requirements, including JavaScript, App Router, and Tailwind CSS.

### 2. Navigate to the Project Directory

```bash
cd bazar-dor
```

### 3. Install Dependencies

Install the required packages:

```bash
npm install better-auth @better-auth/mongo-adapter mongodb
npm install daisyui react-toastify
```

Install any additional UI libraries required by your implementation.

### 4. Configure Environment Variables

Create a `.env.local` file in the root directory:

```env
BETTER_AUTH_DB_URL=your_mongodb_connection_string
BETTER_AUTH_URL=http://localhost:3000
BETTER_AUTH_SECRET=your_secure_random_secret

GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
```

Replace the placeholder values with your actual credentials.

### 5. Configure MongoDB Atlas

1. Create a MongoDB Atlas cluster.
2. Create a database user and configure network access.
3. Copy your MongoDB connection string.
4. Add the connection string to `BETTER_AUTH_DB_URL`.
5. Verify that your application can connect to the database.

### 6. Configure Better Auth

Set up the Better Auth server configuration, MongoDB adapter, authentication API route, and client configuration.

Enable email/password authentication and configure Google Sign-In if required.

### 7. Start the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### 8. Build the Project

To create an optimized production build, run:

```bash
npm run build
```

To start the production server:

```bash
npm run start
```

## 🔧 Troubleshooting

**MongoDB connection error**
- Verify `BETTER_AUTH_DB_URL`.
- Check MongoDB Atlas network access and database credentials.
- Ensure environment variables are available during the build and runtime.

**Google Sign-In error**
- Verify `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET`.
- Check authorized redirect URIs.
- Confirm the Better Auth Google provider is configured correctly.

**Vercel build failure**
- Run `npm run build` locally.
- Review the complete build log.
- Check for missing environment variables and server-side initialization errors.

## 🚧 Future Improvements

- Shopping cart functionality.
- Product search and filtering.
- Product sorting by price.
- Wishlist functionality.
- Order management.
- Payment gateway integration.
- Admin dashboard.
- Product reviews and ratings.

## 👨‍💻 Author

**Moktarul Islam**

- GitHub: https://github.com/immoktarulislam/bazar-dor-rate-1

---

**Bazar Dor — A modern shopping experience built with Next.js.**
