# Mobile App Growth Analysis: Correlations Between Downloads, Advertising, and Revenue

## Introduction
The project was undertaken to investigate the relationships between various mobile app metrics such as downloads, consumer spending (revenue), and advertising spending over the years. The primary research question explored was: *Do higher app downloads always correspond to higher revenue?* Additionally, the study aims to analyze how advertising spending correlates with app downloads and revenue growth, and to assess how the growth in app spending compares with the growth of app downloads. 

The tested hypothesis is that higher downloads would lead to higher revenue, and that there would be a strong correlation between advertising spending and the other metrics over time.

## Selection of Data
The dataset used for this analysis was sourced from Statista and covers mobile app downloads, consumer spending, and advertising spending from 2016 to 2023. The following datasets were merged:

1. **Mobile App Downloads**: Data on the total number of mobile app downloads worldwide from 2016 to 2023.
2. **Consumer Spending (Revenue)**: Data on consumer spending related to mobile apps (revenue) during the same period.
3. **Mobile Advertising Spending**: Data on the worldwide mobile advertising spending from 2016 to 2023.

Before analysis, the data underwent preprocessing, which included:
- **Merging** the datasets based on the year.
- **Handling Missing Data**: Missing values were removed to ensure the integrity of the analysis.
- **Calculating Growth**: Year-over-year growth rates for downloads, consumer spending, and advertising spending were calculated using percentage change.

## Methods
To answer the research questions, Python was used with the following tools:

- **Pandas**: For data manipulation, merging, and calculation of growth percentages.
- **Matplotlib**: For data visualization and plotting.
- **Numpy**: For performing numerical operations.

The Python code first merged the datasets and then calculated the year-over-year growth percentages for downloads, revenue, and ad spending. The correlation coefficients between these growth variables were calculated using Pearson correlation.

- **Merging Data**: Datasets were merged using `pd.merge()` based on the 'Year' column.
- **Growth Calculation**: Growth percentages were calculated using `.pct_change()` method from Pandas.
- **Visualization**: Growth trends were visualized using `matplotlib.pyplot`, displaying the growth in downloads, revenue, and ad spending over time.

## Results
### 1. Do higher app downloads always correspond to higher revenue?
- While there is a general trend that higher app downloads correspond to higher revenue, exceptions were observed. Specifically, there were instances where revenue growth outpaced download growth, indicating that factors like higher in-app purchases, improved monetization strategies, or increased average user spending could be influencing revenue more than downloads.

### 2. How does the growth of mobile app spending compare to the growth of downloads?
- The growth of mobile app spending shows a positive trend over the years, closely following the rise in downloads. However, advertising spending grew at a slightly faster pace than downloads, suggesting that increased marketing efforts might have been a key factor in driving app usage and revenue.

### 3. How does mobile advertising spending correlate with app downloads and revenue growth?
- The analysis found a strong correlation between advertising spending growth and download growth (0.98), but a weaker correlation between advertising spending growth and revenue growth (-0.08). This indicates that while advertising may drive more downloads, its impact on revenue is less direct and may be influenced by other factors such as in-app purchases or subscription models.

Visualizations such as line plots were used to show the year-over-year growth in downloads, revenue, and advertising spending.

## Discussion
The results highlight the importance of not only focusing on downloads but also on other factors like advertising and monetization strategies to assess mobile app growth effectively. Although higher downloads generally correlate with higher revenue, exceptions exist due to different monetization strategies. Advertising spending plays a crucial role in driving downloads but does not always correlate directly with revenue, suggesting that other variables like user retention, in-app purchases, and subscription models are important for understanding revenue growth.

Future research could further explore the impact of specific app categories, regional differences, and more detailed monetization strategies on app growth metrics. Additionally, incorporating data from individual app types could provide more granular insights into the drivers of mobile app success.

## Coding and Data Files
The analysis is implemented in a Jupyter Notebook. The main Python code and datasets used for the analysis are available at the following link:

- [Main Analysis Notebook](./main_analysis.ipynb)

Data files used in the analysis can be found in the `data/` folder.

## References
[1] Statista, “Mobile app revenue worldwide by segment,” *Statista*, 2024. [Online]. Available: https://www-statista-com.ezproxywit.flo.org/forecasts/1262892/mobile-app-revenue-worldwide-by-segment. [Accessed: Dec. 7, 2024].

[2] Statista, “Global mobile app spend (consumer),” *Statista*, 2024. [Online]. Available: https://www-statista-com.ezproxywit.flo.org/statistics/870642/global-mobile-app-spend-consumer/. [Accessed: Dec. 7, 2024].

[3] Statista, “Worldwide free and paid mobile app store downloads,” *Statista*, 2024. [Online]. Available: https://www-statista-com.ezproxywit.flo.org/statistics/271644/worldwide-free-and-paid-mobile-app-store-downloads/. [Accessed: Dec. 7, 2024].

[4] Statista, “Mobile internet advertising revenue worldwide,” *Statista*, 2024. [Online]. Available: https://www-statista-com.ezproxywit.flo.org/statistics/303817/mobile-internet-advertising-revenue-worldwide/. [Accessed: Dec. 7, 2024].

