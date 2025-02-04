# Example Projects


## 1) Quick DFOS Strain Analyser — Ttkbootstrap GUI and Python-Based Data Processing — Private Repository


'Quick DFOS Strain Analyser' is a python-based GUI application designed to process, analyse, and visualise distributed fibre optic sensing (DFOS) strain data. The system efficiently handles large datasets using chunk-based data processing, integrates geometric transformations, and provides an interactive visualisation interface.

<figure style="text-align: center;">
  <iframe width="340" height="280"
    src="https://www.youtube.com/embed/0f-DgnXBncE?mute=1" 
    frameborder="0" allowfullscreen>
  </iframe>
  <figcaption>Figure 1: Video Demo of Quick DFOS Strain Analyser.</figcaption>
</figure>

<p>&nbsp;</p>

### Key Features
- **Efficient Data Handling** – Designed for large JSON-based DFOS strain datasets using chunk-based processing.
- **Strain Data Processing** – Extracts, resamples, and interpolates strain data for enhanced accuracy.
- **Geometry-Based Analysis** – Reads structured Excel-based DOF geometry and aligns strain data accordingly.
- **Graphical User Interface (GUI)** – Tkinter-based real-time data visualization and interaction.
- **Performance Optimisation** – Implements memory management techniques including garbage collection and process monitoring.
- **Logging & Debugging Support** – Uses structured logging for error tracking and performance analysis.

<p>&nbsp;</p>

### Technology Stack

| Component                        | Technology Used                                   |
| -------------------------------- | ------------------------------------------------- |
| **Frontend**                     | Tkinter with TTKBootstrap (GUI Framework)         |
| **Backend**                      | Python (NumPy, SciPy, Pandas, multiprocessing)    |
| **Data Handling**                | JSON chunk-based strain data processing           |
| **Geometry Processing**          | Pandas for structured Excel-based transformations |
| **Interpolation and Resampling** | SciPy's `interp1d`, NumPy's `polyfit`             |
| **Performance Optimization**     | `gc`, `psutil`, multiprocessing                   |
| **Logging and Debugging**        | Python’s `logging` module, `traceback`            |
| **File Handling**                | OS, shutil, tempfile                              |

<p>&nbsp;</p>

### Core Processing Workflow
1. **Data Ingestion**: Reads DFOS strain data in chunks to minimise memory footprint.
2. **Preprocessing**: Extracts strain values, applies resampling, and interpolates missing data.
3. **Geometric Alignment**: Reads and processes Excel-based DOF geometry.
4. **Visualisation**: Displays real-time strain variations via the Tkinter-based GUI.
5. **Performance Enhancements**: Implements structured logging, garbage collection, and parallel execution.

<p>&nbsp;</p>

### Project Structure
```
├── processing/                  # Core strain and geometry processing modules
│   ├── strain_processing.py     # Extracts, resamples, and interpolates strain data
│   ├── geometry_processing.py   # Reads and aligns DOF geometry with strain measurements
├── gui/                         # Graphical user interface components
│   ├── gui.py                   # Tkinter-based visualisation interface
├── utils/                       # Logging and file handling utilities
│   ├── file_helpers.py          # Handles file operations
│   ├── logging_helpers.py       # Manages structured logging
├── main.py                      # Entry point for application execution
├── requirements.txt             # Dependencies
```

<p>&nbsp;</p>

### Building the Executable
This project can be converted into a executable using PyInstaller:
```sh
pip install pyinstaller
pyinstaller --onefile --windowed --name "AMRC_DFOS_Analyser" main.py
```
- The `--onefile` flag bundles everything into a single executable.
- The `--windowed` flag ensures the GUI runs without a terminal.
- The output EXE will be found in the `dist/` folder.

<!-- ========================================================================================= -->

<p>&nbsp;</p>

## 2) [Python Scripting for Composite Structural Simulations in Abaqus](https://github.com/semajrd1/Abaqus-Macros) — Public Repository

This project is an Abaqus Python script that automates the Finite Element (FE) modeling of composite straps with pin-loaded connections. It defines geometry, meshing, material properties, boundary conditions, and contact interactions, allowing for efficient simulation setup and execution in Abaqus CAE. The script includes cohesive zone modeling (CZM) for analyzing delamination and failure mechanisms, making it ideal for composite structure research and engineering applications.

