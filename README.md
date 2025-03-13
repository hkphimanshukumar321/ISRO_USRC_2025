# ISRO_USRC_2025
DEVELOPING ANAV  AND REINFORCEMNT LEARNING BASED  PATH PLANNING  


Repository Structure Overview
css
Copy
/ (root)
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── .gitignore
├── docs/
│   ├── project-overview.md
│   ├── requirements.md
│   ├── api-documentation.md
│   ├── design/
│   │   ├── system-architecture.pdf
│   │   └── subsystem-diagrams.pdf
│   ├── test-plan.md
│   └── changelog.md
├── src/
│   ├── hardware/
│   │   ├── schematics/
│   │   │   └── drone-frame-design.pdf
│   │   ├── firmware/
│   │   │   ├── flight-controller/
│   │   │   │   └── main.c
│   │   │   └── sensor-interfaces/
│   │   │       ├── lidar_driver.c
│   │   │       └── imu_driver.c
│   │   └── build-instructions.md
│   ├── software/
│   │   ├── navigation/
│   │   │   ├── slam_module.py
│   │   │   ├── path_planning.py
│   │   │   └── reinforcement_learning.py
│   │   ├── control/
│   │   │   ├── pid_controller.cpp
│   │   │   └── sliding_mode.cpp
│   │   ├── emergency/
│   │   │   ├── battery_monitor.py
│   │   │   └── collision_avoidance.py
│   │   └── utils/
│   │       ├── logger.py
│   │       └── data_processing.py
├── tests/
│   ├── unit/
│   │   ├── test_navigation.py
│   │   ├── test_control.cpp
│   │   └── test_emergency.py
│   ├── integration/
│   │   └── test_system_integration.py
│   └── simulation/
│       ├── gazebo/
│       │   └── simulation_world.world
│       └── run_simulation.sh
├── assets/
│   ├── images/
│   │   ├── system_diagram.png
│   │   └── component_layout.jpg
│   ├── models/
│   │   ├── drone_model.stl
│   │   └── sensor_mounts.stl
│   └── videos/
│       └── simulation_demo.mp4
├── config/
│   ├── simulation_config.yaml
│   └── system_config.yaml
└── scripts/
    ├── build.sh
    ├── deploy.sh
    └── setup_environment.sh
Detailed Explanation of Components
Root-Level Files
README.md:
Provides an overview of the project, setup instructions, usage guidelines, and a summary of the repository structure.
CONTRIBUTING.md:
Contains guidelines for contributing (coding standards, branch naming conventions, and commit message formats) to foster collaboration and maintain code quality.
LICENSE:
States the legal usage terms for the project.
.gitignore:
Specifies files and directories to be ignored by Git (e.g., build artifacts, temporary files, local configurations), ensuring a clean repository history.
Documentation (docs/)
Project Documentation:
Contains all project-related documentation including:
project-overview.md: A high-level description of the ANAV project.
requirements.md: Detailed project requirements and specifications.
api-documentation.md: Describes the API endpoints (if applicable) and data flow between modules.
design: Folder for architecture diagrams and subsystem designs.
test-plan.md: Detailed test cases and simulation plans.
changelog.md: Records changes and version updates.
Source Code (src/)
hardware/:
Contains hardware-related resources:
schematics/ and firmware/ folders hold design files (e.g., drone frame, sensor mounting details) and source code for microcontrollers (e.g., flight-controller firmware, sensor drivers).
build-instructions.md: Guides for assembling hardware components.
software/:
Organized into functional modules:
navigation/: Houses code for SLAM, path planning, and reinforcement learning for adaptive navigation.
control/: Contains implementations of control algorithms like PID and sliding mode control.
emergency/: Scripts for monitoring battery levels, collision avoidance, and other emergency protocols.
utils/: Common utilities (logging, data processing) that support multiple modules.
Testing (tests/)
unit/:
Unit tests for individual software modules ensuring each function behaves as expected.
integration/:
Tests that verify interactions between different modules, ensuring overall system cohesion.
simulation/:
Contains scripts and configurations for running simulations (e.g., Gazebo simulation files) to validate system behavior in a virtual Martian-like environment.
Assets (assets/)
images/ & models/:
Provide visual aids (diagrams, CAD models) for system design and component layout.
videos/:
Demonstrations or simulation recordings that showcase the project in action.
Configuration (config/)
Config files:
YAML or JSON files to set parameters for simulations, system configuration, and deployment. This ensures that changes in the environment or system setup can be managed centrally.
Scripts (scripts/)
Automation Scripts:
Includes shell scripts for building the project, deploying updates, and setting up the development environment.
Git Architecture and Best Practices
Branching Strategy:
A common strategy (like GitFlow or feature-branch workflow) should be adopted:
main/master: Contains the stable release.
develop: Used for integration of new features.
feature/bugfix branches: For individual development tasks.
Commit Messages:
Follow clear, descriptive commit messages that indicate what has changed and why. For example:
csharp
Copy
feat(navigation): add dynamic path planning with A* algorithm
fix(control): adjust PID controller parameters for improved stability
.gitignore:
Maintain a robust .gitignore file to avoid checking in local configuration files, compiled binaries, and other non-source code files.
Scalability and Maintainability
Modularity:
Separating hardware and software modules makes it easier to update components without affecting other parts of the project.
Documentation:
Centralized documentation in the docs/ folder ensures every team member understands the project requirements, design, and testing protocols.
Testing Framework:
A dedicated tests/ folder ensures that new code changes do not break existing functionality, promoting continuous integration and delivery.
Automation:
Scripts for building, deployment, and simulation help streamline the development process, reducing manual overhead and ensuring reproducibility.
File Relationships and Interconnections
README.md & CONTRIBUTING.md:
Serve as entry points, guiding new developers through repository structure and contribution guidelines.
Docs & Config Files:
The docs/ folder explains the overall architecture, while config/ holds environment-specific settings—together they keep the project well-documented and configurable.
Src and Tests:
The code in src/ is closely mirrored by corresponding tests in tests/ to ensure every module can be validated independently and in integration.
Assets and Scripts:
Visual aids in assets/ support design decisions referenced in documentation, and automation scripts in scripts/ ensure the project can be built and deployed consistently.






 ANAV – Autonomous Navigation Aerial Vehicle

