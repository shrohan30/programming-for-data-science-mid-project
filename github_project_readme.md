# Global Energy Transition: Growth in Energy Demand, Fossil-Fuel Dependence and the Rise of Renewables

**Course:** BDS3106 – Programming for Data Science  
**Semester:** Fall 2026–2027  
**Institution:** American International University–Bangladesh (AIUB), Faculty of Science and Technology  
**Project Phase:** Mid-Term Project (Phase I)

---

## 📌 Project Overview
Energy underpins economic growth, yet it remains the primary driver of global greenhouse-gas emissions. As global energy demand continues to rise alongside ongoing fossil-fuel reliance, understanding the pace at which low-carbon alternatives are scaling is essential for evaluating climate progress.

In **Phase I** of this project, we conduct an exploratory data analysis (EDA) of global and national energy trajectories using Python to answer four core research questions:

| ID | Research Question | Key Variables Analyzed |
| :--- | :--- | :--- |
| **RQ1** | How have global primary energy consumption and electricity generation changed over time? | `primary_energy_consumption`, `electricity_generation` (`World`) |
| **RQ2** | Is the world moving away from fossil fuels, and how fast are renewables growing in comparison? | `fossil_fuel_consumption`, `renewables_consumption` |
| **RQ3** | Which countries consume the most energy, and which rely most on renewable electricity? | `primary_energy_consumption`, `renewables_share_elec` |
| **RQ4** | How strongly are economic size, population, and energy mix associated with energy use and emissions? | `gdp`, `population`, `greenhouse_gas_emissions`, `carbon_intensity_elec`, `renewables_share_energy` |

---

## 📊 Dataset & Ethical Use
This project uses the **Our World in Data (OWID) Energy Dataset** (`energy-data.csv`), which compiles official statistics from the Energy Institute Statistical Review of World Energy, Ember, the U.S. EIA, and related sources.

* **Source Repository:** [github.com/owid/energy-data](https://github.com/owid/energy-data)
* **Dimensions:** `23,232 rows × 131 columns` (`3` identifiers: `country`, `year`, `iso_code`; `128` numeric indicators)
* **Coverage:** `1900–2025` across `314` entities (`220` countries totaling `17,134` country-year records, plus regional/income aggregates)
* **License & Ethical Compliance:** Published under **Creative Commons BY 4.0**. In compliance with data-sharing guidelines, the raw CSV file is **not redistributed** in this repository. All records represent aggregate national statistics with zero personal or sensitive information, and missing values (`NaN`) were preserved rather than imputed.

---

## 📁 Repository Structure

```text
├── PDS_midproject.ipynb                  # Main Jupyter/Colab notebook organized into 5 analytical stages
├── BDS3106_Midterm_Project_Report.pdf    # Phase I Mid-Term Project Report (PDF)
├── BDS3106_Midterm_Project_Report.docx   # Phase I Mid-Term Project Report (Word Document)
├── DATA_SOURCE.md                        # Dataset link, schema summary, and CC BY 4.0 attribution note
└── README.md                             # Project documentation, setup guide, and team contributions
```

*(Note: `energy-data.csv` and `energy-data_cleaned.csv` are excluded from version control; follow the instructions below to download and generate them locally.)*

---

## ⚙️ Dependencies & Environment
The analysis was developed in **Python 3** (Google Colab / Jupyter Notebook) using the following libraries:
* `pandas`
* `numpy`
* `matplotlib`
* `jupyter` / `notebook`

Install the required packages via `pip`:
```bash
pip install pandas numpy matplotlib jupyter
```

---

## 🚀 How to Reproduce
1. **Clone this repository:**
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```
2. **Download the dataset:**
   Download `energy-data.csv` directly from the official OWID repository:
   ```bash
   curl -L -o energy-data.csv https://raw.githubusercontent.com/owid/energy-data/master/owid-energy-data.csv
   ```
   *(Alternatively, download it manually from [github.com/owid/energy-data](https://github.com/owid/energy-data) and place `energy-data.csv` in the root project folder.)*
3. **Run the notebook:**
   Launch Jupyter Notebook or open `PDS_midproject.ipynb` in Google Colab / VS Code and run all cells sequentially from top to bottom:
   ```bash
   jupyter notebook PDS_midproject.ipynb
   ```
   Running the notebook validates the raw data, separates country records (`iso_code` present) from regional aggregates, exports `energy-data_cleaned.csv`, and generates all statistical summaries and Figures 1–8.

---

## 🔍 Key Preliminary Findings (Phase I)
1. **Rising Global Demand:** World primary energy consumption rose **+308%** from `43,360 TWh` (1965) to `176,737 TWh` (2024), while global electricity generation more than doubled (**+102.5%**) between 2000 and 2024.
2. **Fossil Fuels Losing Share, Still Growing in Volume:** Between 2000 and 2024, fossil fuels' share of primary energy declined from **85.6% to 80.6%** as renewables more than tripled (**+218.7%**). However, absolute fossil-fuel consumption still grew by `+48,000 TWh`, driving an **+81.2%** increase in electricity-sector greenhouse-gas emissions.
3. **High Concentration of Consumption:** In 2023, **China** (`47,072 TWh`) and the **United States** (`26,217 TWh`) together accounted for **~42.6%** of global primary energy consumption.
4. **Renewable Leaders vs. Major Consumers:** Countries with the highest average renewable electricity shares (e.g., Bhutan, Lesotho, Paraguay, Iceland, Nepal, DR Congo, Ethiopia, Albania, Norway, Namibia at `97–100%`) are predominantly smaller hydropower-rich economies rather than top total energy consumers.
5. **Scale vs. Clean-Energy Signal:** Total energy use and emissions correlate strongly with GDP ($r = 0.982$) and electricity generation ($r = 0.987$) due to economic scale, whereas a higher renewable energy share correlates negatively with electricity carbon intensity ($r = -0.700$).

---

## 👥 Team Member Contributions

| Member | Student Name | Student ID | Assigned Role & Key Contributions |
| :--- | :--- | :--- | :--- |
| **Member 1** | `[Enter Member 1 Name]` | `[XX-XXXXX-X]` | Data loading, dataset structure understanding, and initial schema inspection |
| **Member 2** | `[Enter Member 2 Name]` | `[XX-XXXXX-X]` | Data validation, missing-value handling, entity separation, and preprocessing |
| **Member 3** | `[Enter Member 3 Name]` | `[XX-XXXXX-X]` | Descriptive statistical analysis, exploratory data analysis (EDA), and visualisations |
| **Member 4** | `[Enter Member 4 Name]` | `[XX-XXXXX-X]` | Renewable-energy deep dive, correlation analysis, and synthesis of preliminary findings |
| **Member 5** | `[Enter Member 5 Name]` | `[XX-XXXXX-X]` | Limitations & next steps review, report compilation, and repository/reproducibility packaging |

---

## 📚 References
1. Our World in Data (2025). *Energy dataset* [CSV, CC BY 4.0]. GitHub: https://github.com/owid/energy-data
2. Ritchie, H., Rosado, P., & Roser, M. (2022). *Energy*. Our World in Data. https://ourworldindata.org/energy
3. Energy Institute (2024). *Statistical Review of World Energy*. https://www.energyinst.org/statistical-review
4. Ember (2024). *Global Electricity Review*. https://ember-energy.org