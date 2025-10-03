# Blotato Social Publisher (n8n Workflow)

## 📌 Overview
This repository contains an **n8n workflow** that automates the entire process of:
1. Generating short video scripts with AI.  
2. Creating and rendering faceless videos via **Blotato**.  
3. Automatically publishing the videos across multiple social platforms (Instagram, Facebook, LinkedIn, Threads, TikTok, YouTube, etc.).  

It is designed for creators who want to **automate short-form video production and publishing** without manual editing or posting.

---

## ⚙️ Features
- 🧠 **AI Agent**: Brainstorms ideas, writes scripts, and captions.  
- 🎬 **Video Creation**: Uses Blotato API to generate videos with captions, voice, and animations.  
- ⏳ **Wait & Fetch**: Polls until video rendering is complete.  
- 📤 **Social Publishing**: Publishes automatically to multiple platforms.  
- 🗓 **Schedule Trigger**: Runs daily at a specified time.  

---

## 📂 Repository Structure
blotato-social-publisher-n8n/
│
├── README.md # Project documentation
├── workflows/
│ └── workflow.json # Exported n8n workflow
├── assets/
│ └── diagram.png # (Optional) workflow diagram or screenshots
└── config/
└── sample.env # Environment variable template

---

## 🔑 Setup

### 1. Prerequisites
- [n8n](https://n8n.io) installed (self-hosted or cloud).  
- A **Blotato API key** (sign up at [blotato.com](https://blotato.com)).  
- Accounts for the social platforms you want to publish to.

### 2. Import Workflow
- In n8n, go to **Workflows → Import from File**.  
- Import `workflows/workflow.json`.  

### 3. Configure Environment
Create a `.env` file based on `config/sample.env`:
```env
BLOTATO_API_KEY=your_api_key_here
INSTAGRAM_ID=your_instagram_account_id
FACEBOOK_ID=your_facebook_account_id
FACEBOOK_PAGE_ID=your_page_id
LINKEDIN_ID=your_linkedin_id
THREADS_ID=your_threads_id
TIKTOK_ID=your_tiktok_id
YOUTUBE_ID=your_youtube_id
PINTEREST_ID=your_pinterest_id
PINTEREST_BOARD_ID=your_board_id
BLUESKY_ID=your_bluesky_id
4. Run the Workflow
Enable the Schedule Trigger node.
The workflow will generate, render, and publish videos automatically at the scheduled time.
