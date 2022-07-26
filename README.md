# Linkedin Webscrapper and Job Data EDA 

<img src="https://upload.wikimedia.org/wikipedia/commons/0/01/LinkedIn_Logo.svg" width="400">

One of my first EDAs coded with Python, Pandas, Seaborn and Matplotlib in Jupyter Notebooks, it's about analyzing job-ads from Linkedin and made stats about the information regarding places and applicants for different jobs. The EDA uses different visualization techniques and also a georeferential heatmap with the job locations. 

The core of this EDA project is the Linkedin Webscrapper which extracts the content of up to 1000 job ads for your desired job and country.

In this EDA I compared stats of 2 jobs: "data scientist" and the other "full-stack developer". 

You are free to use or modify this scrapper. 

## Getting Started

There are 3 Jupyter Notebook files and one CSV:

- eda_linkedin_v_fin.ipynb
- linkedin_jobs_datascraper.ipynb
- csv_concater.ipynb
- linkedin_datos.csv (Sample data)

## How does it work?

The webscrapper linkedin_jobs_datascraper.ipynb can search and extract up to 1000 jobs for a chosen country and job from linkedin, the output is a CSV file. Please have in mind that Linkedin is very restrictive so the scrapper may cause blocking of your account if you use it too often.
With the Python Script csv_concater.ipynb you can concat the different files in order to use in the eda_linkedin_v_fin.ipynb file.

### Prerequisites

Requirements for using the Jupyter Notebook,the visualizations and the webscrapper:
- Python, Pandas, Numpy, Jupyter Notebook
- Matplotlib, Seaborn, Squarify, Folium, Geocoder, ipywidgets, geopy
- Selenium and Beautifulsoup

### Installing Webscrapper
Install all the missing libraries via pip install
for example:

    pip install beautifulsoup

When you have opened the linkedin_jobs_datascraper.ipynb  please look for
the part User Login Information, there you need to your linkedin username in user_data and your password in password.

    user_data = "username@usermail.com"
    password = "yourpassword"

In the next lines you need to change the search parameters.
In "searchterm_org" you need to put the Jobtitle and in "searchlocation" any of the countries which are in the list "geoid". You can add more countries ther but you will need to find out the Linkedin country code.

When you have done the steps and run the file you will get a CSV with the name made of the job-title and the country name. You can make multiple files and the use the CSV concater, csv_concater.ipynb.

The csv_concater.ipynb, concats all the CSV in the same folder.

### Installing EDA

Install all the missing libraries via pip install
for example:

    pip install geocoder

or for example

    pip install folium

Open the  eda_linkedin_v_fin.ipynb file, then check the file path of the CSV file

    linkedin_datos.csv


## Running all the cells

Please run all the cells of the Jupyter Notebook eda_linkedin_v_fin.ipynb file, especially all which are used for the data cleaning step by step.

At the end you should be able to see a heatmap of the job distribution geo referntial located in the region.

## Deployment

When you use the Jupyter notebooks please take care about the paths and that the folder is writeable.

## Built With

  - [Folium](https://github.com/python-visualization/folium) - Used for the map
  - [Geopy](https://geopy.readthedocs.io/en/stable/) - Used for geoencoding


## Authors

  - **Christian Jerome Bader** - [Github Profile](https://github.com/jeromebader)

## License

This project is licensed under the CC0 4.0 Universal.

