# 🤖 Insta Reels Bomber Bot (n8n)
🚀 A goofy AI bot that annoys your friends every hour with random Instagram reels. Because why not?

🌟 What Does It Do?
✅ Picks a random Instagram reel from my list
✅ Sends it automatically to my friends on Telegram
✅ Runs every hour (or whenever I feel like it)
✅ Fully built in n8n (the no-code/low-code automation tool)

🎬 How It Works
I keep a list of my favorite reels (links)

The bot picks one randomly

Sends it to a list of my friends’ Telegram chat IDs

My friends either love me or block me 😎

🔧 How I Built It
Tools
n8n — my favorite workflow tool

Telegram Bot API — for spamming friends nicely

A bit of JavaScript — for picking random reels

⚙️ n8n Workflow Steps
Schedule Trigger → runs hourly

Code Node → picks a random reel:

js
Copy
Edit
const reels = JSON.parse([reels]);
const randomReel = reels[Math.floor(Math.random() * reels.length)];
return [{ json: { reel: randomReel } }];
Set Node → list of chat IDs

Split Out Node → loops through chat IDs

Merge Node / Set Node → merges each chatId with the random reel

Telegram Node → sends the message:

kotlin
Copy
Edit
Check out this reel: {{ [reel] }}
🤯 Why?
Because I wanted to:

“Build an AI agent that sends reels to my friends every one hour.”

…and because I’m slightly unhinged.