![ANAV Logo](assets/images/anav_logo.png) <!-- Optional: Replace with your logo -->

**ANAV** is an innovative project aimed at developing an autonomous aerial vehicle capable of advanced navigation, mapping, and emergency response in challenging environments. Designed with both scalability and reliability in mind, ANAV leverages cutting-edge sensor fusion, SLAM, and AI-driven control algorithms to enable safe and efficient autonomous flight—ideal for exploration missions in environments where conventional navigation aids are unavailable.

> *"Empowering autonomous exploration through intelligent aerial navigation."*

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Repository Structure](#repository-structure)
4. [Setup Instructions](#setup-instructions)
5. [Usage](#usage)
6. [Contributing Guidelines](#contributing-guidelines)
7. [License](#license)
8. [Acknowledgments](#acknowledgments)
9. [Roadmap](#roadmap)
10. [FAQs](#faqs)
11. [Contact Information](#contact-information)

---

## Project Overview

**ANAV** (Autonomous Navigation Aerial Vehicle) is developed to address the challenges of navigating unstructured and dynamic environments, such as those encountered in planetary exploration. The project aims to:
- Enable real-time mapping and localization using advanced SLAM techniques.
- Implement dynamic path planning and obstacle avoidance.
- Integrate a robust emergency response system for safe failover.
- Provide a modular platform that supports both hardware and software innovations.

The project is designed for researchers, engineers, and enthusiasts interested in autonomous systems, robotics, and aerospace technologies.

---

## Features

- **Autonomous Navigation:** Utilizes SLAM and AI-based path planning for real-time decision making.
- **Robust Sensor Fusion:** Integrates data from LiDAR, IMU, radar, and cameras to ensure high precision.
- **Emergency Response:** Implements fail-safe mechanisms such as battery monitoring and collision avoidance.
- **Modular Design:** Separates hardware and software components for ease of maintenance and scalability.
- **Simulation & Testing:** Provides a Gazebo-based simulation environment for pre-deployment testing.
- **Extensible Architecture:** Designed to support future enhancements, including additional sensors and control algorithms.

---

## Repository Structure

Below is an overview of the repository layout and the purpose of each major folder/file:

ANAV/ ├── README.md # Project overview and documentation ├── LICENSE # License information ├── .gitignore # Specifies files/folders to ignore in Git ├── docs/ # Project documentation and design files │ ├── project-overview.md # Detailed project description │ ├── requirements.md # System requirements and specifications │ ├── design/ # Architecture diagrams and design documents │ │ ├── system-architecture.pdf │ │ └── subsystem-diagrams.pdf │ └── test-plan.md # Testing strategies and plans ├── src/ # Source code of the project │ ├── hardware/ # Hardware schematics, firmware, and build guides │ │ ├── schematics/
│ │ │ └── drone-frame-design.pdf │ │ ├── firmware/
│ │ │ ├── flight-controller/ │ │ │ │ └── main.c │ │ │ └── sensor-drivers/ │ │ │ ├── lidar_driver.c │ │ │ └── imu_driver.c │ │ └── build-instructions.md │ ├── software/ # Software modules for navigation, control, etc. │ │ ├── navigation/ │ │ │ ├── slam_module.py │ │ │ ├── path_planning.py │ │ │ └── reinforcement_learning.py │ │ ├── control/ │ │ │ ├── pid_controller.cpp │ │ │ └── sliding_mode.cpp │ │ ├── emergency/ │ │ │ ├── battery_monitor.py │ │ │ └── collision_avoidance.py │ │ └── utils/ │ │ ├── logger.py │ │ └── data_processing.py │ └── config/ # Configuration files for simulations and deployments │ ├── simulation_config.yaml │ └── system_config.yaml ├── tests/ # Test suites and simulation scripts │ ├── unit/ # Unit tests for individual modules │ ├── integration/ # Integration tests across components │ └── simulation/ # Simulation environment scripts (e.g., Gazebo) ├── assets/ # Static assets (images, models, videos) │ ├── images/ │ ├── models/ │ └── videos/ └── scripts/ # Automation scripts for building and deployment ├── build.sh ├── deploy.sh └── setup_environment.sh

markdown
Copy

---

## Setup Instructions

### Prerequisites

- **Git:** Version control system for cloning the repository.
- **Python 3.8+ / C++ Compiler:** Depending on the module (ensure necessary build tools are installed).
- **CMake:** For building firmware components.
- **ROS (Robot Operating System):** For simulation and robotics integration (if applicable).
- **Gazebo:** Simulation environment for testing the aerial vehicle.
- **Additional Dependencies:** Refer to `requirements.txt` or install scripts in the `scripts/` directory.

### Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/ANAV.git
Navigate to the Project Directory:

bash
Copy
cd ANAV
Install Software Dependencies:

For Python modules, run:
bash
Copy
pip install -r requirements.txt
For ROS-based modules, follow the ROS installation guidelines provided in the ROS Wiki.
Configure Environment Variables:

bash
Copy
cp .env.example .env
Edit the .env file as needed for your local setup.

Build Firmware (if applicable):

bash
Copy
cd src/hardware/firmware/flight-controller
mkdir build && cd build
cmake ..
make
Run Setup Script:

bash
Copy
./scripts/setup_environment.sh
Usage
Once the project is set up, you can run the simulation and test individual modules.

Running the Simulation
Launch the Gazebo simulation environment:
bash
Copy
./tests/simulation/run_simulation.sh
Monitor the system outputs via the provided ROS topics or log files.
Example: Running the SLAM Module
Execute the SLAM module with:
bash
Copy
python src/software/navigation/slam_module.py --config config/simulation_config.yaml
View the generated map and localization data in the console or through visualization tools such as RViz.
Common Tasks
Testing Modules: Run unit tests with:
bash
Copy
pytest tests/unit/
Deploying Firmware: Follow the instructions in src/hardware/build-instructions.md for uploading the firmware to the flight controller.
Contributing Guidelines
We welcome contributions from the community! To ensure a smooth development process, please follow these guidelines:

Fork the Repository: Create your own fork and clone it locally.
Create a Feature Branch:
bash
Copy
git checkout -b feature/your-feature-name
Commit Your Changes: Use clear and descriptive commit messages.
bash
Copy
git commit -m "feat: add new SLAM optimization algorithm"
Push to Your Branch:
bash
Copy
git push origin feature/your-feature-name
Open a Pull Request: Submit your changes for review. Please ensure your code adheres to our coding standards and includes appropriate tests.
Issue Reporting: If you encounter bugs or have feature requests, please open an issue on GitHub.
For more detailed information, please review our CONTRIBUTING.md.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgments
Third-Party Libraries: Thanks to the contributors of ROS, Gazebo, and other open-source tools that made this project possible.
Inspiration: The innovative work in autonomous navigation and aerial robotics has inspired the development of ANAV.
Contributors: We appreciate the hard work of all team members and external contributors who have provided valuable feedback and code improvements.
Roadmap
Short Term:
Refine SLAM algorithms for higher accuracy.
Improve integration tests for system-wide validation.
Medium Term:
Incorporate additional sensor modules.
Expand simulation scenarios to cover diverse environments.
Long Term:
Develop a comprehensive mobile app for real-time monitoring and control.
Explore hardware-in-the-loop (HIL) testing for improved deployment readiness.
FAQs
Q: What environments is ANAV designed for?
A: ANAV is primarily designed for autonomous aerial navigation in challenging and dynamic environments such as planetary exploration or indoor mapping scenarios.

Q: How can I contribute to improving the simulation environment?
A: Contributions are welcome! Please refer to our contributing guidelines and open a pull request with your proposed changes.

Contact Information
For support or collaboration inquiries, please reach out via:

Email: contact@anavproject.org
GitHub Issues: Open a new issue in the repository for any bugs or feature requests.
Happy Coding and Exploring!
