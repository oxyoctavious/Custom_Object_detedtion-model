




### 📘 **How I Built This Project – Custom Object Detection Android App**

#### 📁 1. Project Setup

* **IDE**: Android Studio Hedgehog
* **Language**: Kotlin / python
* 

    * `TensorFlow Lite`
    * `TensorFlow Lite Task Vision`
* **Gradle Version**: 8.12 # it was 6.5 eariler whit diddnt supported the java 21
* **Kotlin Version**: 1.9.23 #was 1.3.72 but now changed to this for berrter performance
* **JDK**: Java 21

#### 🧠 2. Model Preparation

* **Model Source**: Trained a custom model using \[TensorFlow Lite Model Maker / Teachable Machine / etc.]
* **Model Type**: `.tflite`
* **Input Size**: 224x224 or 300x300 
* **Placed in**: `app/src/main/assets/`

#### 📲 3. Android Integration Steps

1. Created a new Android Studio project with **Empty Activity**
2. Added required dependencies in `build.gradle`:

   ```gradle
   implementation 'org.tensorflow:tensorflow-lite-task-vision:0.4.3'
   ```
3. Loaded the `.tflite` model from the `assets/` folder
4. Used `ObjectDetector` API from TFLite to run detection
5. Parsed and drew bounding boxes using `Canvas` on `ImageView` or camera preview

#### 🔧 4. Fixes and Configuration

*  6-12-2025 
* Fixed **Gradle compatibility error** (Java 21 + Gradle 6.5) by:

    * Upgrading to **Gradle 8.12**
    * Upgrading to **Kotlin 1.9.23**
* Used `.gitignore` to keep the repo clean
* Added `README.md` and committed project to GitHub



* fixed **org.gradle.api.internal.plugins.PluginApplicationException: Failed to apply plugin 'kotlin-android'.**:by
   
    * Upgrading to **Gradle plugin 8.2.2**
      older version was not supported Kotlin 1.9.23 and incompatible with Gradle 8.x
      older version was 4.1.2
    * Upgraded **jcenter() with mavenCentral()**
      jcenter() is deprecated and no longer reliable.
  
* Fixed **Namespace not specified**: by

* AGP 8+ requires a namespace to be explicitly defined in your module-level (app) build.gradle.

You’ll see this error if your build.gradle still uses the old package only in the AndroidManifest.xml.   

    * Fixed this by adding some new line of code 
* **android {
    namespace 'com.yourcompany.yourappname'  // ← change this to your actual app's package name
compileSdk 34**

**defaultConfig {
    applicationId "com.yourcompany.yourappname"  // ← should match namespace
        ...
    }
}**

### Pending Issues
* **app:processDebugResource**
  ![Resource downloading](starter/screenshots/Error.png)
* **packege error in XMlfile**


### PROGRESS 
* After fixing the error the error the project is being downloading the resources
  ![Resource downloading](starter/screenshots/Resource.png)

#### 🧪 5. Testing

* Tested on a real Android device
* Verified model loads, camera works, and objects are detected
* Adjusted score threshold and max results

#### 📸 6. Screenshots (Optional)

*Add if available*:

```markdown
![Detection Demo](screenshots/demo.png)
```

---

### ✅ Where to Put This?

You can now do **either**:

1. **Add this to the bottom of your current `README.md`**
   Just paste under `## 🙌 Credits` or create a new section `## 🛠 Development Guide`

**OR**

2. Create a new file:

    * In Android Studio, right-click root > New > File > `DEVELOPMENT.md`
    * Paste the content
    * Push with:

      ```bash
      git add DEVELOPMENT.md
      git commit -m "Add detailed development guide"
      git push
      ```

---

Would you like me to format this for direct copy-paste or commit it into a file for you?
