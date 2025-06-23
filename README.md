


## 📄 `README.md` for: **Custom Object Detection Android App**


# 📱 Custom Object Detection Android App

This is a custom object detection Android application built using **TensorFlow Lite**. It performs real-time object detection on live camera input using a custom-trained `.tflite` model.

---

## 🚀 Features

- ✅ Real-time object detection
- ✅ Custom-trained TFLite model
- ✅ Works on Android phones
- ✅ Lightweight and fast
- ✅ Clean UI with bounding boxes drawn over detected objects

---

## 🧠 Model Details

- **Format**: TensorFlow Lite (`.tflite`)
- **Input size**: *e.g.* 300x300 
- **Labels**: Custom objects (e.g., helmet, phone, mask – based on training data)
- **Framework used for training**: TensorFlow / TFLite Model Maker 
---

## 📂 Project Structure

```

starter/
├── app/
├── .gitignore
├── build.gradle
├── local.properties
├── model.tflite  ← Your model file (in assets)
├── labelmap.txt  ← Optional labels file
└── README.md

````

---

## ⚙️ How to Run the App

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/oxyoctavious/Custom_Object_detedtion-model.git
   cd Custom_Object_detedtion-model
````

2. **Open in Android Studio:**

    * Open `starter/` as a project.

3. **Build & Run:**

    * Connect your Android device.
    * Click ▶️ Run from Android Studio.

4. **Ensure model and labels are in:**

   ```
   app/src/main/assets/
   ```

---

## 🧪 Sample Output

> *You can add screenshots or GIFs here later*

---

## 📄 License

This project is licensed under the **MIT License** – feel free to use, modify, and distribute it.

---

## 🙌 Credits

Built by: Vedant Balasaheb Vidhate
Internship/Project: Google AI/ML Virtual Internship via Eduskill
Using TensorFlow Lite and Android Studio



