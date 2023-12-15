# Global-Life-Expectancy-Prediction-Model

## Introduction

Our project centers around utilizing data on average life expectancy from the World Health Organization, spanning 179 countries between 2000 and 2015. Our objective is to construct a predictive regression model, considering various factors, to offer insights into enhancing a country's average life expectancy. The ultimate aim is to empower nations with proactive measures, enabling them to address critical factors and potentially avert national crises, ultimately fostering longer and healthier lives.

Our progress intends to identify pivotal variables impacting average life expectancy, crafting models that enable leaders to make informed, data-driven decisions. Our goal is to develop a regression model with high prediction accuracy, emphasizing relevant variables and extending predictions to unseen data. Additionally, we aim to uncover insights on the variables most influencing a nation's life expectancy, proposing strategies for optimization.

In terms of statistical methodology, we plan to leverage various visual plots (Ex. Residual Plots) to validate model assumptions and depict life expectancy trends globally. Through regression techniques, we aim to select an accurate prediction model, verify assumptions, and provide valuable insights for world leaders.

This project holds personal significance for us, particularly those with roots in developing nations. We aspire to contribute to the improvement of living conditions in these regions, promoting longer and healthier lives to stimulate overall national growth. We firmly believe that enhancing living conditions globally will yield mutual benefits for people worldwide, fostering a stronger and more interconnected world.

## Dataset

The dataset, sourced from Kaggle (Lasha., 2023), comprises information from 179 countries spanning the years 2000-2015 and encompasses 21 features. Key variables such as Population, GDP, and Life Expectancy were inputted using World Bank data. Details on vaccinations, alcohol consumption, BMI, HIV incidents, mortality rates, and thinness were derived from World Health Organization datasets, while schooling information was obtained from Our World in Data, a project of the University of Oxford. The dataset introduces a variable classifying countries as Developed or Developing, adhering to definitions provided by the World Trade Organization and the United Nations.

Key features include:

1. **Country:** List of the 179 countries.
2. **Region:** The distribution of 179 countries across 9 regions, including Africa, Asia, Oceania, European Union, Rest of Europe, etc.
3. **Year:** Observed years ranging from 2000 to 2015.
4. **Infant Deaths:** Represents infant deaths per 1000 population.
5. **Under-Five Years Old Deaths:** Represents deaths of children under five years old per 1000 population.
6. **Adult Mortality:** Represents deaths of adults per 1000 population.
7. **Alcohol Consumption:** Represents recorded alcohol consumption in liters of pure alcohol per capita for individuals aged 15 and above.
8. **Hepatitis B:** Represents the percentage of coverage of Hepatitis B (HepB3) immunization among 1-year-olds.
9. **Measles:** Represents the percentage of coverage of Measles-containing vaccine first dose (MCV1) immunization among 1-year-olds.
10. **BMI:** A measure of nutritional status in adults, calculated as a person's weight in kilograms divided by the square of their height in meters (kg/m2).
11. **Polio:** Represents the percentage of coverage of Polio (Pol3) immunization among 1-year-olds.
12. **Diphtheria:** Represents the percentage of coverage of Diphtheria tetanus toxoid and pertussis (DTP3) immunization among 1-year-olds.
13. **Incidents_HIV:** Incidents of HIV per 1000 population aged 15-49.
14. **GDP per Capita:** GDP per capita in current USD.
15. **Population (Millions):** Total population in millions.
16. **Thinness (10-19 Years):** Prevalence of thinness among adolescents aged 10-19 years (BMI < -2 standard deviations below the median).
17. **Thinness (5-9 Years):** Prevalence of thinness among children aged 5-9 years (BMI < -2 standard deviations below the median).
18. **Schooling:** Average years that people aged 25 and above spent in formal education.
19. **Economy Status (Developed):** Developed country.
20. **Economy Status (Developing):** Developing country.
21. **Life Expectancy:** Average life expectancy of both genders in different years from 2010 to 2015.

## Methodology

