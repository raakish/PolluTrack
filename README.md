# PolluTracker

Hello, my name is Ackshat Tiwari, and I am very excited to share the project which I have made, PolluTrack. This app helps Loudoun County by allowing users to identify, assess, respind to, and upvote pollution incidents that are taking place within the county. I will talk about the **Features**, **Tech Stack**, **Impacts**, **What's next**, and **How to set up**. Keep reading for more.

---

## 🚀 Features

### **Citizen Report Page (`index.html`)**
Initially, there is a citizens page where residents of Loudoun County can identify pollution and submit online reports explaining pollution. Here is what my program can allocate:
- Location, based on an interactive map
- Name and email
- A text box where you can describe the pollution
- Image uploading
Users are envouraged to providing a concise but understandable description of the pollution so that other people can understand it.

---

### **Volunteer Reports Page (`volunteerPage.html`)**
- Displays all the reports in a gallery layout
- Each report card shows the following:
 - Short Title
 - Uploaded Images
 - Date
 - Upvote count and upvote button
- When you click it, it shows the full complaint, a map hihglighting the location, and a comment box where you can post and view comments for the report.


---


## 🧰 Technologies Used

- **HTML5 + CSS3**
- **JavaScript**
- **Google Maps API**
- **Supabase**
  - Database table
  - Storage bucket

---


## 💥 Impacts
- Provides a grassroots solution to tacking pollution
  - The platform empowers residents to easily report pollution issues, helping raise awareness about local environmental problems that might otherwise go unnoticed.
- Improved response and cleanup efforts
  - Volunteers and environmental groups get real-time access to reports, photos, and coordinates — making it easier to prioritize and carry out cleanup or investigative actions.
- Provides data for long term environmental planning
  - Stored reports provide valuable long-term data for:
   - Tracking pollution trends  
   - Identifying repeat offenders or hotspots  
   - Supporting environmental policy decisions


---


## 📌 Future Improvements
- Incorportate spam-filtering features to block automated or false reports.
- Integrate AI-based description analysis
- Add sorting (e.g. newest, most upvoted, most commented), and advanced search filters
- Turn into an app, for easier access on mobile phones

---

## How to set up
This setup might feel lengthy because the program itself would not function. This is because the API keys provided in the code are placeholders, and would not let the program work. You need to set up a database table on Supabase, your own URL and key, and a storage bucket with the same path below. 

Your database must contain the following columns. The rows are not required, but they are some sample data that would be collected.

| id  | created_at         | fullName      | email             | longitude | latitude | complaint         | image_url         | upvotes | comments        | comment_date       |
|-----|------------------|---------------|-----------------|-----------|---------|-----------------|-----------------|--------|----------------|------------------|
| 1   | 2025-11-15 16:00:15.845797+00 | John Doe      | john@example.com | -122.42   | 37.77   | Litter everywhere | http://img.com/1 | 5      | [c1], [c2], [c3]   | [d1], [d2], [d3] |
| 2   | 2025-11-23 23:17:50.461556+00 | Jane Smith    | jane@example.com | -122.43   | 37.78   | Chemical runoff | http://img.com/2 | 3      | [c4], [c5]    | [d4], [d5] |

A storage bucket must be designed as well for images to be stored in. The bucket will follow a path like this, where images is the name of the bucket.

```images/
└── reports/
    └── images/
        ├── sample_image_1.jpg
        └── sample_image_2.png
```
