# AI Dev Studio

মোবাইল-ফ্রেন্ডলি **সার্ভারলেস** AI কোডিং অ্যাসিস্ট্যান্ট।  
DeepSeek / Grok / OpenAI-compatible API + GitHub-এ সরাসরি কোড পুশ সাপোর্ট করে।

সব ডেটা (API Key, Token, চ্যাট) শুধু আপনার ফোনের **localStorage**-এ থাকে। কোনো ব্যাকএন্ড সার্ভার নেই।

---

## ফিচার

- একাধিক আলাদা কনভারসেশন (একে অপরের সাথে মিশে না)
- প্রতিটি চ্যাটে আলাদা GitHub রিপোজিটরি সেট করা যায়
- AI যে ফাইলগুলো দেয় সেগুলো এক ক্লিকে GitHub-এ Push (নতুন/আপডেট)
- পুরো চ্যাট `.md` হিসেবে ডাউনলোড
- একক মেসেজ `.txt` হিসেবে ডাউনলোড
- এক্সট্র্যাক্টেড ফাইলগুলো `.zip` হিসেবে ডাউনলোড
- মোবাইল-ফ্রেন্ডলি UI + PWA (Add to Home Screen)

---

## দ্রুত শুরু (GitHub Pages – সবচেয়ে সহজ)

1. এই রিপোজিটরিটি আপনার GitHub-এ ফর্ক বা নতুন রিপো বানিয়ে কোড আপলোড করুন।
2. **Settings → Pages → Source**: `GitHub Actions` সিলেক্ট করুন।
3. `main` ব্রাঞ্চে পুশ করলে অটোমেটিক লাইভ সাইট তৈরি হবে।
4. মোবাইল ক্রোম/এজ থেকে সাইট ওপেন করে **Add to Home Screen** করুন → অ্যাপের মতো ব্যবহার করুন।

---

## GitHub Personal Access Token তৈরি (ফ্রি অ্যাকাউন্টেই সম্ভব)

1. GitHub-এ লগইন করুন।
2. উপরের ডানদিকে প্রোফাইল ছবি → **Settings**
3. নিচে স্ক্রল করে **Developer settings**
4. **Personal access tokens → Tokens (classic)**
5. **Generate new token (classic)**
6. Note দিন (যেমন: `AI Dev Studio`)
7. Expiration বেছে নিন
8. স্কোপ থেকে **`repo`** টিক দিন (পুরো রিপোজিটরি অ্যাক্সেসের জন্য)
9. Generate token → টোকেনটা কপি করে রাখুন (আর দেখা যাবে না)

অ্যাপে ⚙️ সেটিংস → GitHub Token বক্সে পেস্ট করে **রিপোজিটরি লোড করুন** বাটনে চাপুন।

> Fine-grained token ও ব্যবহার করা যায়, তবে Classic + `repo` scope সবচেয়ে সহজ।

---

## AI API Key সেটআপ

### DeepSeek (সাস্তা ও ভালো)
- Base URL: `https://api.deepseek.com/v1`
- Model: `deepseek-chat` বা `deepseek-reasoner`
- Key: [platform.deepseek.com](https://platform.deepseek.com) থেকে নিন

### xAI Grok
- Base URL: `https://api.x.ai/v1`
- Model: `grok-beta` / `grok-2` ইত্যাদি
- Key: [console.x.ai](https://console.x.ai) থেকে নিন

### OpenAI
- Base URL: `https://api.openai.com/v1`
- Model: `gpt-4o-mini` ইত্যাদি

যেকোনো OpenAI-compatible endpoint কাজ করবে।

---

## Capacitor দিয়ে Android APK বানানো (ঐচ্ছিক)

লোকাল মেশিনে বা CI-তে:

```bash
npm install
npx cap init "AI Dev Studio" com.aidevstudio.app --web-dir www
npx cap add android
npx cap sync
npx cap open android
```

Android Studio থেকে APK/AAB বিল্ড করুন।  
GitHub Actions-এ পূর্ণ Android বিল্ড করতে চাইলে আলাদা workflow + signing key লাগবে (আরও জটিল)।

---

## ব্যবহারের ফ্লো

1. সেটিংসে API Key + GitHub Token দিন → রিপো লোড করুন
2. নতুন কনভারসেশন খুলুন
3. ড্রপডাউন থেকে টার্গেট রিপো সিলেক্ট করুন
4. কোড লিখতে বলুন (AI ফাইলগুলো বিশেষ ফরম্যাটে দেবে)
5. **🚀 Push to GitHub** বাটনে চাপলে সরাসরি সেই রিপোতে কমিট হবে
6. চাইলে ZIP বা পুরো চ্যাট ডাউনলোড করুন

---

## নিরাপত্তা নোট

- API Key ও GitHub Token শুধু আপনার ডিভাইসের localStorage-এ থাকে।
- কোনো সার্ভারে পাঠানো হয় না (শুধু সরাসরি AI API ও GitHub API-তে)।
- পাবলিক ওয়াইফাইতে ব্যবহারের সময় সতর্ক থাকুন।
- Token-এ শুধু প্রয়োজনীয় `repo` পারমিশন দিন।

---

Made for mobile-first coding with AI + GitHub.
