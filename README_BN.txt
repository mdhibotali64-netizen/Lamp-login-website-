LAMP LOGIN ANIMATION WEBSITE
============================

ফিচার
- ছবির মতো dark olive background, হলুদ আলো, animated lamp ও fireflies
- Responsive login/signup UI
- Node.js backend চালালে SQLite database-এ user account, bcrypt password hash ও server session
- Node server না চালিয়ে index.html খুললে local demo mode-এ সাইনআপ/লগইন কাজ করবে

চালানোর নিয়ম (Backend সহ)
--------------------------
১) কম্পিউটারে Node.js 18 বা তার পরের সংস্করণ ইনস্টল করুন।
২) এই ফোল্ডার খুলে Terminal/Command Prompt চালান।
৩) চালান: npm install
৪) একটি শক্তিশালী session secret সেট করুন (production-এ অবশ্যই):
   Linux/macOS: SESSION_SECRET="এখানে-লম্বা-র‍্যান্ডম-সিক্রেট" npm start
   Windows PowerShell: $env:SESSION_SECRET="এখানে-লম্বা-র‍্যান্ডম-সিক্রেট"; npm start
   লোকাল পরীক্ষার জন্য: npm start
৫) ব্রাউজারে http://localhost:3000 খুলুন।
৬) Create an account দিয়ে অ্যাকাউন্ট খুলে Sign In পরীক্ষা করুন।

গুরুত্বপূর্ণ নিরাপত্তা নোট
-------------------------
- সরাসরি index.html খুললে localStorage-ভিত্তিক DEMO fallback চলে। এতে পাসওয়ার্ড ব্রাউজারের localStorage-এ plain text হিসেবে থাকে। বাস্তব/প্রোডাকশন ব্যবহারে এই demo mode ব্যবহার করবেন না।
- বাস্তব ব্যবহারে সবসময় Node backend-এর মাধ্যমে চালান; index.html ফাইল আলাদাভাবে খুলবেন না।
- প্রকাশের আগে HTTPS, persistent session store, শক্তিশালী SESSION_SECRET, rate limiting/monitoring, backups, privacy policy, terms, এবং production security review যোগ করুন।
- Google/GitHub বোতামগুলো ডিজাইন করা আছে; OAuth Client ID/Secret ও callback route কনফিগার না করা পর্যন্ত social login কাজ করবে না।
- এই starter-এ ইমেইল ভেরিফিকেশন, password reset, CAPTCHA, admin panel বা OAuth অন্তর্ভুক্ত নয়।
- ফন্ট Google Fonts থেকে লোড হয়; ফন্ট না এলে fallback font ব্যবহার হবে।
