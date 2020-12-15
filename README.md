# ITU-ML5G-PS-031_TeamKCGI
Theme2 of ITU AI/ML in 5G Challenge Global Round in Japan: Network State Estimation by Analyz-ing Raw Video Data (NEC)
# Problem statement
Due to the COVID-19 pandemic in 2020, telework using web camera has become a new working style for most people. In this situation, current networks are subjected to a higher traffic load due to increased bandwidth-consuming video applications. As a result, heavy network congestion may occurs and affect video streaming services negatively. In this study, we focus on estimating the network state by analyzing video data.
# DateSet
[Downlad dataset](https://www.ieice.org/~rising/AI-5G/dataset/theme2-NEC/dataset_and_issue.tar.gz)  
Original videos are transmitted to an imaginary video viewer via a network emulator. Dataset for training is generated based on network conditions as follows:  
Throughput range: from 1100 kbps to 2000 kbps at 100 kbps intervals.  
Packet loss ratios: 0.001%, 0.01%, 0.025%, 0.05%, 0.1%, and 0.25%.
# Experiment environment
- Local machine with a AMD Ryzen7 1700 CPU @ 3GHz, Nvidia 1050 GPU 
- Google colab with a Intel Xeon CPU @ 2.20GHz, Nvidia T4 GPU
- Python 3.7.2
- Keras 2.4.3
- OpenCV 3.4.2
# Proposed Method
- Gathering file size and video bit rate from both original video and received video.
- Learning throughput using gathered file size and video bit rate though a neural network.
- Extract every frame from both original video and received video and calculate PSNR for each frame.
- Learning Packet loss ratio using calculated PSNR though a neural network.
- prediction
# Result
The performance of the proposed models are evaluated based on mean absolute error (MAE).
- MAE of Throughput: 4.44 
- MAE of Packet loss ratio: 0.04
