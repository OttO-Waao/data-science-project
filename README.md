# data-science-project
# Job Posting Scraping and Analysis System (Job Data Science Project)

## 1. Problem or Research Question
This project aims to analyze public job posting data from a recruitment website (job001.cn) to answer the following questions: What are the differences in salary distributions across different cities and job categories? What are the specific impacts of work experience and education on salary? What are the most in-demand professional skills in the current job market?

## 2. Dataset Source and Usage Permissions
The data is sourced from publicly available web pages on `http://www.job001.cn`. This project is strictly for academic purposes and personal portfolio demonstration. It adheres to the website's scraping protocols and does not scrape any personal privacy data (such as contact information). Only public information such as job titles, company short names, salary ranges, and locations is extracted.

## 3. Methods and Tools
- **Data Acquisition**: Used `requests` and `BeautifulSoup` for web scraping and parsing.
- **Data Preprocessing**: Used `pandas` for deduplication, missing value imputation, and salary text cleaning (extracting numbers and converting them to a unified currency unit).
- **Data Analysis & Visualization**: Used `matplotlib` and `seaborn` to plot salary distribution bar charts, education requirement pie charts, city job count line charts, experience-salary scatter plots, and cross-analysis heatmaps.
- **Text Mining**: Used `jieba` for Chinese word segmentation and keyword extraction (TF-IDF), and `wordcloud` to generate a skill word cloud.

## 4. Key Findings and One Limitation
**Key Findings**:
1. The average salary for technical positions is significantly higher than that of marketing, administrative, and financial positions.
2. With the increase in work experience (1-3 years -> 3-5 years -> 5-10 years), the average salary shows a clear upward trend.
3. Keyword extraction reveals that "Python", "Java", "Data Analysis", and "Project Management" are the most frequently occurring in-demand skills.
**Limitation**: Due to anti-scraping restrictions on the website, a single run only scrapes the first 2 pages of each category (approximately a few dozen records), resulting in a limited sample size. Additionally, some job salaries are displayed as "Negotiable" or have extremely wide ranges, which may cause bias in the average salary calculation.

## 5. Instructions for Running the Analysis
1. Clone this repository locally.
2. Install dependencies: `pip install -r requirements.txt`
3. Run the main program: `python job_analysis.py` (or run all cells in the Jupyter Notebook).
4. In the terminal, select option `1` (Immediately update data and analyze).
5. The program will automatically scrape the data and generate visualization charts (saved as `.png` files) and an analysis report.
