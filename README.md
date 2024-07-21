# Video-Steganography
Video steganography, which hides secret information within ordinary video files, is an effective method for covert data transmission. Traditional methods face issues like low data capacity, noticeable visual changes, and susceptibility to detection. This project develops a desktop application for Video in Video Steganography using CAE to hide a secret video inside another video, both containing audio. A dataset of 644 videos for cover and secret categories was collected from personal recordings. Each video was trimmed to 15 seconds, standardized to 30 fps, and 300 frames were extracted. A CNN extracts features from video frames, and an AutoEncoder embeds one video into another. Data augmentation techniques like resizing, normalization, and de-normalization improve accuracy and performance. The system's performance will be evaluated using MSE, SSIM, and PSNR. This system is beneficial for secure information transmission in defense, intelligence, journalism, and government. Advanced embedding techniques and CNN are expected to achieve high accuracy with minimal noticeable changes.

#### Note: Steganography is applied for both the video and the audio part. This is done by seperating the video and the audio component and then individually feeding them to the Convolutional Auto Encoder.

## System Block Diagram
<img src="https://github.com/user-attachments/assets/b5178a90-e7f5-4eef-baff-59d2155a194a" alt="blockdiagram" width="800">


## System Flowchart

<table>
  <tr>
    <td style="text-align: center;">
      <h3>Encoder</h3>
      <img src="https://github.com/user-attachments/assets/dacad918-9891-427c-9e13-8c4049bcda65" alt="Encoder Flowchart" width="400" height="800">
    </td>
    <td style="text-align: center;">
      <h3>Decoder</h3>
      <img src="https://github.com/user-attachments/assets/b57ffb14-1c6b-4053-a338-f5c76b2fa436" alt="Decoder Flowchart" width="400" height="800">
    </td>
  </tr>
</table>


## Implementation Architecture
### Video
<img src="https://github.com/user-attachments/assets/4df3df91-5ae3-407a-b3db-c63ad1c348d4" alt="model_architecture" width="800">

### Audio
Under progress...


## Preprocessing
Preprocessing techniques used for the video part are:
- **Rescaling**: Adjusting the size of video frames to a uniform dimension to ensure consistency across the dataset.
- **Normalization**: Transforming pixel values to a common scale, typically between 0 and 1, to facilitate model training.
- **Denormalization**: Converting normalized pixel values back to their original scale for interpretation or visualization purposes.
