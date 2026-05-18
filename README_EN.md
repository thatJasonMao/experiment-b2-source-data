# VR Evacuation Experiment — Source Data & Statistical Results

## 1. About This Repository

This repository has been specifically prepared for the peer review of a manuscript submitted to **Advanced Engineering Informatics**. In the spirit of data transparency and openness, we make the raw experimental data, publication-quality figures with detailed data reports, and statistical analysis results publicly available here, so that reviewers and readers can inspect, verify, and reproduce the findings.

The study investigates how smoke concentration and the number of non-player characters (NPCs) influence evacuation decision-making and visual attention behavior in a virtual reality (VR) fire evacuation experiment. Eye-tracking and movement trajectory data were collected from multiple participants under varying smoke density and NPC density conditions.

## 2. Repository Structure

This repository is organized into three major sections:

### 📁 RawData — Raw Experimental Data

The `RawData/` directory contains raw data collected from all participants across all experimental trials. Each trial is stored in a folder named `Trial_<SHA256-Hash>` and includes two CSV files:

| File | Description |
|------|-------------|
| `EyeGaze_Simulation_Info_*.csv` | Eye-tracking data for the trial, including timestamps, gaze point coordinates, and gaze target classification |
| `Subject_Simulation_Info_*.csv` | Movement trajectory data for the trial, including timestamps, position coordinates, and velocity |

### 📁 Figures — Publication-Quality Figures & Data Reports

The `Figures/` directory is organized by figure category and provides high-resolution PNG versions of all core figures from the manuscript, accompanied by detailed data reports (CSV/TXT format) to facilitate verification of the underlying data.

| Subdirectory | Description |
|-------------|-------------|
| `GazeSpatialPattern/` | Gaze spatial distribution patterns at each decision point (DP1-DP4): DBSCAN clustering results and KDE heatmaps, with cluster statistical reports in `Reports/` |
| `Hesitations/` | Spatial distribution of hesitation points under different smoke concentration and NPC count conditions, with hesitation point coordinate data in `Reports/` |
| `SpeedPattern/` | Speed distribution density heatmaps, planar velocity vector plots, trajectory speed curves, and overall speed distribution analysis for each decision point |
| `Trajectories/` | Evacuation trajectory comparison plots across different smoke concentration and NPC count conditions |

### 📁 Statistics — Statistical Results Referenced in the Manuscript

The `Statistics/` directory contains the final statistical results referenced in the manuscript.

| Subdirectory | File | Description |
|-------------|------|-------------|
| `Behaviors/` | `BehavioralFeatures.xls` | Participant behavioral feature statistics |
| `Choices/` | `DirectionalChoices.xlsx` | Directional choice statistics |
| `FixationDuration/` | `FixationDuration_Mean.xlsx` / `FixationDuration_Total.xlsx` | Mean and total fixation duration statistics |
| `GlobalMetrics/` | `EvacuationEfficiency.xlsx` | Global evacuation efficiency metrics |
| `PathMetrics/` | `PathEfficiency.xlsx` | Path efficiency metrics |
| `Saccade/` | `SaccadeCount.xlsx` | Saccade count statistics |

## 3. Data Privacy & Ethics Statement

To protect participant privacy and comply with research ethics standards, the following anonymization measures have been applied to this repository:

- **Participant Identity Anonymization**: All personally identifiable information (including name, age, and gender) has been irreversibly anonymized using the **SHA-256** hashing algorithm. The hash value in each trial folder name (`Trial_<Hash>`) is generated from participant identity information combined with a trial index, making it impossible to reverse-engineer the original identity.
- **Limited Data Disclosure**: Data related to participants' personal experiences, psychological questionnaire scales (e.g., PANAS, SSQ, GSE, ITS), and other sensitive information that could potentially enable indirect identification are **not included** in this public disclosure. Requests for such data should be directed to the corresponding author in writing. Access will be granted on a case-by-case basis, subject to compliance with research ethics standards and data protection regulations.

## 4. License

This project is open-sourced under the **MIT License**. See [LICENSE](LICENSE) for details.
