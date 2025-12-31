# WelVision - Automated Roller Defect Inspection System

## Project Description
WelVision is an advanced industrial defect inspection system designed to automate the quality control process for roller manufacturing. By leveraging the power of Computer Vision and Artificial Intelligence (specifically Yolo and PyTorch), the application detects surface defects in real-time, ensuring high production standards. The system integrates seamlessly with industrial hardware (PLCs and Cameras) to provide a complete automation solution.

---

## Project Details

### Problem Statement
Manual inspection of industrial rollers is labor-intensive, time-consuming, and prone to human error. Consistent quality assurance is difficult to maintain with the naked eye, leading to potential defects slipping through the production line. WelVision solves this by providing precise, automated, and continuous monitoring.

### Key Features
- **AI-Powered Detection:** Utilizes state-of-the-art Deep Learning models (YOLO via Ultralytics) to identify defects with high accuracy.
- **Real-Time Imaging:** Captures and processes live video feeds from industrial cameras.
- **PLC Integration:** Communicates directly with Siemens PLCs (via Snap7) to triger actions (e.g., stopping the line, rejecting parts).
- **User Management:** secure login and role-based access control for operators and administrators.
- **Comprehensive Reporting:** Database storage (MySQL) for historical defect tracking and diagnosis.
- **Configurable Settings:** Adjustable parameters for camera exposure, model selection, and inspection thresholds.

### Technical Architecture
- **Inference Engine:** PyTorch & Ultralytics (YOLO)
- **Image Processing:** OpenCV & Pillow
- **GUI:** Custom Tkinter-based interface for ease of use on shop floors.
- **Database:** MySQL for robust data management.
- **Hardware Interface:** Snap7 for PLC communication; `pygrabber` for camera interfacing.

---

## Tech Stack
- **Language:** Python 3.x
- **Deep Learning:** PyTorch, Torchvision, Ultralytics
- **Computer Vision:** OpenCV-Python, Pillow
- **GUI:** Tkinter (Standard Lib), tkcalendar
- **Database:** MySQL Connector
- **Automation:** Python-Snap7 (Siemens S7 PLC communication)
- **Utilities:** Numpy, Pandas, PyWin32

---

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/DCode-v05/Welvision-App.git
cd Welvision-App
```

### 2. Install dependencies
The project uses `pip` for dependency management. Note that PyTorch installation may require the extra index URL for CUDA support as specified in the requirements file.

```bash
pip install -r requirements.txt
```

### 3. Database Setup
Ensure you have a MySQL server running. Configure the database connection settings in `database.py` or the application settings menu to point to your instance.

### 4. Run the Application
Start the main application using the entry point script:

```bash
python main.py
```

---

## Usage
- **Login:** Launch the app and log in with valid credentials.
- **System Check:** Use the System Check module to verify camera and PLC connectivity.
- **Inspection:** Navigate to the main inspection screen to start the automated process.
- **Analysis:** View historical data and defect logs in the Diagnosis section.
- **Settings:** Administrators can adjust model confidence thresholds and camera parameters.

---

## Project Structure
```
Welvision-App/
│
├── main.py              # Application entry point
├── backend.py           # Core logic and background processing
├── database.py          # Database connection and query handlers
├── requirements.txt     # Python dependencies
├── IC Capture Settings/ # Camera configuration profiles
├── frontend/            # GUI Source Code
│   ├── app.py           # Main Application Window
│   ├── backup/          # Backup relate modules
│   ├── data/            # Data handling modules
│   ├── diagnosis/       # Defect analysis and reporting screens
│   ├── inference/       # AI Inference display logic
│   ├── info/            # Information and help screens
│   ├── login/           # Authentication modules
│   ├── model_management/# AI Model management interface
│   ├── navbar/          # Navigation bar components
│   ├── settings/        # System configuration panels
│   ├── system_check/    # Hardware status checks (PLC/Camera)
│   ├── user_management/ # User administration
│   └── utils/           # Frontend utility functions
├── models/              # Trained AI models (.pt files)
├── utils/               # Helper scripts and shared utilities
└── README.md            # Project documentation
```

---

## Contributing

Contributions are welcome! To contribute:
1. Fork the repository
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature
   ```
5. Open a pull request describing your changes.

---

## 📬 Contact
For any queries or suggestions, feel free to reach out:

- 📧 **Email:** abineshbalasubramaniyam@example.com
- 💼 **LinkedIn:** [linkedin.com/in/abinesh-b-1b14a1290/](https://linkedin.com/in/abinesh-b-1b14a1290/)
- 🐙 **GitHub:** [github.com/Abinesh2418](https://github.com/Abinesh2418)
