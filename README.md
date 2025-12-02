RoadSense: 3D Hazard Intelligence

A depth-aware road safety system that detects obstacles, potholes, lane paths, and drivable road regions when visibility goes full villain mode (fog, rain, night, glare, you name it).

Three big ideas
	1.	Fuses LiDAR, Ultrasonic, IR sensors, an Accelerometer, and a camera into a single real-time pipeline to build 3D scene awareness of the road ahead.
	2.	Uses tuned neural perception models for classification and segmentation to ensure hazards don’t get ignored just because the weather wants attention.
	3.	Generates GPS-tagged hazard intel via REST endpoints to help communities know what’s broken, where it’s broken, and ideally fix it before someone’s suspension rage-quits.

Accuracy that actually matters

Obstacle classification accuracy: 84% (adverse visibility)
Drivable road segmentation accuracy: 94%
Lane detection accuracy: 92%
Pothole detection precision: 89%

What RoadSense does

Provides reliable awareness of road hazards. Builds 3D surface understanding using sensor fusion. Runs YOLOv11 detection variants for obstacles and lanes. Uses EfficientNet-U-Net backbone for drivable region segmentation. Sends structured hazard reports via REST endpoints. Tags hazards using GPS. Supports proactive road safety awareness for drivers and maintenance teams. Works in fog, rain, low light, glare, and night conditions.

Tech Stack

Python + IoT + ML + MySQL + OpenCV + PyTorch + Ultralytics YOLO + REST APIs + ONNX runtime + mixed-precision acceleration.

Why this exists (besides over-engineering therapy)

Most camera-based systems fail in adverse visibility. Single-sensor systems lack depth or classification reliability. Manual inspections are slow and error-prone. RoadSense fixes the “I can’t see it, so it’s not my problem” flaw with multi-sensor fusion and AI perception.

Societal Impact

Improves road hazard awareness. Helps prevent vehicle damage. Enables safer low-visibility driving. Supports infrastructure teams with precise hazard mapping. Encourages proactive road maintenance decisions. Keeps communities safer, smarter, and hopefully less full of potholes shaped like emotional regret.

Repository Structure

/models – Trained model weights and configs
/src – Sensor fusion pipeline, inference scripts, API server
/results – Model accuracy reports and curves (PDFs)
README.md – You’re here. Congrats on making it this far
.gitignore – Because your training checkpoints don’t need public grading too

How to Run

Clone the repo. Set up dependencies using requirements.txt. Start the API server using Node/Express backend wrapper. Run inference using yolo predict scripts or segmentation pipeline. Feed sensor test data through RoadSense fusion engine. Generate hazard report endpoints.

Privacy Note on PDFs

Rendered result PDFs are safe and uploaded because they only display model performance metrics and inference samples. They contain no personal user data or individual-identifying GPS coordinates.

License

This is a team-built research prototype for road safety awareness. Models used from Ultralytics follow their licensing. Repository code is open for learning and extension. Do the right thing with it. The road will thank you.
