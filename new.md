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

## Features

- Authenticates via TikTok API using **client_credentials OAuth**  
- Queries videos for specific usernames  
- Filters by date range and optionally by region  
- Saves video metadata + transcripts into a CSV file  
- Handles multiple usernames with delay to prevent rate-limiting  

---

## Requirements

- Python 3.8+  
- TikTok Research API credentials (client key & client secret)  

**Python packages:**

```bash
pip install requests
Built-in modules used: csv, datetime, time

Setup
Get your TikTok Research API credentials:

CLIENT_KEY

CLIENT_SECRET

Open the script and fill in the credentials:

python
Copy code
CLIENT_KEY = "your_client_key_here"
CLIENT_SECRET = "your_client_secret_here"
Add TikTok usernames to scrape:

python
Copy code
USERNAMES = ["redditdailyvid", "storytime_confessions", "exampleuser"]
(Optional) Adjust the date range:

python
Copy code
start_date = date(2025, 11, 1)
end_date = date(2025, 11, 9)
(Optional) Change the output CSV filename:

python
Copy code
CSV_FILE = "tiktok_user_videos_and_transcripts.csv"
Usage
Run the script from your terminal:

bash
Copy code
python script_name.py
For each username, the script will:

Authenticate with TikTok API

Query videos in the specified date range

Retrieve transcripts (if available)

Append results to the CSV file

You will see progress printed in the console:

pgsql
Copy code
Access token obtained.
Retrieved 12 videos for 'redditdailyvid'
Retrieved 9 videos for 'storytime_confessions'
Captions + transcripts saved to tiktok_user_videos_and_transcripts.csv
Output
The CSV file contains:

id	username	caption	like_count	view_count	transcript
1234567890	exampleuser	“Am I the jerk for…”	15400	102300	"So this story begins when…"
...	...	...	...	...	...

This can be opened in Excel, Google Sheets, or used in Python for analysis.

Notes & Limitations
Not all videos may have transcripts (voice_to_text may be null)

Some usernames may not be eligible depending on API permissions

TikTok API rate limits apply; the script includes delays to prevent hitting them

Customization
You can modify the script to:

Change the date range

Remove or adjust region filtering

Add more fields from TikTok videos

Export JSON instead of CSV

Query hashtags or trending videos instead of usernames

License
Specify your license here (e.g., MIT, GPL) if sharing publicly.
