<div align="center">

<!-- Animated Typing Header -->
[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=2E74B5&center=true&vCenter=true&width=600&lines=Hi+%F0%9F%91%8B+I'm+Ali+Jaan;Full+Stack+Developer;AI+Integration+Specialist;API+%26+System+Architect)](https://git.io/typing-svg)

<p>
  <a href="https://hirealijaan.com"><img src="https://img.shields.io/badge/Portfolio-hirealijaan.com-2E74B5?style=for-the-badge&logo=google-chrome&logoColor=white"/></a>
  <a href="https://www.linkedin.com/in/engr-ali-jaan-manzoor/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:ranaalijaanmanzoor@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
</p>

</div>

---

### 👨‍💻 About Me

```typescript
const AliJaan = {
  role:        "Full Stack Developer",
  location:    "Lahore, Pakistan 🇵🇰",
  experience:  "3+ years",
  focus:       ["Full Stack Apps", "AI Integration", "API & System Design"],
  currentWork: "Building scalable platforms @ Bright Techno Tonic",
  portfolio:   "https://hirealijaan.com",
};
```

- 🔭 Currently building a **20,000+ user e-learning platform** with live classes, payments & progress tracking
- 🤖 Passionate about **AI-first development** — daily user of Cursor, Claude Code & Windsurf
- 🛠 Specialized in **end-to-end solution delivery** — from architecture to production
- 💬 Ask me about **Python, React, Next.js, Angular, Node.js, NestJS, API design, or system architecture**

---

### 🛠 Tech Stack

#### Frontend
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Redux](https://img.shields.io/badge/Redux-764ABC?style=for-the-badge&logo=redux&logoColor=white)

#### Backend
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white)

#### Databases & Queues
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![BullMQ](https://img.shields.io/badge/BullMQ-EF4444?style=for-the-badge&logo=redis&logoColor=white)

#### Cloud & DevOps
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

#### AI & Dev Tools
![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=for-the-badge&logo=openai&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![Zapier](https://img.shields.io/badge/Zapier-FF4A00?style=for-the-badge&logo=zapier&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=for-the-badge&logo=stripe&logoColor=white)

---

### ⚙️ A Snippet I Reach For — Scalable Background Jobs (BullMQ + Redis)

```typescript
import { Queue, Worker } from "bullmq";
import IORedis from "ioredis";

// Shared Redis connection for queues and workers
const connection = new IORedis(process.env.REDIS_URL, {
  maxRetriesPerRequest: null, // required by BullMQ for blocking ops
});

// Init a queue for async work (emails, webhooks, notifications)
export const emailQueue = new Queue("emails", { connection });

// Worker pulls jobs off the queue and processes them
new Worker(
  "emails",
  async (job) => {
    await sendEmail(job.data); // offloaded from the request path
  },
  { connection, concurrency: 5 },
);
```

> Keeps API responses fast by pushing slow work (notifications, payment hooks, report
> generation) into Redis-backed queues that retry and scale independently.

---

### 🚀 Featured Projects

| Project | Description | Stack | Live |
|--------|-------------|-------|------|
| **E-TutorsCity** | Tutoring marketplace with scheduling, AI-powered matching & secure payments | MEAN Stack | [Live ↗](https://e-tutorscity.com/) |
| **E-LawyerCity** | Ethiopia's first virtual legal office — lawyer discovery, video consults & digital case management | Full Stack | [Live ↗](https://e-lawyerscity.com/) |
| **AgileBrains** | Microservices recruitment & applicant tracking platform with job posting, application tracking & interview notifications | Microservices | [Live ↗](https://agilebrains.com/) |

---

### 🏆 Highlights

- ⚡ Optimized API response times by **40%** through caching & query strategies
- 📈 Improved MongoDB performance by **60%** through targeted indexing
- 💳 Integrated **4 payment gateways** (Stripe, PayPal, Chapa, TeleBirr) processing **USD 10K+/month** at 99.9% uptime
- 🎓 Built an e-learning platform serving **20,000+ active learners** with live Zoom classes & progress tracking
- 👥 Led a team of **10 developers**, shipping **5 products** to production
- 🔎 Cut data-fetching time by **50%** across REST & GraphQL APIs (3,000+ monthly orders)
- 🤖 Delivered AI research tools — BirdWatch (YOLOv5, 77%) & a pneumonia detector (CNN, 84%)

---

<div align="center">
  <i>Open to exciting opportunities in Full Stack Development & AI Integration</i><br/>
  <a href="https://hirealijaan.com"><b>hirealijaan.com</b></a>
</div>
