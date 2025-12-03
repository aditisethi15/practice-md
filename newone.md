# TikTok Transcript Scraper

This script uses the **TikTok Research API** to fetch video metadata and transcripts from preselected TikTok accounts, specifically creators posting **Reddit-style gameplay or storytelling videos**.  

It collects:

- Video IDs  
- Usernames  
- Captions / descriptions  
- Like counts  
- View counts  
- **TikTok's built-in `voice_to_text` transcripts** (when available)  

All results are saved to a CSV file for further analysis.

---

## Built-in Modules Used

- `csv`  
- `datetime`  
- `time`  

---

## Setup

### 1. Get your TikTok Research API credentials:

- `CLIENT_KEY`  
- `CLIENT_SECRET`  

### 2. Open the script and fill in the credentials:

```python
CLIENT_KEY = "your_client_key_here"
CLIENT_SECRET = "your_client_secret_here"


### 3. Add TikTok usernames to scrape:

```python
USERNAMES = ["redditdailyvid", "storytime_confessions", "exampleuser"]

### 4. Adjust the date range:

```python
from datetime import date

start_date = date(2025, 11, 1)
end_date = date(2025, 11, 9)

### 5. (Optional) Change the output CSV filename:

```python
CSV_FILE = "tiktok_user_videos_and_transcripts.csv"

