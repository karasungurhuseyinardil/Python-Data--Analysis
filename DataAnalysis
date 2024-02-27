import pandas as pd
import numpy as np

# Read chip orders data
orders = pd.read_table("http://bit.ly/chiporders")
orders.head()

# Read movie users data
users = pd.read_table("http://bit.ly/movieusers", sep="|", header=None)
users.columns = ["ID", "Age", "Gender", "Occupation", "Zip"]
users.head()

# Display data types of users dataframe
users.dtypes

# Display shape of users dataframe
users.shape

# Display summary statistics for users dataframe
users.describe()

# Display summary statistics for object data types in users dataframe
users.describe(include="object")

# Read IMDb ratings data for movies
movies = pd.read_csv("http://bit.ly/imdbratings")
movies.head()

# Display shape of movies dataframe
movies.shape

# Sort movies by duration in descending order
movies["duration"].sort_values(ascending=False)

# Sort movies by duration in descending order and display the top 10
movies.sort_values("duration", ascending=False)[:10]

# Find movies with duration greater than 200 minutes and calculate their average star rating
long_movies = movies[movies["duration"] > 200]
long_movies["star_rating"].mean()

# Calculate the overall average star rating for all movies
movies["star_rating"].mean()

# Find movies with duration greater than 180 minutes and genre equal to Drama
movies[(movies["duration"] > 180) & (movies["genre"] == "Drama")]

# Display the first few rows of the orders dataframe
orders.head()

# Calculate the average price for all items in orders
orders["item_price"].str.slice(1).astype(float).mean()

# Calculate the average price for items containing "Chicken" in their name
chicken_data = orders[orders["item_name"].str.contains("Chicken")]
chicken_data["item_price"].str.slice(1).astype(float).mean()

# Read drinks by country data
drinks = pd.read_csv("http://bit.ly/drinksbycountry")
drinks.head()

# Display the top 5 countries with the highest beer servings
drinks.sort_values("beer_servings", ascending=False)[:5]

# Display the first few rows of the drinks dataframe
drinks.head()

# Calculate the average alcohol consumption by continent
drinks.groupby("continent").mean()

# Display the average beer servings by continent
drinks.groupby("continent").mean()["beer_servings"]

# Plot a bar chart of average beer servings by continent
drinks.groupby("continent").mean()["beer_servings"].plot(kind="bar")

# Plot a bar chart of average alcohol consumption by continent
drinks.groupby("continent").mean().plot(kind="bar")

# Create a datetime object for January 3, 2001
burak = pd.to_datetime("01/03/2001", dayfirst=True)
burak

# Extract day, month, year, day name, and month name from the datetime object
burak.day
burak.month
burak.year
burak.day_name()
burak.month_name()

# Read UFO reports data
ufos = pd.read_csv("http://bit.ly/uforeports")
ufos.head()

# Display the shape of the UFO reports dataframe
ufos.shape

# Display data types of columns in the UFO reports dataframe
ufos.dtypes

# Convert the "Time" column to datetime format
ufos["Time"] = pd.to_datetime(ufos["Time"])
ufos.dtypes

# Plot a line chart of the number of UFO reports over the years
ufos["Time"].dt.year.value_counts().sort_index().plot()

# Plot a bar chart of the number of UFO reports by month
ufos["Time"].dt.month.value_counts().sort_index().plot(kind="bar")

# Plot a bar chart of the number of UFO reports by day of the week
ufos["Time"].dt.day_name().value_counts().sort_index().plot(kind="bar")

# Plot a bar chart of the number of UFO reports by day of the month
ufos["Time"].dt.day.value_counts().sort_index().plot(kind="bar")

# Read historical Bitcoin to INR exchange rate data
data = pd.read_csv("/content/BTC_INR_Historical Data.csv")
data.head()
