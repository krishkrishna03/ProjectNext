# 🚀 ProjNest — Final Year Projects, Simplified

> **The #1 platform for engineering students in India to discover, purchase, and build standout final year projects — with source code, documentation, PPTs, and expert mentor support.**

---

## 💡 What is ProjNest?

ProjNest is a startup built for final year engineering students across India who struggle with finding the right project idea, tech stack, documentation, and guidance before their submission deadline.

We provide:
- **Curated project kits** with real source code, project reports (60–90 pages), PPTs (15–25 slides), and datasets
- **Live deployed demos** so students can see the project working before purchasing
- **Expert mentor support** for doubts, viva prep, and custom changes
- **Custom project requests** for students with specific requirements

---

## ✨ Name Story

| Name | Why it works |
|------|-------------|
| **ProjNest** ✅ | Short, catchy, memorable. "Nest" = a safe place where your project grows. Easy to say, easy to type. |
| ProjHive | Projects buzzing together like a hive — community feel |
| BuildNest | Focus on building, same warmth |
| FinalDesk | Your final year desk — where work gets done |
| ProjecTree | Projects grow like a tree — creative but hard to spell |

**Recommended: `ProjNest`** — Available as a `.in` domain, clean for branding, works as an app name too.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5, CSS3, Vanilla JS (MVP) → React (v2) |
| Backend | Node.js + Express.js |
| Database | MongoDB + Mongoose |
| Auth | JWT (JSON Web Tokens) |
| Payments | Razorpay (India-first) |
| File Storage | AWS S3 / Cloudflare R2 (for PDFs, PPTs, ZIP files) |
| Hosting (Frontend) | Vercel |
| Hosting (Backend) | Render / Railway |
| Email | Nodemailer + Gmail SMTP |

---

## 📁 Project Structure

```
projnest/
├── client/                  # Frontend
│   ├── index.html           # Main homepage
│   ├── domains.html         # Domain listing page
│   ├── project.html         # Project detail page
│   ├── dashboard.html       # Student dashboard / My Requests
│   ├── css/
│   │   └── style.css
│   └── js/
│       ├── app.js
│       ├── payment.js
│       └── dashboard.js
│
├── server/                  # Backend (Node.js + Express)
│   ├── index.js             # Entry point
│   ├── config/
│   │   └── db.js            # MongoDB connection
│   ├── models/
│   │   ├── User.js          # Student model
│   │   ├── Project.js       # Project listing model
│   │   ├── Order.js         # Purchase/order model
│   │   └── Request.js       # Custom request model
│   ├── routes/
│   │   ├── auth.js          # Login / Register
│   │   ├── projects.js      # Browse & fetch projects
│   │   ├── payment.js       # Razorpay integration
│   │   ├── requests.js      # Student request CRUD
│   │   └── admin.js         # Admin panel routes
│   ├── middleware/
│   │   ├── auth.js          # JWT middleware
│   │   └── admin.js         # Admin check middleware
│   └── utils/
│       ├── email.js         # Send confirmation emails
│       └── storage.js       # S3 file access helpers
│
├── admin/                   # Admin panel (simple HTML or React)
│   └── index.html
│
├── .env.example             # Environment variable template
├── .gitignore
├── package.json
└── README.md
```

---

## ⚙️ Environment Variables

Create a `.env` file in the `server/` directory:

```env
# Server
PORT=5000
NODE_ENV=development

# MongoDB
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/projnest

# JWT
JWT_SECRET=your_super_secret_key_here
JWT_EXPIRE=7d

# Razorpay
RAZORPAY_KEY_ID=rzp_test_xxxxxxxxxxxxxx
RAZORPAY_KEY_SECRET=your_razorpay_secret

# Email (Gmail SMTP)
EMAIL_USER=hello@projnest.in
EMAIL_PASS=your_app_password

# AWS S3 (for file storage)
AWS_ACCESS_KEY=your_aws_access_key
AWS_SECRET_KEY=your_aws_secret_key
AWS_BUCKET_NAME=projnest-files
AWS_REGION=ap-south-1
```

---

## 🚀 Getting Started (Local Development)

### Prerequisites
- Node.js v18+
- MongoDB Atlas account (free tier works)
- Razorpay test account

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/projnest.git
cd projnest
```

### 2. Install dependencies
```bash
cd server
npm install
```

### 3. Set up environment
```bash
cp .env.example .env
# Fill in your values in .env
```

### 4. Run the backend
```bash
npm run dev
# Server runs on http://localhost:5000
```

### 5. Open the frontend
```bash
# Simply open client/index.html in your browser
# Or use Live Server in VS Code
```

---

## 📦 API Endpoints

### Auth
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Student registration |
| POST | `/api/auth/login` | Student login |
| GET | `/api/auth/me` | Get current user |

### Projects
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/projects` | Get all projects |
| GET | `/api/projects/:id` | Get single project |
| GET | `/api/projects/domain/:domain` | Get by domain |

### Orders / Payment
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/payment/create-order` | Create Razorpay order |
| POST | `/api/payment/verify` | Verify payment signature |
| GET | `/api/payment/my-orders` | Get student's purchases |

### Requests
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/requests` | Submit new request |
| GET | `/api/requests/mine` | Get my requests |
| PUT | `/api/requests/:id` | Edit a request |
| DELETE | `/api/requests/:id` | Cancel a request |

---

## 🗺️ Roadmap

- [x] Static homepage with domain listing
- [x] Project detail page with live demo link
- [x] All documents locked behind payment
- [x] Payment modal with Razorpay UI
- [x] My Requests dashboard (edit, update, cancel)
- [ ] Node.js + MongoDB backend
- [ ] JWT authentication (login/register)
- [ ] Real Razorpay payment integration
- [ ] Admin panel (manage requests, upload files)
- [ ] Email notifications after purchase
- [ ] Student dashboard (download purchased files)
- [ ] Mobile app (React Native) — v2
- [ ] Mentor onboarding portal — v2
- [ ] Blog / SEO pages for organic traffic — v2

---

## 🤝 Contributing

This is currently a private project. If you're a collaborator:

1. Fork the repo
2. Create your branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📬 Contact

Built with ❤️ for Indian engineering students.

- 📧 Email: hello@projnest.in
- 💬 WhatsApp: [Support Group](#)
- 📸 Instagram: [@projnest.in](#)

---

## 📄 License

This project is proprietary. All rights reserved © 2026 ProjNest.

---

> *"Every great project started with one small step. Let ProjNest be yours."*
