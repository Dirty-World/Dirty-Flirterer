# 🚀 Dirty Flirterer

![7cde5724-d95b-483f-85b2-8d7b946b496e](https://github.com/user-attachments/assets/9b50e446-ac4e-4e5f-9ee4-0eed865dd57f)


**Effortless, flirty engagement for your Telegram group** 💖

**Dirty Flirterer** by **dirty‑world** is a plug‑and‑play Telegram bot that automatically schedules:

- 💌 **Daily Dirty Questions**  
  1,460 flirty "Question of the Day" prompts (4 years' worth), with `/dirtyqotd skip` to reshuffle on demand.

- 🎲 **Dirty Quizzes**  
  1,460 pop‑culture quizzes plus admin controls:  
  `/adddirtyquiz`, `/listdirtyquizzes`, `/removedirtyquiz`, `/dirtyquiz skip`.

- 🏅 **Dirty Points & Leaderboards**  
  Weekly (`/dirtyweekly`), monthly (`/dirtymonthly`), and yearly (`/dirtyyearly`) leaderboards, auto‑resetting and purging inactive users.  

- 🎉 **Dirty Events**  
  Preloaded monthly celebrations & major holidays (New Year's, Easter, 4 Jul, Thanksgiving, Christmas).  
  Admins can add custom dates via `/dirtyaddevent`, with auto‑pin 🎯 and group‑name updates 🔖.

- 💬 **Dirty Nudges**  
  Random @mention‑style flirt‑nudges in chat. Configurable window & cap: `/dirtynudgeconfig`.  

- 🕹️ **Dirty Games**  
  A library of 200 interactive game cards (`/dirtyplay`, `/dirtygameinfo`, `/dirtyskip`, `/dirtyaddgame`) to break the ice 🔥.

- 📊 **Dirty Reports & Follow‑Up**  
  Engagement analytics (`/dirtyreport`) and automated pings for low‑engagement members (`/dirtyfollow`) in your admin or main group 🚀.

Everything runs on **Google Cloud Functions** + **Firestore** with **Cloud Scheduler** RRULE triggers—no extra admin work, zero PII stored. Uses **Workload Identity Federation** for secure, keyless authentication between GitHub Actions and Google Cloud.

---

## 🛠️ Installation & Setup

1. **Clone & Install**  
   ```bash
   git clone https://github.com/dirty-world/dirty-flirterer.git
   cd dirty-flirterer
   npm install      # or `pip install -r requirements.txt`
   
2. Provisioning Infra
   Use Terraform to set up Firestore & Cloud Scheduler jobs.

3. Deploy Bot
Deploy Cloud Functions and configure your Telegram webhook.

4. Configure
Set BOT_TOKEN, chat_id, time windows, and optional admin_chat_id in .env or Firestore.

5. Enjoy
Sit back and watch Dirty Flirterer keep your group flirty, fun, and fully engaged ✨.

---

## 💰 Free Tier Optimization

Dirty Flirterer is designed to run entirely within Google Cloud Platform's free tier limits, just like its sibling projects. Here's how we keep it cost-free:

### 🔒 Security & Authentication

- **Workload Identity Federation**:
  - Secure authentication without service account keys
  - Uses OpenID Connect (OIDC) tokens from GitHub Actions
  - Short-lived credentials instead of long-lived service account keys
  - Repository-specific access control
  - Automatic credential rotation

### 🔄 Resource Optimization

- **Cloud Functions**:
  - 128MB memory allocation (minimum)
  - 60-second timeouts
  - Efficient cold starts
  - Minimal dependencies

- **Firestore Usage**:
  - Batched reads/writes
  - Caching for high-frequency data
  - Time-based document updates
  - Efficient data structures

- **Cloud Scheduler**:
  - Consolidated jobs (fewer triggers)
  - Optimized RRULE expressions
  - Staggered scheduling

### 📊 Data Management

- **Storage Efficiency**:
  - Minimal data retention
  - Compressed content where possible
  - Automatic cleanup of old records
  - Efficient indexing

- **API Calls**:
  - Rate limiting with backoff
  - Cached responses
  - Batched operations
  - Minimal external dependencies

### 🛠️ Development Practices

- **Testing**: Local testing before deployment
- **Monitoring**: Budget alerts at 80% and 100% thresholds
- **Deployment**: Optimized package sizes under 100MB
- **Error Handling**: Graceful degradation when approaching limits

Following these optimization practices ensures Dirty Flirterer remains completely free to run while maintaining all functionality.
