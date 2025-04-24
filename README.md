# Lab 10 - Python and AI: Surrender your Data to our future AI Helpers

Aashika Uppala, Megan Fister

4/22/2025

## Introduction
The objective of this lab was to use Python and AI tools to develop user-friendly applications that search and visualize data from large water quality databases provided by USGS. Students used the Pandas Python library and a Large Language Model (LLM) to generate functions that cleaned and searched station and results databases. Part 1 involved mapping water quality stations using location data. Part 2 required plotting specific contaminant trends over time across various sites. Part 3 focused on creating an interactive web app using Streamlit that allows users to upload datasets, filter by contaminants, date range, and value, and visualize results dynamically. The final outcome was a fully functional Streamlit web application that dynamically filters and displays water quality station locations and contaminant trends. Python scripts were developed collaboratively with the help of AI tools and deployed via GitHub and Streamlit.

## Methods
### Instruments
• A Computer with internet access

• A Python compiler and IDE like Anaconda Cloud

### Main goal of code:
To develop scripts and an app capable of parsing and visualizing water quality data by site and contaminant trends.

### AI Models Used:

CoPilot, ChatGPT (GPT-4), OpenAI, 2025

## Results

### Prompt 1:
station.csv  Generate a Python function that accesses the database, filters for the names of water quality measurement sites, and displays the location information for all sites without repetition

### Prompt 2:
Generate a Python function that creates a map that pinpoints the location of every station in the database

### Prompt 3:
narrowresult.csv generate a Python function that accesses the database, filters for a desired water quality characteristic (pH), and plots the results. Each site should be represented as a separate line with a different color, where the Y-axis represents the measured values and the X-axis represents time.

### Prompt 4:
Modify the code such that you can ask for two characteristics at the same time

### Prompt 5:
The pH graph looks wrong. Why are the lines going all over the place?

### Prompt 6:
Can you graph it now?

### Prompt 7:
narrowresult.csv 
Generate a Python function that accesses the database, filters for a desired water quality characteristic (DO), and plots the results. Each site should be represented as a separate line with a different color, where the Y-axis represents the measured values and the X-axis represents time

### Prompt 8:
Please modify the code such that you can ask for two characteristics at the same time (temperature and DO)

### Prompt 9:
Please modify the code such that you can ask for two characteristics at the same time

### Prompt 10:
Generate a Python function to develop a Streamlit app that allows the user to upload both databases used in Part 1 and 2, to search for a contaminant in the databases. Once a contaminant has been selected you should be able to define the range of values and dates that you want to show. After modifying the ranges, update the map showing the location of the stations with the contaminant within that range and measured during the time frame. It should also show you a trend over time of the contaminant in all the stations shown.

### Prompt 11:
I want to only get the real values and ignore the string values. I don't want to convert string to point values.

### Prompt 12:
Can you modify the code for the streamlit app to ignore the string values in the ResultMeasureValue column?

### Prompt 13:
I keep getting this error when it tries to plot "TypeError: '<=' not supported between instances of 'str' and 'float'". How can we fix this?

### Prompt 14:
I am now getting this error "KeyError: "['LatitudeMeasure', 'LongitudeMeasure'] not in index"". How can we fix this?

### Prompt 15:
I am now getting this error "ValueError: Location values cannot contain NaNs." How can we fix this? I also need to plot the trends in order by date. Should it be reordered by date?

### Prompt 16:
I am getting this error "ValueError: Location values cannot contain NaNs.
Traceback:
File "/workspaces/Lab10/streamlit_app.py", line 79, in <module>
    main()
File "/workspaces/Lab10/streamlit_app.py", line 47, in main
    site_map = folium.Map(location=map_center, zoom_start=6)
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/home/vscode/.local/lib/python3.11/site-packages/folium/folium.py", line 277, in __init__
    self.location = validate_location(location)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^
File "/home/vscode/.local/lib/python3.11/site-packages/folium/utilities.py", line 108, in validate_location
    raise ValueError("Location values cannot contain NaNs.")" How do I fix this?

### Prompt 17:
I want to sort the database so that the data is in chronological order and characteristics are in alphabetical order. Also, can you plot by day instead of by month?



Link to app: https://lab10maps.streamlit.app/

Note: The link to our app worked originally, but now when you go to the link, the page is empty. You might have to fork the page and allow it to redirect you to GitHub and open the app from the GitHub page. 

## Discussion 
This lab demonstrated the power of combining AI tools with programming to solve real-world data challenges. By leveraging LLM-generated code, we were able to quickly build and debug functions for parsing and visualizing large datasets. We also learned the importance of prompt iteration and specificity when collaborating with AI models. The Streamlit app showcases how code can be converted into a practical tool for scientific communication and public accessibility.

## Conclusion
This lab reinforced practical skills in data analysis using Pandas and introduced web deployment via Streamlit. Key takeaways include:
Effective data cleaning and filtering using Python; Visualizing trends to derive meaningful insights; Learning how to prompt AI to write efficient, modular code;
Creating and deploying real-time applications from codebases; These tools and skills have broad implications for environmental monitoring, research communication, and data-driven policy decisions.
