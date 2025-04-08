# Netflix-Data-Anaysis
Exploratory Data Analysis &amp; Visualizion of Netflix

![logo](https://github.com/saurav190101/Netflix-Data-Anaysis/blob/main/photo-1574375927938-d5a98e8ffe85.avif)


# 📺 Netflix Data Analysis Project

**Tools Used:** Python, pandas, matplotlib, seaborn, plotly express

## 📊 Overview

In this project, I analyzed Netflix data to extract key insights using Python. The analysis covers:

- Most-watched genres
  
  ```
genre_typemovies=df.loc[df['type']=='Movie']
count_genre = genre_typemovies['genre'].str.split(', ').explode()  #convert into  list and after explode(in each row)each row
count_genre=count_genre.value_counts().reset_index()

count_genre=pd.DataFrame(count_genre)

plt.figure(figsize=(16,8))
sns.barplot(y='genre', x='count', data=count_genre, palette='viridis')
plt.xticks(rotation=90)
plt.tight_layout()
plt.title('Top Genre Movies',fontsize=14)

plt.show()   
``` 
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
- Movies dominate Netflix's content library
- India and USA are top countries producing Netflix content


## 📁 Dataset

Source: [Netflix Dataset on Kaggle](https://www.kaggle.com/code/shivamb/netflix-shows-and-movies-exploratory-analysis/input)