<figure style="text-align: center;">
  <img src="assets/Pin_Strap_FEA.png" alt="Figure Caption" width="300">
  <figcaption>Figure 2: Example FEM Generated Via Python Scripting.</figcaption>
</figure>

<p>&nbsp;</p>

### Features
- **Parametric Geometry Creation** – Define strap and pin dimensions in the script for custom models.
- **Advanced Material Properties** – Supports orthotropic composites and isotropic metallic materials.
- **Cohesive Zone Modeling (CZM)** – Enables delamination and failure predictions in laminated composites.
- **Mesh Generation & Refinement** – Uses adaptive meshing with fine curved-edge refinements.
- **Automated Boundary Conditions & Loads** – Applies symmetry constraints and displacement-driven loading.
- **Contact & Interaction Definition** – Includes tie constraints, cohesive contact, and frictional interactions.
- **Batch Job Submission** – Runs simulations in Abaqus/CAE without manual intervention.

<p>&nbsp;</p>

## 3) [Responsive Flask Web Application with SQL Database](https://github.com/semajrd1/Isabelle-Baptism-Website) — "Isabelle's Baptism Website" — Public Repository

This project is a Flask-based web application designed to manage guest RSVPs and provide event details for Isabelle’s baptism. The system is built using a PostgreSQL relational database, a responsive front-end, and a secure API-driven backend. It includes a structured MVC pattern and is designed to be scalable and easily deployable.

<figure style="text-align: center;">
  <iframe width="340" height="280" 
    src="https://www.youtube.com/embed/7SG_m_pFNII?mute=1" 
    frameborder="0" allowfullscreen>
  </iframe>
  <figcaption>Figure 3: Video Demo of Isabelle's Baptism Web App.</figcaption>
</figure>

<p>&nbsp;</p>

### Key Features
- **Event Information System** – Displays event details with dynamic content rendering through Jinja2 templates.
- **Guest RSVP Management** – Enables user form submission with real-time validation and database storage.
- **Flask Backend with SQLAlchemy ORM** – Manages data persistence with PostgreSQL, with SQLite fallback for local testing.
- **Modular and Scalable Architecture** – Implements separation of concerns with distinct routing, template, and static file management.
- **RESTful API Integration** – Supports data exchange and future expansion into mobile/web applications.
- **Responsive Frontend** – Uses CSS Grid and SASS for layout management and optimized UI across devices.

<p>&nbsp;</p>

### Technology Stack
- **Frontend:** HTML, CSS (SASS), JavaScript
- **Backend:** Flask (Python), Jinja2, SQLAlchemy ORM
- **Database:** PostgreSQL (primary), SQLite (fallback for local development)
- **Security Measures:** Environment variable configurations, database migration compatibility, and input validation.

<p>&nbsp;</p>

### Project Structure
```
├── instance/          # Flask instance folder (e.g., database, sensitive data)
├── static/            # CSS, JavaScript, and images
├── templates/         # HTML templates
├── virtual/           # Virtual environment (not included in Git)
├── .gitignore         # Git ignore file
├── app.py             # Main Flask application
├── requirements.txt   # Dependencies
```

<p>&nbsp;</p>

---

# Technical Competencies

- **Programming Languages**: Python, SQL, MATLAB, C, JavaScript, LaTeX
- **Machine Learning & AI**: TensorFlow, PyTorch, Scikit-learn, YOLO, K-means clustering, Deep Learning
- **Cloud & Databases**: AWS (Lambda, S3, DynamoDB, EC2), Snowflake, PostgreSQL, MySQL
- **Engineering & Simulation Software**: Abaqus, Ansys Workbench, Fusion 360
- **Data Visualization**: Matplotlib, Plotly, Seaborn, Power BI

<p>&nbsp;</p>

---

# Conferences & Presentations

