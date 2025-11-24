# 🌐 Web Application Engineering – 

# 🚀 সূচিপত্র

1. Web Architecture
2. Browser & Rendering
3. Client–Server Communication
4. API & Backend
5. Authentication & Security
6. Database & Optimization
7. Performance & Scalability
8. DevOps & Deployment
9. Realtime & Distributed System Concepts
10. Extra Pro Tips

---

# ⭐ অংশ–১: Web Architecture

## **1. ওয়েব অ্যাপ্লিকেশন কীভাবে কাজ করে?**

**উত্তর:**
একটি ওয়েব অ্যাপ্লিকেশন হলো Client–Server ভিত্তিক সফটওয়্যার। ইউজার ব্রাউজার দিয়ে Request পাঠায়, Server প্রসেস করে Response ফেরত পাঠায় এবং Browser UI Render করে।

---

## **2. Client–Server Model কী?**

**উত্তর:**

* **Client:** ইউজার ইন্টারফেস (Browser / Mobile App)
* **Server:** Logic + Database পরিচালনা করে
  Client request পাঠায়, server data/procesing করে response ফেরত দেয়।

---

## **3. Web Application Architecture-এর প্রধান ৩টি ধরন কী?**

**উত্তর:**

* **Monolithic Architecture**
* **Microservices Architecture**
* **Serverless Architecture**

---

## **4. Single Page Application (SPA) কীভাবে কাজ করে?**

**উত্তর:**
SPA অ্যাপ একবারে HTML/CSS/JS লোড করে এবং এরপর সমস্ত পেজ পরিবর্তন browser-এর ভেতর JavaScript handle করে। Page reload লাগে না – React, Vue, Angular ব্যবহার করে।

---

## **5. Multi-Page Application (MPA) কী?**

**উত্তর:**
প্রতিটি পেজ লোডের সময় সার্ভার থেকে নতুন HTML পাঠায়। SEO অনেক ভালো কিন্তু SPA এর মতো smooth experience দেয় না।

---

## **6. CSR, SSR এবং SSG এর পার্থক্য কী?**

**উত্তর:**

* **CSR:** Browser-এ render (React SPA)
* **SSR:** Server HTML Render করে পাঠায় (Next.js)
* **SSG:** Build time-এ HTML generate (Next.js static pages)

---

## **7. Component-Based Architecture কী?**

**উত্তর:**
UI কে ছোট ছোট component-এ ভাগ করে reusable এবং maintainable করে তোলা। React এই architecture follow করে।

---

# ⭐ অংশ–২: Browser & Rendering

## **8. DOM (Document Object Model) কী?**

**উত্তর:**
Browser HTML → Tree Structure-এ convert করে। JavaScript এই tree manipulate করে UI পরিবর্তন করতে পারে।

---

## **9. DOM Rendering এর ধাপগুলো কী?**

**উত্তর:**

1. Parsing HTML → DOM Tree
2. Parsing CSS → CSSOM Tree
3. DOM + CSSOM → Render Tree
4. Layout Calculation
5. Painting on Screen

---

## **10. Reflow এবং Repaint কী?**

**উত্তর:**

* **Reflow:** Layout পুনরায় গণনা
* **Repaint:** শুধুমাত্র visual update
  Performance optimization এ এগুলো খুব গুরুত্বপূর্ণ।

---

## **11. Browser কীভাবে JavaScript execute করে?**

**উত্তর:**
JavaScript Engine (V8/SpiderMonkey) কোডকে bytecode-এ convert করে এবং event loop দ্বারা asynchronous কাজ handle করে।

---

## **12. Event Loop কীভাবে async কাজ করে?**

**উত্তর:**
Event Queue, Call Stack এবং Microtask Queue মিলিয়ে asynchronous কার্য সম্পন্ন করে।

---

# ⭐ অংশ–৩: Client–Server Communication

## **13. HTTP কী এবং কীভাবে কাজ করে?**

**উত্তর:**
HyperText Transfer Protocol—Client request পাঠায়, Server response পাঠায়। Stateless protocol।

---

## **14. HTTPS কেন নিরাপদ?**

**উত্তর:**
TLS/SSL encryption ব্যবহার করে data সুরক্ষিতভাবে transfer হয়।

---

## **15. REST API কী?**

**উত্তর:**
Resource ভিত্তিক API, যেখানে client HTTP method (GET/POST/PUT/DELETE) ব্যবহার করে server-এর সাথে যোগাযোগ করে।

---

## **16. GraphQL REST থেকে কিভাবে আলাদা?**

**উত্তর:**
GraphQL এ client যা data চায় শুধু সেটাই request করে—REST-এ fixed endpoints।

---

## **17. WebSocket কী?**

**উত্তর:**
Full-duplex real-time communication protocol। Server এবং Client দুই দিক থেকেই data push করতে পারে।

---

## **18. CORS কেন লাগে?**

**উত্তর:**
Browser cross-origin request security restrict করে। CORS allow header দিয়ে নির্দিষ্ট domain কে অনুমতি দেওয়া হয়।

---

# ⭐ অংশ–৪: API & Backend

## **19. Middleware কী?**

**উত্তর:**
Request–Response এর মাঝের ফাংশন যা validation, auth, logging ইত্যাদি কাজ করে।

---

## **20. API Versioning কেন গুরুত্বপূর্ণ?**

