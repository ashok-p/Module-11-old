# Module-11-Challenge - Forecasting Net Prophet
With over 200 million users, MercadoLibre is the most popular e-commerce site in Latin America. The company wants to leverage their search data into projecting sales forecasts, understanding consumer behavior etc. Facebook Prophet was chosen to be used for this activity as it provides excellent mechanisms to do such analysis.

The Starter Code was provided along with the historical search, sales and stock data of MercadoLibre.

---

## User Story
MercadoLibre is the most popular e-commerce site in Latin America. As a growth analyst at MercadoLibre you've been tasked with analyzing the company's financial and user data in clever ways to make the company grow. Specifically:

* The data science manager asks if the Google search traffic for the company links to any financial events at the company.  
* Marketing wants to mine the hourly search data so that they can target their campaigns more effectively and improve their departmental ROI.  
* Finance wants to know if any relationship between the search data and the company stock price exists.  
* The management wants to know the near-term forecast for the popularity of MercadoLibre and the associated search patterns.  
* Understanding the capabilities of the Data Science group, Finance wants assistance in forecasting sales projections for their upcoming quarter. 

---

## Acceptance Criteria  
The application must meet the following acceptance criteria:  

* Find unusual patterns in the Google search data to link them to corporate events, if possible 
* Mine the search traffic data for seasonality  
* Relate the search traffic to stock price patterns  
* Create a time series model with Prophet that analyzes and forecasts patterns in the hourly search data    
* Forecast revenue by using time series models  
  
---

## The Application  

The application follows these stages: 
    
### Find Unusual Patterns in Hourly Google Search Traffic      
* Read the search data into a DataFrame, and then slice the data to just the month of May 2020. (During this month, MercadoLibre released its quarterly financial results.) Use hvPlot to visualize the results.

* Calculate the total search traffic for the month, and then compare the value to the monthly median across all months. 
 

### Mine the Search Traffic Data for Seasonality 
* Group the hourly search data to plot the average traffic by the day of the week (for example, Monday vs. Friday).  

* Using hvPlot, visualize this traffic as a heatmap, referencing the `index.hour` as the x-axis and the `index.dayofweek` as the y-axis. 

* Group the search data by the week of the year.

### Relate the Search Traffic to Stock Price Patterns
* Read in and plot the stock price data. Concatenate the stock price data to the search data in a single DataFrame.

* Slice the data to just the first half of 2020 (`2020-01` to `2020-06` in the DataFrame), and then use hvPlot to plot the data to answer whether MercadoLibre performance agreed with the narrative - "Market events emerged during the year of 2020 that many companies found difficult. But, after the initial shock to global financial markets, new customers and revenue increased for e-commerce platforms."

* Create a new column in the DataFrame named “Lagged Search Trends” that offsets, or shifts, the search traffic by one hour. Create two additional columns for 1) “Stock Volatility”, which holds an exponentially weighted four-hour rolling average of the company’s stock volatility, and 2) “Hourly Stock Return”, which holds the percent change of the company's stock price on an hourly basis.  Then, review the time series correlation, to analyze relationship between the lagged search traffic and the stock volatility, and between the lagged search traffic and the stock price returns. 

### Create a Time Series Model with Prophet to analyze and forecast search patterns     
* Set up the Google search data for a Prophet forecasting model.

* After estimating the model, plot the forecast to answer the near-term forecast for the popularity of MercadoLibre.

* Plot the individual time series components of the model to answer the following questions:

    * What time of day exhibits the greatest popularity?

    * Which day of the week gets the most search traffic?

    * What's the lowest point for search traffic in the calendar year?


### Forecast Revenue by Using Time Series Models
* Read in the daily historical sales figures, and then apply a Prophet model to the data.

* Interpret the model output to identify any seasonal patterns in the company's revenues.  

* Produce a sales forecast for the the next quarter with the following 3 scenerios: 
    * projected total sales revenues 
    * projected upper limit for sales revenues, and
    * projected lower limit for sales revenues.
 
---

## Technologies
The application is developed using:  
* Language: Python 3.7,   
* Packages/Libraries: Pandas, holoviews, hvplot.pandas, matplotlib, numpy; fbprophet (Facebook Prophet)
* Development Environment: VS Code and Terminal, Google Colab
* OS: Mac OS 12.1

---
## Installation Guide
Following are the instructions to install the application from its Github respository.  

### Clone the application code from Github as follows:
copy the URL link of the application from its Github repository      
open the Terminal window and clone as follows:  

   1. %cd to_your_preferred_directory_where_you want_to_store_this_application  
    
   2. %git clone URL_link_that_was_copied_in_step_1_above   
    
   3. %ls     
        Module-11-Challenge    
        
   4. %cd Module-11-Challenge     

At this point you will have the the entire application files in the current directory as follows:

    * README.md                       (this file that you are reading)  
    * forecasting_net_prophet.ipynb         (the application jupter lab notebook)  
    * Resources                      (Folder with the data required) 
        - google_hourly_search_trends.csv  
        - mercado_daily_revenue.csv     
        - mercado_stock_price.csv  

---

## Usage
The following details the instructions on how to run the application.  

### Setup Google Colab to run the application


   5. click on [Google Colab](https://colab.research.google.com/) - an IDE that allows you to run Jupyter Notebooks in the cloud. You can also copy and paste the link https://colab.research.google.com/ in your web browser as an alternative. 
    
   6. click on **upload** 
    
   7. click on **Choose File** to select the notebook **forecasting_net_prophet.ipynb** from the folder in Step 4 above 

---

### Run the Application 

After the notebook **forecasting_net_prophet.ipynb** has loaded, click on **Runtime** tab and select **run all**  

After uploading all the required libraries, the notebook will be waiting for you to input all the Resource file names.   
From the Resources folder in Step 4 above select all the **csv** files and press enter 


---

## Contributors
Ashok Pandey - ashok.pragati@gmail.com   
www.linkedin.com/in/ashok-pandey-a7201237

---

## License
The source code is the property of the developer. The users can copy and use the code freely but the developer is not responsible for any liability arising out of the code and its derivatives.

---