1. **Distributed Fibre Optic Sensing for Real-Time Monitoring of VARTM Manufacturing and Processing of Composite Laminates** – *FPCM 2025, Abu Dhabi, UAE.* **James R. Davidson***, Fayyaad Amod, Oliver M. Simpson, Hanisa Hasrin, Danijela Stankovic, Conchúr M. Ó Brádaigh, Samuel Furtado.

2. **Flow Front Monitoring and Permeability Analysis of Pneumatically Spliced Woven Fabrics** – *FPCM 2025, Abu Dhabi, UAE.* Fayyaad Amod*, **James R. Davidson**, Mohammed S. Alotaibi, Hanisa Hasrin, Danijela Stankovic, Conchúr Ó Brádaigh, Colin Robert.

3. **On-Line Pneumatic Compaction System for Consolidation on a Powder Polymer Towpreg Processing Line** – *FPCM 2025, Abu Dhabi, UAE.* Hanisa Hasrin*, Fayyaad Amod, **James R. Davidson**, Conchúr M. Ó Brádaigh, Colin Robert.

4. **Influence of Stacking Sequence and Exclusion Diameter on Mechanical Performance of Notched Angle-Ply CF-Epoxy Laminates** – *SAMPE Europe Conf. 2024, Belfast, Northern Ireland.* **James R. Davidson***, Danijela Stankovic, James A. Quinn, James M. Maguire, Gabrielis Cerniauskas, Ankur Bajpai, Colin Robert, Conchúr M. Ó Brádaigh, Edward D. McCarthy.

5. **Unlocking Potential: Exploring the Use of Waste Mixed Plastics and Waste Fibres in High-Performance C-Sections** – *ICCS27, Sep 2024, Bologna, Italy.* Danijela Stankovic*, **James R. Davidson**, Saskia Bulstrode, Dilum Fernando, Dipa Ray.

6. **Exploring Seamless Fibre Transitions: Mechanical Characterisation Of Pneumatically Spliced Connections For Multi-Material Composites** – *ECCM21, Jul 2024, Nantes, France.* **James R. Davidson***, Shunhua Mai, Fayyaad Amod, Danijela Stankovic, Mohammed S. Alotiabi, Murat Çelik, Hanisa Hasrin, Colin Robert, Edward D. McCarthy, Conchúr M. Ó Brádaigh. DOI: 10.60691/yj56-np80.

7. **Tailored Hybrid Composite Preforms by Automated Fibre Placement of Powder Epoxy-Based Towpregs** – *ECCM21, Jul 2024, Nantes, France.* Murat Çelik*, Arun Kumar Alapati, **James R. Davidson**, Hanisa Hasrin, David May, Colin Robert, Conchúr Ó Brádaigh. DOI: 10.60691/yj56-np80.

8. **Recycled Extruded Fibre-Reinforced Thermoplastics for a Sustainable Future: Tensile, Flexural, and DMA Performance Assessment** – *Polymers 2024, Athens, Greece.* **James R. Davidson***, Anastasia P. Tsavea, Alejandro Perez, Danijela Stankovic, Fayyaad Amod, Hanisa Hasrin, Colin Robert, Conchúr M. Ó Brádaigh. Poster-DOI: 10.13140/RG.2.2.14623.98724.

9. **Numerical and experimental investigation of wrap-around effect of electrostatic powder deposition on a powder epoxy tapeline** – *Polymers 2024, Athens, Greece.* Hanisa Hasrin*, Murat Çelik, Thomas Noble, **James R. Davidson**, Conchúr M. Ó Brádaigh, Colin Robert. Poster-DOI: 10.13140/RG.2.2.25752.00005.

10. **Sustainability in Construction: Transforming Waste Plastics into High-Value Composites** – *Polymers 2024, Athens, Greece.* Danijela Stankovic Davidson*, Kit O'Rourke, **James R. Davidson**, Christopher Griffin, Keith Doyle, Dipa Ray. Poster-DOI: 10.13140/RG.2.2.17892.59528.

11. **A Unique Approach to Adhesive Joint Design: Composite Layup Tailoring for Bondline Stress Optimisation** – *FiBreMod Conf., Dec 2019, Leuven, Belgium.* **James R. Davidson***, Edward D. McCarthy, Conchúr M. Ó Brádaigh.


