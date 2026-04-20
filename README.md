# 🔩 Fastener Sorting using OpenCV and Raspberry Pi

## 📌 Overview

This project implements an automated **fastener sorting system** using **computer vision**.
A camera connected to a Raspberry Pi detects and classifies fasteners (nuts and bolts) based on their shape, and the system outputs their positions and type.

The detection is performed using **OpenCV**, and object classification is based on **aspect ratio analysis**.

---

## 🎯 Features

* 📷 Real-time object detection using a camera
* 🔍 Contour-based segmentation
* 🧠 Classification of fasteners:

  * Nut (approximately square shape)
  * Bolt (elongated shape)
* 📍 Position detection using object center
* 📊 Normalized coordinate mapping
* 🖥️ Live visualization with bounding boxes and labels

---

## ⚙️ Technologies Used

* Python 3
* OpenCV (`cv2`)
* NumPy

---

## 🧠 Working Principle

1. Capture live video from the camera
2. Convert frame to grayscale
3. Apply thresholding for object segmentation
4. Perform morphological operations to remove noise
5. Detect contours
6. Filter contours based on area
7. Compute bounding box and aspect ratio
8. Classify object:

   * Nut → aspect ratio ≈ 1
   * Bolt → elongated aspect ratio
9. Compute center coordinates
10. Normalize coordinates for further processing


---

## 🧾 Output

* Bounding box drawn around detected fasteners
* Label displayed (Nut / Bolt)
* Center point marked
* Console output:

```
