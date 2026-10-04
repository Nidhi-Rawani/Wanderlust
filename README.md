# Wanderlust 🧭

A full-stack travel listing website where users can post places to stay, upload photos, view them on a map, and leave star-rated reviews.

**Live Demo:** https://wanderlust1-9mce.onrender.com
*(Hosted on Render's free tier, so the first load may take 30-60 seconds.)*

## Features

- Add, edit, and delete listings with image upload
- Sign up and log in (Passport.js)
- Only the owner of a listing can edit or delete it
- Star-rating reviews (Starability)
- Map location for each listing
- Form validation (Joi) and flash messages
- Reviews are deleted automatically when their listing is deleted

## Tech Stack

- **Backend:** Node.js, Express.js
- **Database:** MongoDB Atlas, Mongoose
- **Frontend:** EJS, EJS-Mate, Bootstrap, CSS
- **Auth:** Passport.js (local strategy), express-session, connect-mongo
- **Image Upload:** Multer, Cloudinary
- **Validation:** Joi

## Project Structure

```
├── models/         # Mongoose schemas (Listing, Review, User)
├── routes/         # Express routers (listings, reviews, users)
├── controllers/    # Route logic
├── views/          # EJS templates
├── public/         # CSS, JS, static files
├── utils/          # ExpressError, wrapAsync
├── middleware.js   # isLoggedIn, isOwner, validation
├── cloudConfig.js  # Cloudinary setup
└── app.js          # Entry point
```

## Run Locally

1. Clone the repo and install dependencies
   ```bash
   git clone <your-repo-link>
   cd <your-repo-folder>
   npm install
   ```

2. Create a `.env` file in the root folder
   ```
   ATLASDB_URL=your_mongodb_atlas_url
   SECRET=your_session_secret
   CLOUD_NAME=your_cloudinary_cloud_name
   CLOUD_API_KEY=your_cloudinary_api_key
   CLOUD_API_SECRET=your_cloudinary_api_secret
   ```

3. Start the server
   ```bash
   node app.js
   ```

4. Open `http://localhost:8080/listings`
