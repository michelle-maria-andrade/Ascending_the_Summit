# Ascending the Summit

This repository contains the environment assets, configuration files, and mission boundaries for the **Ascending the Summit** drone simulation task.

---

## Important: Git LFS Required
This repository uses **Git Large File Storage (LFS)** to manage the large environment archive (`LandscapeMountains.zip`). 

To clone this repository correctly, you **must** have Git LFS installed on your system.

---

### Installation & Cloning

1.  **Install Git LFS**:
    * **Ubuntu/Debian**: `sudo apt install git-lfs`
    * **Fedora**: `sudo dnf install git-lfs`
    * **Windows**: Download from [git-lfs.github.com](https://git-lfs.github.com/)

2.  **Initialize LFS**:
    ```bash
    git lfs install
    ```

3.  **Clone the Repo**:
    ```bash
    git clone git@github.com:michelle-maria-andrade/Ascending_the_Summit.git
    cd Ascending_the_Summit
    ```

4.  **Pull Large Files** (If they didn't download automatically):
    ```bash
    git lfs pull
    ```

---

### Project Structure
* **LandscapeMountains.zip**: The compressed Unreal Engine environment.
* **boundary_1.txt & boundary_2.txt**: Example coordinate sets for simulation flight boundaries.
* **settings.json**: Configuration file for the simulation environment.

---

### Mission Requirements & Usage

#### 1. Flight Constraints
* **Altitude**: Maintain a constant height of **6m** for the entire coverage area.
* **Obstacle Avoidance**: Ensure the flight path successfully navigates around all natural obstacles within the landscape.

#### 2. Search & Detection Protocol
* **Initial Run**: Execute the search within the provided boundary files.
* **Lake Not Detected**: If the lake is not identified in the first run, update the search parameters to extend **150m** outside the given boundaries.
* **Lake Detected**: Once the lake is identified, the boundary file must be updated minimally to include the newly discovered lake perimeter.

