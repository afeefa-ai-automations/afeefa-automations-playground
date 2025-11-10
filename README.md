# 🤖 AI Marketing Assets Generator (n8n Workflow)


An automated n8n workflow that creates **marketing visuals (ads, Instagram posts, and stories)** from a product link — all powered by AI.  
This system connects **Google Sheets, AI models, and automation tools** to streamline the entire creative process.

---

## 🎯 Overview

The **AI Marketing Assets Generator** is designed to automatically:
1. Fetch product details from a Google Sheet.
2. Download and clean the product image (remove background).
3. Generate AI-based marketing prompts.
4. Convert and merge assets (text + visuals).
5. Create ad, post, and story images.
6. Upload them to Google Drive.
7. Update the Google Sheet with generated file links.

All this happens in a single automated flow — saving hours of repetitive work for marketing teams.

---

## 🧩 Workflow Breakdown

### **Step 1: Get the Data**
- **Trigger:** Google Sheets
- **Action:** Fetch product link and extract info
- **Result:** Updates Google Sheet with processing status

### **Step 2: Download & Remove Background**
- Downloads product image
- Removes the background using an external API (`remove.bg` or similar)

### **Step 3: Generate and Align Prompts**
- AI prompt generation using **Google Gemini Chat Model**
- Custom **JavaScript** node to structure prompt outputs

### **Step 4: Divide Prompts**
- Splits prompts for different asset types (Ad / Post / Story)

### **Step 5: Convert Image to Base64**
- Converts the cleaned product image into Base64 format for easier transmission

### **Step 6: Merge Prompts & Images**
- Combines prompts and image data into a unified payload for each creative type

### **Step 7: Clean & Align Merge Inputs**
- Final formatting and preparation before sending to image generation endpoints

### **Step 8: Image Generation**
- Generates AI marketing visuals via API calls:
  - **Ad Image**
  - **Instagram Post**
  - **Instagram Story**

### **Step 9: Convert & Save**
- Converts generated Base64 strings into image files

### **Step 10: Create Folder**
- Automatically creates a new folder in Google Drive for each product

### **Step 11: Upload Files**
- Uploads generated visuals into the folder

### **Step 12: Update Google Sheets**
- Appends generated image links back into the sheet for tracking

---

## 🧠 Tools & Integrations Used

| Tool / Service | Purpose |
|----------------|----------|
| 🧾 **Google Sheets** | Input + output management |
| 🧰 **n8n** | Workflow automation |
| 🖼 **Remove.bg / Similar API** | Image background removal |
| 💬 **Google Gemini AI** | AI text prompt generation |
| 💾 **Google Drive** | File storage and folder creation |
| 🧑‍💻 **Custom JS Nodes** | Data formatting and logic alignment |

---

## 🚀 How to Use

1. Clone this repository and import the workflow JSON into your **n8n instance**.  
2. Connect your credentials for Google Sheets, Google Drive, and any AI APIs.  
3. Adjust API endpoints if necessary (e.g., for background removal or image generation).  
4. Set up your **Google Sheet** with columns for:
   - Product link  
   - Product name  
   - Generated asset URLs  
5. Click **“Execute Workflow”** and let automation do the rest.

---

## 🎥 Demo Video

Watch the workflow in action here:  
👉 [**Video Walkthrough**](https://www.kapwing.com/w/hUzsBwXJIa)

*(Replace with your actual video link once ready.)*

---

## 💡 Future Enhancements

- Add caption and hashtag generation using AI  
- Auto-publish to social media (Instagram, Facebook, LinkedIn)  
- Include brand color and logo integration  
- Enable client dashboard to view generated assets  

---

## 🏷 License

This project is for educational and creative automation purposes.  
Feel free to modify and extend it as per your marketing needs.

---

**Author:** Tasneem Afeefa  
**Tagline:** *"Automate Creativity — The Future of Marketing."*
