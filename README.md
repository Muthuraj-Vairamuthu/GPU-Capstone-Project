# GPU-Accelerated RGB Channel Enhancement on SIPI Images

This project demonstrates GPU-powered batch processing of color images using the **USC-SIPI Miscellaneous Image Database**. We enhance color channels using **CuPy** (NumPy on GPU) to simulate a real-time image enhancement pipeline.

## 📁 Dataset
- Source: [USC-SIPI Image Database (Miscellaneous Volume)](https://sipi.usc.edu/database/database.php?volume=misc)
- Format: TIFF
- Sample images: Lena, Peppers, etc.

## 🚀 GPU Framework
- [CuPy](https://cupy.dev) — for GPU array manipulation
- Run on NVIDIA Tesla T4 (Kaggle GPU environment)

## 🧪 Method
For each image:
- **Red Channel**: Brightened by 20%
- **Green Channel**: Contrast-enhanced via centered scaling
- **Blue Channel**: Smoothed with a 3x3 convolutional blur
- Channels are then **merged back** into a single color image

## 📂 Output Files
Located in `/outputs`:
- `*_enhanced.png`: Final reconstructed image
- `*_red_brightened.png`, `*_green_contrast.png`, `*_blue_blurred.png`: Sample channel outputs
- `log.txt`: Processing log
- `timing.csv`: GPU processing time for each image

## 📝 How to Run
Use the Jupyter Notebook:
```bash
sipi_gpu_batch_transform.ipynb
