# Loudoun County Pollution Reporting System

A web-based application that allows citizens to report environmental pollution issues in Loudoun County and enables community volunteers to view, upvote, and comment on submitted reports.  
This project uses **Google Maps**, **Supabase**, **Client-side JavaScript**, and **HTML/CSS**.

---

## 🚀 Features

### **Citizen Report Page (`index.html`)**
- Interactive **Google Maps marker** to pinpoint pollution locations.
- Input fields for:
  - Full name  
  - Email  
  - Pollution description  
  - Image uploads (supports multiple)
- Live image preview before submission.
- Uploads photos to a storage bucket.
- Saves a pollution report to **Reports** including:
  - Latitude / longitude  
  - Name + email  
  - Complaint text  
  - Array of image URLs  
  - Timestamp  
  - Upvotes (default: 0)  
  - Comments & comment timestamps

---

### **Volunteer Reports Page (`volunteerPage.html`)**
- Displays all submitted reports in a responsive card gallery.
- Each card includes:
  - Shortened complaint title  
  - First image preview  
  - Timestamp  
  - Upvote button
- Clicking a card opens a **dialog with full details**, including:
  - Full report text  
  - Reporter’s name & email  
  - All uploaded images  
  - A map showing the exact coordinates  
  - Comment section with timestamps  
- Comments are saved in Supabase as arrays:

---


---

## 🧰 Technologies Used

- **HTML5 + CSS3**
- **Vanilla JavaScript**
- **Google Maps JavaScript API**
- **Supabase**
  - Database (PostgreSQL)
  - Storage (image uploads)
  - REST API for CRUD operations




## 🧪 How It Works (Brief Overview)


### **Submitting a Report**
1. User fills out the form and selects a location on the map.
2. Images are uploaded to **Supabase Storage**.
3. The report is saved in the **Reports** table with all associated image URLs.
4. User receives a confirmation that the report was successfully submitted.

---

### **Viewing Reports**
- Reports are displayed in a **gallery-style layout**.
- Each card shows:
  - A shortened version of the complaint  
  - A preview image  
  - Upvote count  
  - Timestamp  
- Clicking a report opens a **modal dialog** containing:
  - Full complaint text  
  - Reporter’s name and email  
  - All uploaded images  
  - A Google Maps view centered on the pollution location  
  - A comment submission area  

---

### **Commenting**
- New comments are appended to the existing:
  - `comments` array  
  - `comment_date` array  
- Comments appear immediately and persist for all future visitors.

---

## 📌 Future Improvements (Optional)
- Add volunteer authentication  
- Add spam filtering or rate limiting  
- Integrate AI-based description analysis  
- Support image deletion or editing  
- Add sorting (e.g. newest, most upvoted, most commented)  



