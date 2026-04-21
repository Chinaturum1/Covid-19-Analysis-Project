# COVID-19 Global Impact Analysis — Power BI Dashboard

An interactive Power BI dashboard exploring the global footprint of the COVID-19 pandemic across cases, deaths, government policy responses, and vaccination efforts. The analysis draws on the [Our World in Data (OWID)](https://ourworldindata.org/covid-cases) COVID-19 dataset and is structured around three self-defined research themes.

---

## Repository Contents

| File | Description |
|---|---|
| `Covid_Project_Work.pbix` | Interactive Power BI dashboard (5 report pages) |
| `COVID19_Report.pptx` | PowerPoint summary report of findings |
| `README.md` | Project documentation |

---

## Research Questions

The analysis was structured around three themes developed independently for this project.

### Theme A — Global Intensity
- What were the overall cases and fatalities recorded due to Covid?
- What year had the highest number of cases?
- In what year did the most deaths occur?
- How frequent were there new fatalities and cases?
- What was the average reproduction rate recorded?

### Theme B — Geographic Impact
- What was the mortality rate in each continent, and which continent was most affected?
- What countries had the highest mortality rate?

### Theme C — Global Response & Prevention
- How strict overall were government policies regarding the pandemic? *(Stringency Index)*
- What could we note about the number of cases in countries with stricter policies and their death rate? Did a high Stringency Index contribute to lowering deaths and new cases, or did it not help?
- Were there enough vaccinations available for prevention?

---

## Dashboard Pages

**1. Impact Metrics**
Overview cards for total global cases and deaths, case fatality rate, top-affected countries and continents, and trend lines across years.

**2. New Cases**
Daily and cumulative new case tracking, top countries by new case volume, continental breakdown, and the ratio of new cases to total cases over time.

**3. New Deaths**
New death trends over time, top countries by new death count, continental comparisons, and the ratio of new deaths to total deaths.

**4. Vaccinations**
New vaccinations administered, people vaccinated, country and continent rankings by vaccination volume, and daily vaccination rate.

**5. Gov. Policies**
Stringency Index and reproduction rate by country and continent, policy trend lines across the pandemic timeline, and high-stringency day analysis.

---

## Dataset

**Source:** Our World in Data — COVID-19 Dataset  
**URL:** https://github.com/owid/covid-19-data  
**Coverage:** Global, daily records from January 2020 onwards  
**Key columns used:** `total_cases`, `total_deaths`, `new_cases`, `new_deaths`, `reproduction_rate`, `stringency_index`, `new_vaccinations`, `new_people_vaccinated_smoothed`

> **Note on data structure:** The OWID dataset includes aggregate rows for world regions, continents, and income groups alongside individual country rows. The data model accounts for this by filtering on non-blank continent values to isolate country-level records in relevant calculations.

---

## Data Model

The report uses a star schema with three tables:

- **COMPACT FACT TABLE** — daily metrics per location (cases, deaths, vaccinations, policy indices)
- **LOCATION DIM** — country and continent attributes
- **DATE DIM** — date hierarchy (Year, Quarter, Month, Day)

---

## Tools Used

- **Microsoft Power BI Desktop** — data modelling, DAX measures, and dashboard design
- **Microsoft PowerPoint** — summary report
- **Data source:** Our World in Data (CSV)

---

## Author

**Okonkwo Uchechukwu Faith**  
Data Analysis Project — 2025
