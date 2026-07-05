🌿 Podcrush: Automatic Edamame Bean Pod Extracting Machine
International Islamic University Malaysia (IIUM)

Department of Mechatronics Engineering (Group 10 - Semester 2, 2025/2026)

📖 Overview
Podcrush is a compact, automated mechatronic appliance engineered to process fresh edamame pods for small-scale agricultural operations and home-based businesses. Traditional edamame shelling is highly labor-intensive, and large industrial machines are too expensive and bulky for small operations. This proof-of-concept prototype replaces manual labor with an affordable, space-saving, and data-driven solution. The system operates on an ESP32 microcontroller to manage physical extraction, active electrical safety monitoring, and IoT cloud alerts.  

✨ Key Features
Automated Extraction Mechanism: Utilizes two counter-rotating rollers covered in abrasive sandpaper to grip and pull the pods through a fixed 7.5 mm gap, effectively cracking the hulls.  

Smart Feeding & Separation: Integrates a high-torque digital servo motor (MG996R) to regulate the hopper gate, alongside a vibrating DC motor to agitate a slanted 3D-printed tray for bean-hull separation.  

Active Safety & Anti-Jam Logic: Features an ACS712 current sensor that continuously tracks the motor load. If a tough pod causes the load to spike above 2.9 A, the system triggers an emergency shutdown to prevent motor burnout.  

Dual-Layer IoT Interface: Hosts a local web dashboard ([http://extractionhub.local](http://extractionhub.local)) for on-site control, and utilizes a Telegram Bot API to send real-time emergency push notifications to mobile devices.  

🛠️ Hardware & Materials
Processing Core: ESP32 DevKitC (Dual-Core 32-bit architecture).  

Actuation: 12V DC geared motors (for extraction rollers and conveyor belt), 12V DC ERM vibrating motor, and an MG996R servo motor.  

Motor Drivers: Heavy-duty motor shields (L298N / TB6600).  

Structural Frame: Constructed from lightweight Aluminum 2020 T-Slot extrusions.  

Safety Shielding: Transparent acrylic polycarbonate panels to protect the operator while allowing visual inspection.  

Custom Parts: Fused Deposition Modeling (FDM) 3D-printed PLA for transmission gears and the feeding mechanism.  

⚙️ System Architecture
The machine relies on a hybrid time-slicing software architecture to manage physical hardware and dual communication layers without system stalls.  

Core 0: Dedicated to high-latency network overhead, including secure TLS/SSL cloud handshakes for the Telegram Bot API.  

Core 1: Handles real-time deterministic tasks, such as high-frequency PWM generation, analog sensor sampling, and hardware interrupts.  

👥 Project Team
Adam Nabil Haniff Bin Ruzaimi  

Ainin Sofiya Binti Kamaruzaman  

Qashrina Aisya Binti Mohd Nazarudin  

Muhammad Haziq Ajmal Bin Md Kamal  

Supervised by: Dr. Hasmawati Bt. Antong & Prof. Dr. Tanveer Saleh
