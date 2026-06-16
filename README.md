# FRC Team #11371 Odyssey - Robot Software

Welcome to the official robot code repository for **FRC Team #11371 Odyssey**. This repository contains the Java-based software utilized to control our competition robot, built atop the modern WPILib ecosystem.

## 🛠️ Tech Stack & Frameworks
* **Language:** Java (100%)
* **Framework:** WPILib (FIRST Robotics Library)
* **Architecture:** Command-Based Programming
* **Tools:** SysId (System Identification), DataLogTool, GradleRIO

## ⚙️ Software Architecture
The codebase strictly follows the **Command-Based paradigm** enforced by WPILib, decoupling the physical hardware components from the operational robot logic:

* **Subsystems:** Encapsulates hardware components (motors, sensors, encoders) and defines basic low-level behaviors.
* **Commands:** Represents high-level, state-driven robot actions (e.g., autonomous routines, teleoperated scoring mechanisms) that require specific subsystems.
* **Operator Interface (OI):** Maps controller inputs (joysticks, gamepads) to specific commands dynamically.

## 📈 System Identification & Tuning
This repository includes integration with **WPILib SysId** for empirical system identification. This allows us to gather data from our drive and mechanism motors to calculate precise feedforward ($kS$, $kV$, $kA$) and feedback ($kP$, $kD$) constants, ensuring optimal PID control loops during competition.

## 🚀 Getting Started
To open and deploy this project, you need:
1. **WPILib VS Code** (matching the competition season version)
2. **JDK 17 / 21** (bundled with WPILib)

### Building the Project
Open the repository in WPILib VS Code and use the WPILib command palette or run:
```bash
./gradlew build
