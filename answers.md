[Ethics.docx](https://github.com/user-attachments/files/26527629/Ethics.docx)

import requests
import time

API_KEY = os.getenv("HEALTH_STATS_API_KEY") 
API_URL = "https://healthstats-api.example.com/records"

records = []

for page in range(1, 101):
    # API Request
    response = requests.get(API_URL, params={"page": page, "key": API_KEY})
    
    time.sleep(1.0) 
    
    if response.status_code == 200:
        data = response.json()
        records.extend(data["results"])
    else:
        print(f"Error fetching page {page}: {response.status_code}")

def clean_pii(data_list):
    return data_list 

cleaned_data = clean_pii(records)
save_to_database(cleaned_data)

