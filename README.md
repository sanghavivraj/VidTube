# VidTube
#  VIDTUBE - Full Stack Video Sharing Platform

**Project Type**: MERN Stack (MongoDB, Express, React, Node.js) with TailwindCSS
 
 **Folder Structure**: `fullstack_learn/` → contains `BackEnd/`, `React_learn/`, and `docs/`

---

##  Objective
VIDTUBE is a full-featured video-sharing platform inspired by YouTube, where users can:
- Upload and manage videos
- It's also manage the Thumbnail 
- Like, comment, and create tweets about content
- Organize videos in playlists
- Subscribe to other users
- Track history and more.

The platform uses JWT authentication, follows a modular controller-service-model pattern, and is designed to be scalable and developer-friendly.

---

##  Key Concepts (**Object**, **Context**, **Information**)

### 1. **User Authentication**
- **Object**: User
- **Context**: Registration, Login, JWT-based Auth, Protected Routes
- **Information**: email, username, fullname, avatar, coverImage, watchHistory

### 2. **Videos**
- **Object**: Video
- **Context**: Upload, Watch, Delete, Edit, Search
- **Information**: title, description, video file, owner, views, likes, dislikes

### 3. **Comments**
- **Object**: Comment
- **Context**: Add comments to a video, fetch comments by video ID
- **Information**: content, owner, video ID, timestamp

### 4. **Tweets**
- **Object**: Tweet
- **Context**: Users can tweet thoughts about a video or general updates
- **Information**: content, owner (user), timestamps

### 5. **Playlists**
- **Object**: Playlist
- **Context**: Users organize videos into categories/playlists
- **Information**: name, description, list of video IDs, owner

### 6. **Subscriptions** *(Upcoming)*
- **Object**: Subscription
- **Context**: Users can subscribe to other users for updates
- **Information**: subscriber ID, subscribedTo ID

### 7. **Watch History**
- **Object**: Watch History Array (inside User)
- **Context**: Updated when user watches any video
- **Information**: List of video IDs with timestamps

---

##  Technologies Used
- Frontend: React (Vite), TailwindCSS, JSX
- Backend: Node.js, Express.js
- Database: MongoDB Atlas with Mongoose ODM
- Authentication: JWT (Access & Refresh Tokens)
- Cloud: Cloudinary for image upload (avatars/covers)
- Testing & API Tools: Postman

---

##  Design Philosophy
- Followed MVC pattern
- Used `asyncHandler` for clean async/await error handling
- `ApiResponse` and `ApiError` utils for consistent API structure
- Modular route setup for each feature (user, video, comment, tweet, playlist)


---

##  Project Modules Summary
| Module     | Feature Handled      | Methods / Routes                  |
|------------|----------------------|-----------------------------------|
| `user`     | Auth/Profile         | login, signup, refresh, logout    |
| `video`    | CRUD + View tracking | create, update, delete, view, get |
| `comment`  | Comments on videos   | create, fetch, delete             |
| `tweet`    | Micro-posting        | create, update, delete, userwise  |
| `playlist` | Video collections    | create, add/remove video, delete  |

---

##  Current Status
-  User Authentication completed
-  Video upload/view/comment system live
-  Tweets module added
-  Playlist module implemented


---

##  Internal Routes Structure (API)
| Route                                                 | Purpose                        |
|-------------------------------------------------------|--------------------------------|
| `POST /api/v1/users/login`                            | Login                          |
| `POST /api/v1/videos/`                                | Upload a new video             |
| `POST /api/v1/comments/`                              | Add comment to video           |
| `GET /api/v1/tweets/user`                             | Get all user tweets            |
| `PATCH /api/v1/tweets/:id`                            | Update a tweet                 |
| `POST /api/v1/playlists`                              | Create playlist                |
| `PATCH /api/v1/playlists/:playlistId/videos/:videoId` | Add/remove video from playlist |

---




