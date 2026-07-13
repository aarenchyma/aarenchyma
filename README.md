# Hi, I'm Victor 👋

## What I actually do

Most of software is not writing code — it's deciding where the boundaries go. I spend most of my time on that: where does this responsibility live, what happens when two things happen at once, what breaks first under load, what's the blast radius when it does.

I'm the sole engineer behind **[Sendrey](sendrey.com)**, a two-sided delivery/errand marketplace, where I own the system end-to-end. A few of the harder problems I've had to actually solve there:

- **Escrow payments under concurrent access** — money moves between wallets, orders, and disputes at the same time. Getting the ledger to stay consistent when two requests touch the same balance is a much harder problem than "call Paystack."
- **Real-time state across sockets, retries, and reconnects** — chat, order tracking, and live calls (WebRTC via Agora) all need to survive dropped connections without silently losing or duplicating events. Sequence numbers, ACKs, and gap detection, not just `socket.emit()`.
- **KYC and dispute pipelines with real state machines** — statuses that can't skip steps, windows that open and close, and admin overrides that have to not break the automated flow.

The stack for this is Node.js/Express, MongoDB, Redis, Socket.IO on the backend, React/Redux (web + Capacitor mobile) and Next.js on the frontend — but the stack was never the hard part.

## Why I'm digging into architecture now

I'm currently taking a software architecture course, and it's reframed a lot for me: writing the code that satisfies a spec is the easy 20%. Deciding the shape of the system — what's a plugin, what's core, what's allowed to know about what — is the part that actually determines whether the codebase is still sane a year later.

I've started working through smaller, focused Java projects specifically to isolate architectural patterns away from the noise of a full production app. First one: a **[payment processing system built on microkernel architecture](link-to-repo)** — a core kernel that knows nothing about *how* any payment method works, only that plugins conform to a shared interface. The point of the exercise wasn't "process a payment," it was proving a new payment method can be added with zero changes to the core.


## Stack

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) 
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white) 
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white) 
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) 
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) 
![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=flat-square&logo=socket.io&logoColor=white) 
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) 
![Redux](https://img.shields.io/badge/Redux-764ABC?style=flat-square&logo=redux&logoColor=white) 
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white) 
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white) 
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) 
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white) 

## Find Me

- 🌐 [Portfolio](https://my-portfolio-ten-orpin-4z4as87101.vercel.app/)
- 💼 [LinkedIn](https://www.linkedin.com/in/akinola-victor-27a33b320/)
- 📍 Lagos, Nigeria
