# Tech Conference Website

## 🚀 Project Overview
This is a **Tech Conference Website** built using **SvelteKit**. It provides an interactive interface for users to browse conference sessions, filter events by day and category, and access an embedded Google Map for location details.

## ✨ Features
- **Dynamic Filtering**: Users can filter sessions by day and track (Main Stage, Tech Talks, Security, etc.).
- **Responsive Design**: Fully optimized for mobile, tablet, and desktop screens.
- **Session Listings**: Displays details about conference sessions with title, time, and track.
- **Google Maps Integration**: Embedded Google Map for easy navigation to the venue.
- **SvelteKit Framework**: Fast and optimized for performance.

---

## 🛠️ Installation & Setup

### **1. Clone the Repository**
```sh
git clone https://github.com/yourusername/tech-conference.git
cd tech-conference
```

### **2. Install Dependencies**
```sh
npm install
```

### **3. Start the Development Server**
```sh
npm run dev
```
By default, the project runs on **http://localhost:5173/**.

---

## 📂 Project Structure
```
tech-conference/
│── src/
│   ├── routes/
│   │   ├── +layout.svelte     # Main layout file
│   │   ├── +page.svelte       # Homepage
│   │   ├── contact/
│   │   │   ├── +page.svelte   # Contact Page (with Google Maps)
│   ├── components/
│   │   ├── Filter.svelte      # Filter buttons for sessions
│   │   ├── SessionCard.svelte # Component for displaying sessions
│── static/                    # Static assets (images, icons, etc.)
│── package.json
│── README.md
│── svelte.config.js
```

---

## 📌 How to Use
1. Visit the website and browse through the **sessions list**.
2. Use the **filter buttons** to view sessions for different days or tracks.
3. Navigate to the **Contact Page** to view the venue location on Google Maps.
4. The site is fully responsive and works well on **mobile devices**.

---

## 🏗️ Deployment
You can deploy the SvelteKit app on platforms like **Vercel, Netlify, or Firebase Hosting**.

### **Deploy on Vercel**
```sh
npm run build
vercel deploy
```

### **Deploy on Netlify**
```sh
npm run build
netlify deploy
```

---

## 🎯 Future Enhancements
- **Session Details Page**: Dedicated pages for each session with speaker info.
- **User Authentication**: Allow attendees to bookmark sessions.
- **Dark Mode**: Improve UI with a theme switcher.

---

## 📜 License
This project is open-source under the **MIT License**.

---

## 💡 Contributions
Contributions are welcome! Feel free to submit a pull request or open an issue.

👨‍💻 **Developed by Hamza Khan
