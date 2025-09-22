🎉 PKC Benchmark Tool (In Development)
TL;DR: After 2 months of using this AI benchmark tool for myself, I'm releasing it into the wild with a "they'll figure it out" attitude. lol

🚨 WARNING: I'm Just Throwing This Out There
"If you're expecting perfect software, please press the back button now."

This project is released based on the following philosophy:

✅ It's good enough for me.

✅ It might be helpful to someone else.

❌ I do NOT guarantee it works perfectly in every environment.

❌ I do NOT operate a 24/7 customer support center.

🤷‍♂️ If it doesn't work, fork it and fix it yourself.

🎯 The Miracle of One-Click
For those of you thinking, "Python? Virtual environments? What's that?"—this is for you:

For Windows Users
1. Double-click OneClick_RUN.bat
2. ☕ Grab a cup of coffee and wait.
3. A browser tab will open automatically.
4. Done.

For macOS Users
1. Double-click OneClick.command
2. See a "malicious software" warning? → Right-click and select "Open".
3. A terminal will pop up with a bunch of text.
4. Done.

For Linux Users
chmod +x oneclick.sh
./oneclick.sh
# You're a pro, you don't need instructions.

All installations happen inside a dedicated jail called .pkc-venv, so your system is safe.

🤖 What's New: The Evolution
Version

Status

Description

v3

🏗️

"Ugh, mobile support is a pain." → Decided to be desktop-only.

v4

🧠

"Just detect the GPU already!" → Auto-selects CUDA/MPS/CPU.

v5

🎯

"How can normies use this without one-click?" → Automated venv setup.

v5.3

💅

"The UI is too clunky." → Slimmed down and right-aligned input fields.

v5.4

📝

"One prompt isn't enough." → Expanded to 3 prompt fields.

v5.5

🌐

"What about English users?" → Auto-detects browser language.

v5.6

🚀

"Give me all the F1 features!" → Integrated HuggingFace search/download.

🎮 How to Use: A 3-Step Guide Even a Fool Could Follow
Step 1: Run It
Choose one of the one-click methods above.

If something pops up in your browser, you're golden.

Step 2: Get a Model
If you have local models: They will be detected automatically.

If not: Click the "Download Model" button → Search on HuggingFace → Download with one click.

Recommended keywords: "llama", "korean", "bllossom"

Step 3: Benchmark
Enter your test sentences into the 3 prompt fields (empty ones are skipped).

Select the model checkboxes.

Click "Start Benchmark".

Watch the results appear in real-time.

That's it! You can check the results in the Summary/Log/Chart/Compare tabs and save them as an HTML file.

📊 Real-World Performance: Based on an RTX 2060 SUPER
For those wondering, "Can my PC even run AI?", here's some real data:

Model

VRAM

Speed

Quality

TL;DR

Bllossom-3B

4.2GB

80 TPS

⚠️

Fast, but mixes languages.

Bllossom-8B

6.9GB

46 TPS

✅

Slower but stable Korean.

Conclusion: 3B is for demos, 8B is for practical use. An RTX 2060-class GPU can handle the 8B model just fine.

🌏 Multilingual Support: The Age of Globalization
The UI automatically changes based on your browser's language:

🇰🇷 Korean: The default, obviously.

🇺🇸 English: For the AI researchers.

🇯🇵 Japanese: For those who wandered in while reading webtoons.

🇨🇳 Chinese: Both Simplified and Traditional supported.

However, the name "PKC Benchmark Tool MARK" remains the same in all languages. I will not compromise on brand identity. lol

⚠️ Compatibility Disclaimer (Please Read)
✅ Environments Where It Will Probably Work Fine
Windows 10/11 + NVIDIA GPU

macOS (Apple Silicon)

Ubuntu/Debian + a decent GPU

🤔 Environments Where It Might Work
Windows 7/8 (too old)

Linux + AMD GPU (ROCm is complicated)

Virtual Machines (GPU passthrough issues)

❌ Environments Where It Definitely Won't Work
Mobile devices (intentionally blocked)

RAM less than 4GB (just give up)

No internet connection (can't download from HuggingFace)

Don't get mad if it doesn't run. I originally built this just for my own machine anyway.

🤝 The Spirit of Open Source & License
PKC Non-Commercial Attribution License v1.0

What You CAN Do:
✅ Use it freely (personal/educational/research)

✅ Dig into the code

✅ Improve it and redistribute

✅ Fork it and create something completely new

What You CANNOT Do:
❌ Sell it for money

❌ Claim you made it

❌ Remove the PKC attribution

What I Ask of You:
🙏 Let me know if you find a bug (fixing it is another story)

🙏 Share any new features you add

🙏 Help translate the documentation

🎭 A Candid Confession from the Developer
Me, 2 months ago:
"Hey AI, just build me a chatbot that works on my PC specs."

Me, now:
"Huh, I ended up building a whole benchmark tool... It's a waste to keep it to myself, so I'll just release it."

Me, in the future (probably):
"Why did I release this..."

🚀 Download & Get Started
GitHub (Coming Soon)
git clone [Repository URL]
cd PKC-Benchmark-Tool
# For Windows
OneClick_RUN.bat
# For macOS/Linux
chmod +x oneclick.sh && ./oneclick.sh

Direct Download
Download the ZIP file → Unpack it → Run the one-click script.

📞 Contact & Support
Get in Touch
📧 Email: pkc0412@gmail.com

🌐 Blog: https://pkcproject.blogspot.com/

💬 GitHub Issues: (Opening soon)

Support Policy
Bug Reports: Welcome (whether I fix them depends on my mood).

Feature Requests: Make it yourself and send a PR.

"How-to" Questions: Read the README first.

Philosophical Debates: I'm open to coffee chats.

🎪 One Last Thing
This tool is not "perfect software."
It's just a "useful tool."

It's okay if it has bugs, compatibility issues, or poor documentation.
I made it with a "they'll figure it out" mentality.

Use it, improve it, share it.
Isn't that the true spirit of open source?

Made with ❤️ and lots of ☕ by PKC

"Release it, even if it's not perfect, and let the community make it better."

P.S. I fully expect someone to write a better version of this announcement and send me a PR. lol