<p>&nbsp;</p>

---

# Publications

1. **Fracture-Mechanical Properties of Tailored Epoxy Nanocomposites at Elevated Temperatures** (2024) – *Journal of Applied Polymer Science*. Ankur Bajpai*, Arun Kumar Alapati, **James R. Davidson**, Prateek Saxena, Bernd Wetzel. DOI: [10.1002/app.56443](https://doi.org/10.1002/app.56443).

2. **Experimental and Numerical Investigations on the Tensile Response of Pin-Loaded Carbon Fibre Reinforced Polymer Straps** (2024) – *Composites Science and Technology*. Danijela Stankovic*, **James R. Davidson**, Valentin Ott, Luke A. Bisby, Giovanni P. Terrasi. DOI: [10.1016/j.compscitech.2024.110915](https://doi.org/10.1016/j.compscitech.2024.110915).

3. **Developing Hybrid C-Sections from Waste and Recycled Composite Materials** (2024) – *Sustainable Materials and Technologies*. Danijela Stankovic, Saskia Bulstrode, **James R. Davidson**, Dilum Fernando, Dipa Ray*. Volume 41. DOI: [10.1016/j.susmat.2024.e01102](https://doi.org/10.1016/j.susmat.2024.e01102).

4. **Advanced Ultrasonic Inspection of Thick-Section Composite Structures for In-Field Asset Maintenance** (2023) – *Polymers*. James A. Quinn*, **James R. Davidson**, Ankur Bajpai, Conchúr M. Ó Brádaigh, Edward D. McCarthy. 15(15). DOI: [10.3390/polym15153175](https://doi.org/10.3390/polym15153175).

5. **Mechanical Characterisation of Pneumatically-Spliced Carbon Fibre Yarns as Reinforcements for Polymer Composites** (2022) – *Materials & Design*. **James R. Davidson***, James A. Quinn, Claudia Rothmann, Ankur Bajpai, Colin Robert, Conchúr M. Ó Brádaigh, Edward D. McCarthy. Volume 213. DOI: [10.1016/j.matdes.2021.110305](https://doi.org/10.1016/j.matdes.2021.110305).

6. **Experimental Study on the Interlaminar Fracture Properties of Carbon Fibre Reinforced Polymer Composites with a Single Embedded Toughened Film** (2021) – *Polymers*. Evanthia J. Pappa*, James A. Quinn, James J. Murray, **James R. Davidson**, Conchúr M. Ó Brádaigh, Edward D. McCarthy. 13(23):4103. DOI: [10.3390/polym13234103](https://doi.org/10.3390/polym13234103).

7. **Powder Epoxy for One-Shot Cure, Out-of-Autoclave Applications: Lap Shear Strength and Z-Pinning Study** (2021) – *Journal of Composite Science*. Thomas Noble, **James R. Davidson**, Christophe Floreani, Ankur Bajpai, William Moses, Thomas Dooher, Alistair McIlhagger, Edward D. McCarthy, Conchúr M. Ó Brádaigh, Colin Robert*. 5(9):225. DOI: [10.3390/jcs5090225](https://doi.org/10.3390/jcs5090225).

8. **Studies on the Modification of Commercial Bisphenol-A-Based Epoxy Resin Using Different Multifunctional Epoxy Systems** (2021) – *Applied Mechanics*. Ankur Bajpai*, **James R. Davidson**, Colin Robert. 2(2):419-430. DOI: [10.3390/jcs5090225](https://doi.org/10.3390/jcs5090225).



<p>&nbsp;</p>

---

# Certifications

- **Dynamic Public Speaking** – University of Washington (Coursera)
- **DeepLearning.AI TensorFlow Developer** – DeepLearning.AI
- **IBM AI Engineering** – IBM Skills Network
- **CS50x Harvard Introduction to Computer Science** – Harvard University
  
# Online Profiles

- [LinkedIn](https://www.linkedin.com/in/james-davidson-698431259/)
- [Google Scholar](https://scholar.google.com/citations?user=OzPJcVwAAAAJ&hl=en)
- [GitHub](https://semajrd1.github.io/Portfolio/)
