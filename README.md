# -markdown-buddy-EdehTochukwu
# Global E-Commerce Sales Performance Analysis

## Overview
This data science project analyzes a synthetic dataset containing global retail transactions. The goal is to evaluate historical sales trends, identify key revenue-driving geographic regions, and train a basic predictive model to forecast upcoming quarterly performance. 

## Project Structure
* `data/synthetic_sales.csv` — The core dataset containing transaction records.
* `scripts/sales_analysis.R` — The main data cleaning, visualization, and modeling script.
* `docs/sales_documentation.Rmd` — Step-by-step documentation detailing the script layout.
* `README.md` — Project landing page.
* `Reflection.md` — AI workflow reflection assignment.

## Installation & Setup
To run this project locally, clone this repository and open the project directory in RStudio or Posit Cloud:

```bash
git clone https://github.com
```

## Dependencies
This project relies on the following R packages. Ensure they are installed before executing the script:
* **tidyverse** (v2.0.0 or higher) - For data manipulation and plotting.
* **lubridate** (v1.9.3 or higher) - For dates and time-series extraction.

## Example Usage
You can run a quick summary of the dataset directly in R with the following snippet:

```r
library(tidyverse)

# Load the synthetic data
sales_data <- read_csv("data/synthetic_sales.csv")

# Quick preview of monthly revenue summaries
monthly_revenue <- sales_data %>%
  group_by(Month = floor_date(Date, "month")) %>%
  summarize(Total_Revenue = sum(Revenue, na.rm = TRUE))

print(head(monthly_revenue))
```

## License
Distributed under the MIT License. See `LICENSE` for more details.

---

### AI Assistance Disclosure
* **AI Tool Used:** Gemini (September 2026)
* **Main Prompts Provided:** 
  1. *"Explain what sections a good GitHub README for an R data analysis project should include."*
  2. *"Revise the sections list so it’s concise and uses Markdown headers and bullet formatting."*
  3. *"Here’s a summary of my R project: Global E-Commerce Sales Performance. Generate a professional README.md file using Markdown with Installation, Example Code, and License sections."*
* **Edits Made:** Replaced sample placeholder file paths with actual intended filenames (`sales_analysis.R`) and updated package dependency versions to reflect accurate R standards.

---

## AI Assistance Disclosure
In accordance with the assignment guidelines, this project utilized artificial intelligence for structural layout drafting and formatting assistance:

* **AI Tool Used:** Gemini (September 2026)
* **Main Prompts Provided:**
  1. *Seed Prompt:* "Explain what sections a good GitHub README for an R data analysis project should include."
  2. *Refinement Prompt:* "Revise the sections list so it’s concise and uses Markdown headers and bullet formatting."
  3. *Drafting Prompt:* "Here’s a summary of my R project: Global E-Commerce Sales Performance. Generate a professional README.md file using Markdown with Installation, Example Code, and License sections."
* **Changes Made After Review:** 
  * Replaced the generic template repository links with the actual required naming syntax (`markdown-buddy-[yourname]`).
  * Manually verified that all Markdown headers (`#`, `##`) and code block indicators rendered properly using GitHub's file preview window.
  * Ensured no AI calculation was utilized, maintaining manual code calculations as required by the course guidelines.
