# Yavar_Hackathon
Person Fall Detection Using YoloV7

# Code Structure
1. Fall Detection Functions
fall_detection(poses): Analyzes detected poses to determine if a fall has occurred based on predefined criteria.
falling_alarm(image, bbox): Annotates an image with a bounding box and text label indicating a detected fall.
2. YOLOv7-POSE Model Handling
get_pose_model(): Loads the YOLOv7-POSE model and returns the model instance along with the device (CPU/GPU) on which it is loaded.
get_pose(image, model, device): Processes an image using the YOLOv7-POSE model to detect human poses.
3. Utility Functions
prepare_image(image): Prepares a processed image for visualization.
prepare_vid_out(video_path, vid_cap): Prepares the output video writer object.
4. Video Processing
process_video(video_path): Processes a video file frame by frame, detects falls, annotates frames, and generates an output video.
5. Main Execution
The main block of code iterates over all video files in a specified directory, processes each video using the process_video function, and saves the annotated output videos.

# Dependencies
torch: PyTorch library for deep learning.

cv2: OpenCV library for computer vision tasks.

numpy: NumPy library for numerical computations.

tqdm: tqdm library for displaying progress bars.

Custom utility functions imported from utils.datasets, utils.general, and utils.plots modules.
