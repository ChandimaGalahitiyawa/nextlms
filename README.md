# Architecture for Next.js-based LMS

## Frontend (Next.js)
- **Deployment**: Hosted on Vercel for fast and efficient deployment.
- **Functionality**: Manages the user interface, course pages, and user interactions.

## Authentication (NextAuth.js)
- **Integration**: Instead Clerk with NextAuth.js for streamlined authentication.
- **Features**: Free to use and supports various OAuth providers such as Google, GitHub, etc.
- **User Access**: Users can easily sign in and be authenticated through NextAuth.

## Payments (Stripe)
- **Payment Processing**: Utilizes Stripe to handle course payments and manage user access.
- **Tracking Purchases**: Leverages Stripe metadata to monitor which courses each user has purchased.
- **Database Management**: Eliminates the need for a separate database to manage user-course relationships.

## Course Data Storage
- **Data Format**: Utilizes JSON files to store course data, replacing traditional databases like MongoDB.
- **Data Fetching**: JSON data can be efficiently fetched using Next.js' static generation or server-side rendering capabilities.

## Video Hosting (Vimeo)
- **Video Storage**: Videos are hosted on Vimeo for reliable and high-quality streaming.
- **Security**: Videos are set to private, with playback restrictions enforced to ensure secure delivery to authorized users only.
