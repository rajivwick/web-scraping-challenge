# Unit 12 Homework: Mission to Mars

In this assignment, you will scrape information from Mars-related websites and analyse it with Pandas. The following information outlines what you need to do.

## Before You Begin

1. Create a new repository for this project called `web-scraping-challenge`. **Do not add this homework to an existing repository**.

2. Clone the new repository to your computer.

3. Inside your local Git repository, create a directory for the web scraping challenge. Use a folder name that corresponds to the challenge: `Mission_to_Mars`.

4. Add your notebook file and CSV to this folder.

5. Push the above changes to GitHub.

## Instructions 

The instructions for this assignment are divided into three parts: 

1. Scrape Mars News

2. Scrape and Analyse Mars Weather Data

3. Submission 

## Part  1: Scrape Mars News

Complete your initial scraping using Jupyter Notebook, Splinter, and BeautifulSoup.

* Create a Jupyter Notebook file called `mars_data_challenge_part_1.ipynb`. Use this file to complete all your scraping and analysis tasks. The following information outlines what you need to scrape.

* Scrape the [Mars News Site](https://redplanetscience.com/) with your automated browser and BeautifulSoup.

* Specifically, scrape the **title** and **preview** of each article. You may wish to use Chrome DevTools to inspect the page to identify which elements to scrape.

* Store the results using Python data structures. Each pair of an article's title and preview should be stored in a Python dictionary, e.g. `{'title': "Mars Rover Begins Mission!", 'preview': "NASA's Mars Rover begins a multi-year mission to collect data about the little-explored planet."}`. Note that each dictionary has two keys: `title` and `preview`. The title and preview text of each article are stored in a dictionary. The dictionaries, in turn, are stored inside a Python list. Print the list in your notebook.

### Optional Activities

It would be a good idea to store the scraped data in a durable file or database. That way, your data does not disappear when you close your notebook.

* Export the scraped data to a JSON file. You may need to research how to do this.

* Export the scraped data to MongoDB. You may need to research how to do this.

## Part 2: Scrape and Analyse Mars Weather Data
- - -

Using your scraping skills, you will extract an HTML table of Mars weather data. You will then use Pandas and Matplotlib to clean, visualise, and analyse the data.

* Create a Jupyter notebook and name it `mars_data_challenge_part_2.ipynb`. Import the relevant dependencies for web scraping. Import Pandas and Matplotlib as well.

* With your automated browser, visit the [Mars weather site](https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html). The URL is `https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html`

* Scrape the data in the HTML table. There are two ways to accomplish this task. The easy way is to use Pandas's `read_html` method. The slightly more challenging way is to scrape the data manually with Splinter and BeautifulSoup. If you choose the latter (you are highly encouraged to do so in order to reinforce your scraping skills), review the following suggestions:

> **Hint** If you scrape the Mars weather site manually, here are some suggestions. First, use DevTools to determine whether the table contains useable classes. Then you can use BeautifulSoup's `find_all` methods to extract all rows in a line of code, for example. Next, you might find and extract the data for each cell in a given row, and store each row's data in a Python list. Using a `for` loop, you might then add each row's data to a list that will contain data from all rows.

* Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here is an explanation of the column headers.

  * id: The identification number of a single transmission from Curiosity.
  * terrestrial_date: The date on Earth.
  * sol: The number of elapsed sols (Martian days) since Curiosity landed on Mars.
  * ls: The solar longitude.
  * month: The Martian month.
  * min_temp: The minimum temperature, in Celsius, of a single Martian day (sol).
  * pressure: The atmospheric pressure in Curiosity's location.

* Examine the data types of all DataFrame columns. If necessary, cast (convert) the data to appropriate `datetime`, `int` or `float` data types. You might use Pandas's `astype` and `to_datetime` methods to accomplish this task.

* Answer the following question: how many months are there on Mars?

* Answer the following question: how many Martian (not Earth) days' worth of data are there in the scraped dataset?

* Answer the following question: what are the coldest and warmest months on Mars (at the location of Curiosity)? Obtain the answer by averaging the minimum daily temperature of each month. Plot the results as a bar plot.

* Answer the following question: which months have the lowest and highest atmospheric pressure on Mars? Obtain the answer by averaging the daily atmospheric pressure of each month. Plot the results as a bar plot.

* Answer the following question: approximately how many terrestrial (earth) days are there in a Martian year? In other words, in the time that Mars circles the Sun once, how many days elapse on the Earth? Estimate the result visually by plotting the daily minimum temperature.

* Export the DataFrame to a CSV file.

## Part 3: Submission

To submit your work to BootCampSpot, create a new GitHub repository and upload the following:

1. The Jupyter notebook containing the code for scraping Mars news.

2. The Jupyter notebook containing the code for scraping and analysing Mars weather data.

3. The exported CSV file.

Ensure your repository has regular commits and a detailed `README.md` file. Then, submit the link to your new repository.

## Rubric

[Unit 12 Homework Rubric](https://docs.google.com/document/d/1H-g23PjJlx5ZsuKcEsOCkEolppWcQ5NMv8hvgbOpl9w/edit)

- - -

© 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.