# AR Ruler 📏

A precise Augmented Reality (AR) measurement tool built with **Swift** and **ARKit**. This application allows users to measure real-world distances by placing 3D anchors in physical space through their iPhone or iPad camera.



## 🌟 Features

* **Point-to-Point Measurement:** Calculate the distance between any two points in the physical world.
* **3D Scene Integration:** Utilizes **SceneKit** to render 3D markers and measurement lines.
* **Real-time Calculations:** Distance is calculated and updated instantly upon placing anchors.
* **Automatic Plane Detection:** Detects horizontal and vertical surfaces to ensure accurate anchor placement.
* **Unit Conversion:** Clear, legible measurement readouts in metric units.

## 🛠️ Technology Stack

* **Language:** Swift
* **Frameworks:**
    * **ARKit:** Handles world tracking, camera scene capture, and spatial understanding.
    * **SceneKit:** Manages the 3D nodes, geometry, and rendering of the measurement UI.
* **Tools:** Xcode, Apple Vision (for feature point detection).

## 📐 How It Works

The app utilizes the **Euclidean distance** formula to calculate the space between two 3D vectors ($P_1$ and $P_2$) provided by ARKit's coordinate system:

$$d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}$$

By transforming a 2D screen tap into a 3D "Raycast," the app identifies the exact coordinates in the real world to place a `SCNNode`.



---

## 🚀 Getting Started

### Prerequisites
* A Mac with **Xcode 14+**.
* An iOS device with an **A9 chip or later** (iPhone 6s or newer, iPad Pro).
* *Note: ARKit cannot be tested on the iOS Simulator.*

### Installation
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/raymondoyondi/Augumented-Reality-Ruler-App.git](https://github.com/raymondoyondi/Augumented-Reality-Ruler-App.git)
    ```
2.  **Open the project:**
    Open `ARRuler.xcodeproj` in Xcode.
3.  **Configure Signing:**
    In the "Signing & Capabilities" tab, select your development team.
4.  **Run:**
    Connect your iPhone/iPad and hit **Cmd + R**.

---

## 🤝 Contributing

Contributions make the open-source community an amazing place to learn and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.
