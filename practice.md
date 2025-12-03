# TikTok Transcript Scraper

This script fetches TikTok video transcripts using the TikTok Research API
and saves them to a CSV file.

## Setup
1. Add your TikTok API credentials in the script:
   - CLIENT_KEY
   - CLIENT_SECRET
2. Add the usernames you want to collect transcripts from.

## Install Dependencies
pip install requests

## Run the Script
python script.py

## Output
Creates a CSV file containing:
- video id
- username
- caption
- like count
- view count
- transcript
