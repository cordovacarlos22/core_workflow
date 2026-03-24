# 🚚 CargoFlow Lite

CargoFlow Lite is a fullstack logistics workflow application designed to automate load creation using AI and streamline communication between drivers and administrators.

This project is inspired by real-world trucking operations, where drivers handle Bill of Lading (BOL) documents and manual processes slow down workflows.

---

## ✨ Overview

CargoFlow Lite allows drivers to upload a photo of a Bill of Lading (BOL), automatically extracts key shipment data using AI, and creates a load record associated with that driver.

Instead of relying on manual data entry by administrators, this system shifts the workflow to drivers while maintaining accuracy through human validation.

---

## 🧠 Key Concept

> AI acts as a **copilot, not autopilot**.

- AI assists with extracting structured data from documents  
- Drivers review and confirm extracted information before submission  
- Admins focus on monitoring and validation instead of manual input  

---

## ⚙️ Features

### 🚛 Driver Features
- Secure authentication (JWT-based)
- Upload Bill of Lading (image)
- AI-powered data extraction (planned: AWS Textract / Vision API)
- Review and edit extracted fields
- Submit loads automatically linked to driver
- Complete delivery checklist
- View assigned and completed loads

### 🧑‍💼 Admin Features
- View all submitted loads
- Filter by driver, status, or date
- Inspect uploaded BOL images
- Review extracted shipment data
- Monitor checklist completion
- Edit/correct load details if needed

---

## 📄 Data Extracted from BOL

The system extracts key logistics fields such as:

- Shipment Plan ID (Load Number)
- Plant Code
- Vehicle ID (Trailer Number)
- Customer Number
- Bill of Lading Number
- Delivery (Ship To) Name and Address
- Delivery Phone Number
- Shipping Comments (e.g., Seal)
- Document Date

Pickup location is standardized: ontario, CA

---

## 🧱 Tech Stack

### Frontend
- React (Vite)
- Tailwind CSS
- React Router DOM
- Axios
- React Hook Form
- Yup (validation)
- Sileo (toast notifications)

### Backend
- Node.js
- Express
- MongoDB
- Mongoose
- JWT Authentication
- Multer (file upload)
- Cloudinary / AWS S3 (image storage)

### AI / Cloud (Planned)
- AWS Textract (document text extraction)
- AWS Rekognition (future: load securement validation)

---

## 🏗️ Architecture
Client (React)
↓
API (Express / Node.js)
↓
Database (MongoDB)
↓
Cloud Storage (Cloudinary / S3)
↓
AI Services (Textract / Vision Models)

---

## 🔄 Application Flow

### Driver Workflow
1. Log in
2. Upload BOL image
3. AI extracts shipment data
4. Driver reviews and edits fields
5. Load is created and assigned automatically
6. Driver completes checklist throughout delivery

### Admin Workflow
1. Log in
2. View all submitted loads
3. Review extracted data and BOL image
4. Monitor checklist progress
5. Filter and manage loads

---

## 📁 Project Structure

cargoflow-lite/
client/     # React frontend
server/     # Node.js backend

---

## 🚀 Getting Started

### 1. Clone the repository
git clone https://github.com/your-username/cargoflow-lite.git
cd cargoflow-lite

---

### 2. Setup Backend

cd server
npm install

Create `.env` file:

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

Run server:

npm run dev

### 3. Setup Frontend

cd client
npm install
npm run dev

---

## 🧪 Future Improvements

- 📸 Load securement validation using computer vision
- 📍 Real-time load tracking (GPS integration)
- 📄 PDF support for BOL uploads
- 🔔 Notifications for load updates
- 📊 Analytics dashboard for operations
- 🏢 Multi-tenant support for logistics companies

---

## 💡 Why This Project Matters

CargoFlow Lite demonstrates:

- Real-world problem solving in logistics
- Fullstack application design
- AI integration with human validation
- Scalable workflow automation
- Strong understanding of operational systems

---

## 👨‍💻 Author

Carlos Cordova  
Full Stack Developer | Cloud Enthusiast  


---

## 📜 License

This project is for educational and portfolio purposes.