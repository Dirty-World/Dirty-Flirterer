# 🚀 Dirty Flirterer

**Effortless, flirty engagement for your Telegram group** 💖

**Dirty Flirterer** by **dirty‑world** is a plug‑and‑play Telegram bot that automatically schedules:

- 💌 **Daily Dirty Questions**  
  1,460 flirty “Question of the Day” prompts (4 years’ worth), with `/dirtyqotd skip` to reshuffle on demand.

- 🎲 **Dirty Quizzes**  
  1,460 pop‑culture quizzes plus admin controls:  
  `/adddirtyquiz`, `/listdirtyquizzes`, `/removedirtyquiz`, `/dirtyquiz skip`.

- 🏅 **Dirty Points & Leaderboards**  
  Weekly (`/dirtyweekly`), monthly (`/dirtymonthly`), and yearly (`/dirtyyearly`) leaderboards, auto‑resetting and purging inactive users.  

- 🎉 **Dirty Events**  
  Preloaded monthly celebrations & major holidays (New Year’s, Easter, 4 Jul, Thanksgiving, Christmas).  
  Admins can add custom dates via `/dirtyaddevent`, with auto‑pin 🎯 and group‑name updates 🔖.

- 💬 **Dirty Nudges**  
  Random @mention‑style flirt‑nudges in chat. Configurable window & cap: `/dirtynudgeconfig`.  

- 🕹️ **Dirty Games**  
  A library of 200 interactive game cards (`/dirtyplay`, `/dirtygameinfo`, `/dirtyskip`, `/dirtyaddgame`) to break the ice 🔥.

- 📊 **Dirty Reports & Follow‑Up**  
  Engagement analytics (`/dirtyreport`) and automated pings for low‑engagement members (`/dirtyfollow`) in your admin or main group 🚀.

Everything runs on **Google Cloud Functions** + **Firestore** with **Cloud Scheduler** RRULE triggers—no extra admin work, zero PII stored.  

---

## 🛠️ Installation & Setup

1. **Clone & Install**  
   ```bash
   git clone https://github.com/dirty-world/dirty-flirterer.git
   cd dirty-flirterer
   npm install      # or `pip install -r requirements.txt`
   Provision Infra
2. Provisioning Infra
   Use Terraform to set up Firestore & Cloud Scheduler jobs.

3. Deploy Bot
Deploy Cloud Functions and configure your Telegram webhook.

4. Configure
Set BOT_TOKEN, chat_id, time windows, and optional admin_chat_id in .env or Firestore.

5. Enjoy
Sit back and watch Dirty Flirterer keep your group flirty, fun, and fully engaged ✨.
