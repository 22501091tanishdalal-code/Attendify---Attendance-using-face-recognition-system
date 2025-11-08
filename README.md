
# **Attendify – Multi-Person Face Recognition Attendance System**

Attendify is a real-time attendance system powered by **InstaFaceLibrary**, using **KNN** and **SVM** for accurate face classification. It detects and recognizes multiple people in a single frame, marks their attendance automatically, and stores all records securely through **Supabase**. The system is designed for classrooms, offices, and team environments that require fast, contactless, and proxy-proof attendance tracking.

---

## ✅ **Features**

* **Multi-Person Detection:** Recognizes multiple faces at the same time.
* **Real-Time Recognition:** Fast processing using InstaFaceLibrary.
* **Hybrid Classification:** Uses both **KNN** and **SVM** for optimal accuracy.
* **Secure Data Storage:** Integrates with **Supabase** for attendance logs and user data.
* **Easy Enrollment:** Add new users with just a few images.
* **Scalable:** Works with small datasets (10–20 users) and can expand with external datasets.

---

## 📌 **Tech Stack**

* **Python**
* **InstaFaceLibrary**
* **KNN & SVM Classifiers**
* **OpenCV**
* **Supabase**
* **NumPy / Pandas**

---

## 🛠️ **How It Works**

1. **Face Detection**
   The system detects all faces present in the input frame using InstaFaceLibrary’s fast detectors.

2. **Embedding Extraction**
   Each detected face is converted into a high-dimensional embedding vector.

3. **Classification (KNN + SVM)**

   * **KNN** handles quick matching and neighbor comparison.
   * **SVM** provides strong separation for visually similar faces.

4. **Attendance Marking**
   Recognized faces are logged and sent to Supabase along with timestamps.

5. **Dashboard / Interface**
   Attendance data can be viewed or managed through your Supabase dashboard or custom UI.

---

## 🧩 **Project Structure**

```
Attendify/
│── data/               # Training images & embeddings
│── models/             # Saved KNN & SVM models
│── src/
│    ├── detect.py      # Multi-face detection
│    ├── train.py       # Training script (KNN + SVM)
│    ├── recognize.py   # Real-time recognition
│    ├── supabase.py    # Supabase integration
│── requirements.txt
│── README.md
```

---

## 🚀 **Getting Started**

### **1. Clone the Repository**

```
git clone https://github.com/your-username/Attendify.git
cd Attendify
```

### **2. Install Requirements**

```
pip install -r requirements.txt
```

### **3. Add Training Images**

Place images inside the `data/` folder with subfolders per person.

### **4. Train the Model**

```
python src/train.py
```

### **5. Run Attendance System**

```
python src/recognize.py
```

---

## 🗂️ **Database Setup (Supabase)**

1. Create a project in Supabase
2. Add a table: `attendance`
3. Columns:

   * `id` (uuid)
   * `name` (text)
   * `timestamp` (timestamptz)
   * `image_url` (for recognition)
4. Paste your **API URL** and **Anon Key** into `supabase.py`

---

## 📸 Demo

Add screenshots or GIFs showing:

* Multi-person detection
* Real-time recognition
* Attendance logs in database

---

## 🤝 Contributions

PRs are welcome! Feel free to improve detection, add dashboards, optimize models, or extend database features.

---

## 📄 License

MIT License.



Just let me know!
