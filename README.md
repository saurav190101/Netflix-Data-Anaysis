# Netflix-Data-Anaysis
Exploratory Data Analysis &amp; Visualizion of Netflix

![logo](https://github.com/saurav190101/Netflix-Data-Anaysis/blob/main/photo-1574375927938-d5a98e8ffe85.avif)


# 📺 Netflix Data Analysis Project

**Tools Used:** Python, pandas, matplotlib, seaborn, plotly express

## 📊 Overview

In this project, I analyzed Netflix data to extract key insights using Python. The analysis covers:

- Most-watched genres
- Year-wise content production
- Trends in TV Shows vs Movies
- Duration patterns
- Country-wise content


## 🔍 Key Libraries Used

- pandas for data manipulation
- matplotlib and seaborn for static plots
- plotly express for interactive visualizations

## 📌 Sample Insights

- Content peaked around 2018–2020
```
movie_count=df['release_year'].value_counts().reset_index()
most_movie_releaseyear=movie_count.sort_values(by='release_year',ascending=False)
most_movie_releaseyear
px.line(most_movie_releaseyear,x='release_year',y='count',markers=True ,title=' Most Movie Release By Year')
```

- India and USA are top countries producing Netflix content
```
filter_data=df['country'].value_counts().reset_index()
filter_data['country']=filter_data['country'].replace('unknown','others')
filter_data=filter_data.sort_values(by='count',ascending=False).head(5)
filter_data
px.pie(filter_data,names='country',values='count' ,title='Top movies and series by countries')
```

## 📁 Dataset

Source: [Netflix Dataset on Kaggle](https://www.kaggle.com/code/shivamb/netflix-shows-and-movies-exploratory-analysis/input)