**উত্তর:**
পুরনো এবং নতুন API একসাথে maintain করতে version ব্যবহার করা হয়।

---

## **21. Rate Limiting কী?**

**উত্তর:**
API abuse বা DDoS attack প্রতিরোধে প্রতি IP বা user-এর request limit করা।

---

## **22. JWT Authentication কীভাবে কাজ করে?**

**উত্তর:**
Token → payload + signature → client cookies/localStorage এ রাখে → request header এ পাঠিয়ে user verify করা হয়।

---

## **23. Refresh Token কেন ব্যবহার করা হয়?**

**উত্তর:**
Access token ছোট সময়ের জন্য valid হয়। Refresh token ব্যবহার করে নতুন access token জেনারেট করা যায়।

---

# ⭐ অংশ–৫: Security

## **24. XSS Attack কী?**

**উত্তর:**
Attacker UI তে malicious script inject করে user-এর data চুরি করতে পারে।

---

## **25. CSRF Attack কী?**

**উত্তর:**
User logged-in থাকা অবস্থায় অন্য site থেকে unauthorized request পাঠানো।

---

## **26. SQL Injection কী?**

**উত্তর:**
Raw query-তে malicious SQL পাঠিয়ে database manipulate করা। Prepared Statement দিয়ে সমাধান।

---

## **27. HTTPS না থাকলে কী ঝুঁকি?**

**উত্তর:**
Password/data plaintext এ যায়—attacker সহজে intercept করতে পারে।

---

## **28. OWASP Top 10 কী?**

**উত্তর:**
Web security vulnerabilities এর global standard list।

---

# ⭐ অংশ–৬: Database & Optimization

## **29. SQL vs NoSQL পার্থক্য**

**উত্তর:**

* SQL → Structured, Relational, ACID
* NoSQL → Flexible, Distributed, High scalability

---

## **30. Index কী এবং কেন দরকার?**

**উত্তর:**
Index data দ্রুত খুঁজে পেতে সাহায্য করে (like book index)।

---

## **31. Joins এর ধরন কী?**

**উত্তর:**
Inner, Left, Right, Full join।

---

## **32. Database Normalization কী?**

**উত্তর:**
Redundancy কমানো এবং relational structure ঠিক রাখা।

---

## **33. Caching কেন দরকার?**

**উত্তর:**
Same data বারবার query না করে দ্রুত সার্ভ করতে cache ব্যবহার করা হয়। Redis জনপ্রিয়।

---

# ⭐ অংশ–৭: Performance & Scalability

## **34. Load Balancing কী?**

**উত্তর:**
Incoming traffic multiple server-এ ভাগ করে দেওয়া।

---

## **35. CDN কেন গুরুত্বপূর্ণ?**

**উত্তর:**
Static files user-এর nearest server এ store করে speed বাড়ায়।

---

## **36. Lazy Loading কী?**

**উত্তর:**
প্রয়োজন হলে তখনই resource load করা।

---

## **37. Debounce & Throttle কেন ব্যবহার করা হয়?**

**উত্তর:**
Frequent events control করতে (scroll/search)।

---

## **38. Bundle Splitting কী?**

**উত্তর:**
JS bundle ছোট ছোট ভাগে ভাগ করে load time কমানো।

---

# ⭐ অংশ–৮: DevOps & Deployment

## **39. CI/CD কী?**

**উত্তর:**
Code push হলেই automated test, build এবং deploy pipeline।

---

## **40. Docker কী?**

**উত্তর:**
Application কে containerize করে everywhere একই environment দিতে।

---

## **41. Kubernetes কী?**

**উত্তর:**
Container orchestration system—deployment, scaling, load balancing—all automated.

---

## **42. Reverse Proxy কী?**

**উত্তর:**
Client request আগে গ্রহণ করে proper server-এ পাঠায়। (Nginx জনপ্রিয়)

---

# ⭐ অংশ–৯: Realtime & Distributed Systems

## **43. Pub/Sub কী?**

**উত্তর:**
Publisher event পাঠায়, subscriber event receive করে।

---

## **44. Distributed System কী?**

**উত্তর:**
Multiple server মিলিয়ে একসাথে কাজ করা যেখানে data এবং logic distributed।

---

## **45. CAP Theorem কী?**

**উত্তর:**
Consistency, Availability, Partition Tolerance – একসাথে তিনটি পূর্ণ করা যায় না।

---

## **46. Message Queue কেন দরকার?**

**উত্তর:**
Async tasks handle করতে queue খুব গুরুত্বপূর্ণ (RabbitMQ, Kafka)।

---

## **47. Horizontal vs Vertical Scaling**

**উত্তর:**

* Horizontal → Server সংখ্যা বাড়ানো
* Vertical → Server CPU/RAM বাড়ানো

---

# ⭐ অংশ–১০: Extra Pro Tips

## **48. Monolithic vs Microservices**

**উত্তর:**
Monolithic = One big codebase
Microservices = ছোট ছোট independent services

---

## **49. Serverless Architecture কী?**

**উত্তর:**
Function-based execution যেখানে server manage করতে হয় না (AWS Lambda)।

---

## **50. API Gateway কেন ব্যবহার করা হয়?**

**উত্তর:**
Microservices পরিচালনা, routing, security ও rate limiting control করার জন্য Gateway ব্যবহৃত হয়।