We aim to streamline our model selection process by employing a systematic approach. Initially, we will utilize forward selection, followed by backward selection and stepwise methods to identify the most impactful variables. Subsequently, we will construct a new model incorporating consistently selected variables and conduct a best subset model selection. This strategy optimizes computational resources by eliminating insignificant variables first. To further refine our model, we will explore higher order and interaction terms. This approach ensures that we consider the best variables identified through various methods and assess if there are superior model subsets. Our goal is to strike a balance between computational efficiency and a thorough search for the best model, ensuring a robust selection process.

The project unfolds in two main phases. First, we conduct an extensive model selection process, followed by the identification of interaction terms and higher order terms, and then confirming adherence to regression assumptions. The challenge lies in the subjective nature of model selection, requiring us to leverage collective knowledge. There is no definitive "wrong" answer in this step, emphasizing the need for a careful and informed decision-making process. In the event that assumptions are not met, we would utlize corrective actions such as variable deletion for multicollinearity, log transformation, or box-cox transformation.

Our work is divided into two parts: Lukas and Shabbir will focus on selecting the best model, while Gurdeep and Harjot will enhance the model with higher order terms, interaction terms, and assess regression assumptions. Concluded with a joint effort to finalize the write up and report.

## Results

$\frac{life\_expectancy^{3.33}-1}{3.33} = -774459.69 + 122320.49x{schooling}\\ + 2257.98x_{polio} + 10.96x_{gdp/capita} + 36066.39x_{bmi} - 150716.01x_{incidents hiv} -\\ 0.00016x^2_{gdp/capita} + 0.0000000008x^3_{gdp/capita} +  4852.97x_{incidents hiv}*x_{bmi} - \\4396.57x_{schooling}*x_{bmi}$

Our exhaustive regression model selection process unveiled crucial predictors significantly linked to life expectancy. Notably, variables such as schooling, Polio immunization coverage, GDP per Capita, BMI, and incidents of HIV emerged as influential factors. The model revealed that the average number of years of schooling is associated with increase in life expectancy, advocating for investments in education to foster longer lives. Similarly, higher Polio immunization coverage exhibited a positive correlation with life expectancy, suggesting fortified immunization programs for improved life spans. Surprisingly, the relationship between GDP per Capita and life expectancy showcased a cubic trend. Encouraging healthy BMI ranges and effective management of HIV incidents were also pivotal, showcasing positive correlations with longer life expectancy. This nuanced understanding challenges the traditional belief in continual economic growth as the sole driver of increased life spans. Our model's insights offer strategic guidance to nations, advocating for a holistic approach encompassing education, healthcare initiatives, balanced economic growth, and disease management to foster longer and healthier lives among populations.

## Conclusion

The approach undertaken for our project exhibits promise in uncovering influential factors impacting life expectancy across nations. By employing a systematic model selection process, we identified key predictors, including education, healthcare initiatives, economic indicators, and disease management, that significantly influence life expectancy. However, considering the complexity of socio-economic factors affecting longevity, augmenting our approach with a more expansive dataset, encompassing a wider array of socio-cultural aspects, could offer a more comprehensive understanding. Additionally, integrating advanced machine learning techniques, such as ensemble methods or deep learning architectures, might provide more nuanced insights into the intricate interplay of factors affecting life expectancy. While our current approach is robust, further exploration involving broader datasets and advanced methodologies could enhance the depth and accuracy of our predictions.

In considering future endeavors, several avenues present themselves for further exploration and refinement. First and foremost, expanding our dataset to incorporate cultural, environmental, and policy-related variables could enrich our understanding of life expectancy determinants. Exploring regional or local-level data to capture nuances within countries could provide more targeted strategies for enhancing life expectancy at a more granular level. Moreover, validating our findings through longitudinal studies or by incorporating real-time data streams could offer dynamic insights into evolving factors influencing life expectancy. Additionally, collaborating with public health organizations or governmental bodies to implement and assess the impact of interventions based on our findings could provide tangible validations and foster the practical application of our research. Continual refinement of our predictive models, validation of assumptions, and addressing potential confounding variables are critical for establishing robust and reliable recommendations for policymakers and global health practitioners.

## References

Lasha., 2023. Life expectancy (WHO) fixed. Kaggle. https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated
