# Human Activity Recognition Using Video and Wearable Sensor Data

This project explores a **multimodal deep learning framework** for fall detection and activity recognition, combining **video (SD images)** and **sensor data (GAF & RP images)**. Developed using the [UP-FALL dataset](https://www.mdpi.com/1424-8220/19/9/1988), our system uses CNN-based models to classify 11 human activities with up to **91% test accuracy**.

---

## Dataset
We used the [UP-FALL Detection Dataset](https://www.mdpi.com/1424-8220/19/9/1988) containing:
- Video recordings from static cameras
- Sensor data from accelerometers and gyroscopes (wrist & ankle)
- 11 activities: 5 types of falls, 6 normal movements

Due to size constraints, data is not included here. Please download it from the [official source](https://www.mdpi.com/1424-8220/19/9/1988).

---

## Methodology

### Video Preprocessing:
- Extracted grayscale frames
- Computed Summed-Difference (SD) images with 50% overlap
- Resized to 32x32 and normalized

### Sensor Data Preprocessing:
- Calculated **Gramian Angular Fields (GAF)** and **Recurrence Plots (RP)** for ankle and wrist sensors
- Stacked sensor features with SD images to form a multi-channel input

---

## Experiments

| Input Type                            | Accuracy | Precision | Recall |
|--------------------------------------|----------|-----------|--------|
| SD Images (Video only)               | 84.0%    | 74%       | 70%    |
| Video + GAF (2-channel)              | 86.0%    | 74%       | 72%    |
| Video + RP (Ankle only)              | 87.1%    | 74%       | 74%    |
| Video + RP (Ankle + Wrist)           | **91.0%**| 83%       | 82%    |
| Weighted stacking (5-channel)        | 87.15%   | -         | -      |

---

## Technologies Used

- Python (NumPy, Pandas, TensorFlow/Keras)
- UP-FALL dataset
- Matplotlib, Seaborn for visualization

---

## Contributors

This project was developed by a student team at Nazarbayev University as part of a group research initiative.

- Aruay Amangeldi
- Alisher Nurmukhanov
- Raiymbek Yeslyam
- Zhaksylyk Chalgimbayev
- Akhmetzhan Kussainov
- Ayan Zholdybayev
- Azat Serikbayev

---

## Report

Full project report is available at Report.pdf

See the full project report in [`report/HAR_Final_Report.pdf`](report/HAR_Final_Report.pdf)

