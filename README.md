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

Follow these steps to run the project locally.

### 1. Clone the Repository

```bash
git clone https://github.com/immoktarulislam/bazar-dor-rate-1
```

Navigate to the project folder:

```bash
cd bazar-dor
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env.local` file in the project root and configure the required environment variables.

```env
BETTER_AUTH_DB_URL=your_mongodb_connection_string
BETTER_AUTH_URL=http://localhost:3000
BETTER_AUTH_SECRET=your_secure_random_secret

GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
```

Replace the placeholder values with your actual configuration.

**Important:** Never commit `.env.local` or expose your database credentials, authentication secret, or Google client secret in a public repository.

### 4. Configure MongoDB Atlas

1. Create a MongoDB Atlas cluster.
2. Create a database user.
3. Configure the appropriate network access rules.
4. Copy your MongoDB connection string.
5. Add the connection string to `BETTER_AUTH_DB_URL`.
6. Ensure your application connects to the intended database.

### 5. Configure Google Sign-In

1. Open the Google Cloud Console.
2. Create or select a project.
3. Configure the OAuth consent screen.
4. Create OAuth 2.0 credentials.
5. Add your application's authorized redirect URI according to your Better Auth configuration.
6. Add the client ID and client secret to your environment variables.

Make sure the Google OAuth configuration matches the authentication callback URL used by your application.

### 6. Run the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### 7. Build for Production

Check whether the application builds successfully:

```bash
npm run build
```

Start the production server locally:

```bash
npm run start
```

## 🔒 Authentication

Bazar Dor uses Better Auth to manage user authentication.

Authentication features include:

- Email and password sign-up.
- Email and password sign-in.
- Google social sign-in.
- Session management.
- Authentication API routes.

Authentication requires valid environment variables and a working database connection. Google Sign-In also requires valid Google OAuth credentials.

## 🌍 Deployment

The application can be deployed on [Vercel](https://vercel.com/).

1. Push your project to GitHub.
2. Import the repository into Vercel.
3. Configure the required environment variables in Vercel Project Settings.
4. Ensure MongoDB Atlas allows connections from the deployment environment.
5. Configure the production `BETTER_AUTH_URL`.
6. Update Google OAuth authorized redirect URIs for production.
7. Deploy and verify the authentication and product pages.

Run `npm run build` locally before deployment to identify build-time errors.

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
