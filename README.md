# Infosys-Stock-Price-Prediction
Stock price prediction of Infosys Limited by analysing historical data using AWS services.

This repository contains the necessary code and resources to predict Infosys Company's stock prices. The prediction is achieved by utilizing Amazon S3 Bucket for data storage, Amazon SageMaker for building and deploying the predictive model and is visualised using Amazon Quicksight.

⚠️ Important Disclaimer: Please Read Before Proceeding ⚠️

The stock price prediction results presented in this project are for educational and illustrative purposes only. They are based on historical data and machine learning algorithms, which may not accurately reflect future market behavior. The financial markets are complex and subject to various unpredictable factors that can impact stock prices. This project's predictions should not be used for making actual stock picking or investment decisions. It's crucial to consult with financial professionals and conduct thorough research before making any investment choices. Remember that all investments carry risks, and past performance is not indicative of future results.

Introduction
Stock price prediction is a common problem in financial analysis. In this project, i aim to predict the stock prices of Infosys Company using historical stock price data. Three essential components of stock data are:
* Volume: The total number of shares traded during a given period.
* Opening Price: The price at which a stock starts trading when the market opens.
* Closing Price: The price at which a stock ends trading when the market closes.

I will be using historical stock price data covering the period from January 2, 1996 to August 14, 2023, (BSE Data).

Data Collection: You can download the historical stock price data as a CSV file from your preferred company's website/ official websites of the stock exchanges or can use the provided CSV file in the repository➡️(https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/blob/main/INFOSYS%20STOCK%20(HISTORICAL%20PRICES).csv).
Certainly, I'll provide you with a detailed step-by-step guide based on your instructions for setting up Amazon SageMaker, creating a model for stock price prediction, and obtaining the predicted output. 

### Step-by-Step Guide: Stock Price Prediction Using Amazon SageMaker

1. **Accessing Amazon SageMaker Console**
   - Go to the [Amazon SageMaker Console](https://console.aws.amazon.com/sagemaker/).
   - Click on "Get started" to initiate the process.

2. **Setting Up SageMaker Domain**
   - On the SageMaker Dashboard, click on "Set up SageMaker Studio Domain."
   - Choose a unique domain name and click "Next."

3. **Creating Execution Role**
   - Under "Execution Role," click "Create a new role."
   - Select "Any S3 bucket" and click "Create role."
   - Leave other settings as default and click "Submit."

4. **Domain Status Check**
   - Wait for the domain status to change to "InService."
   - Once it's in "InService," click on the name of the domain.

5. **Launching SageMaker Studio**
   - Click the "Launch Studio" button.
   - Wait for a while (it took around 7 minutes for me) until the canvas icon appears.

6. **Accessing Canvas Dashboard**
   - Click the canvas icon to access the Canvas dashboard.

7. **Importing CSV File**
   - In the Canvas dashboard, head to the "Datasets" item bar.
   - Import the CSV file containing historical stock price data.

8. **Creating a Model**
   - Go to "My Models" and click on "Create model."
   - Provide a name for your model and click "Create."

9. **Selecting Dataset**
   - Choose the imported dataset for the model and click the "Select dataset" icon.

10. **Selecting Prediction Target**
   - In the "Select column" section, choose "MarketClose" (as that's the value we want to predict).

11. **Configuring Time Series Model**
   - Hover your cursor over the "Model Type" section and select "Configure time series model."

12. **Setting Model Parameters**
   - Configure the time series model as per your requirements.
   - Follow the instructions and select appropriate options.

13. **Initiating Model Building**
   - Click on "Quick build" to initiate the model building process.
   - Now, wait patiently as the model is being built (this can take around 14-20 minutes).

14. **Predicting Using the Model**
   - Once the model building is complete, select "Predict" to generate predictions.
   - You will be presented with the output data based on the model's predictions.

Remember that these steps provide a general guideline based on your description. The exact options and buttons might vary slightly depending on updates and changes to the Amazon SageMaker interface. Additionally, the accuracy of your predictions will depend on the quality of the model, the features you've selected, and the nature of the stock market data.
Certainly, here's a detailed step-by-step guide for uploading the CSV file and JSON file to an S3 bucket and then using Amazon QuickSight to visualize the data:

### Step-by-Step Guide: Uploading Data to S3 and Visualizing with Amazon QuickSight

1. **Uploading Files to S3 Bucket**

   - Go to the [Amazon S3 Console](https://s3.console.aws.amazon.com/s3/).
   - Click on "Create bucket" to create a new bucket or select an existing one.

2. **Uploading CSV File**

   - Click on the created bucket.
   - Click on the "Upload" button.
   - Select your downloaded CSV file (https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/blob/main/prediction_results.csv`) and click "Next."
   - Keep default settings and click "Next."
   - Review and click "Upload."

3. **Uploading JSON File**

   - Similarly, upload the (https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/blob/main/manifest-file%2C%20(quicksight).json) you have to the same bucket using the "Upload" button.
   - Follow the same process as with the CSV file.

4. **Creating an Amazon QuickSight Dataset**

   - Go to the [Amazon QuickSight Console](https://quicksight.aws.amazon.com/).
   - Click "Datasets" on the left-hand menu.
   - Click "New dataset" and choose "S3."
   - Choose your S3 bucket.
   - Select the uploaded CSV file and click "Connect."

5. **Data Preparation in QuickSight**

   - QuickSight might detect column types, but you can adjust them if needed.
   - Follow the steps to preview and save the dataset.

6. **Creating Visualizations**

   - Click "Analysis" on the left-hand menu.
   - Click "New analysis."
   - Select the dataset you created.

7. **Creating Visualizations Using QuickSight**

   - Click "Add" to add a visual.
   - Choose the visualization type you want (e.g., line chart, bar chart, etc.).
   - Drag and drop columns onto the visual's fields.
   - Adjust settings, labels, and formatting as needed.

8. **Adding Insights (Optional)**

   - Use "Insights" to automatically generate visualizations based on your data.
   - Click "Insights" on the left-hand menu.
   - Choose "Create a new insight" and follow the steps.

9. **Creating a Dashboard**

   - After creating visuals and insights, you can create a dashboard to combine them.
   - Click "Add" and choose "Dashboard."
   - Add visuals and insights to the dashboard canvas.
   - Arrange and resize them as desired.

10. **Publishing and Sharing**

   - Once your dashboard is ready, click "Share" in the top-right corner.
   - Choose options for sharing with others.

Remember that Amazon QuickSight offers various customization and visualization options. The steps provided here give you a basic guide, but you can explore more features in QuickSight to fine-tune your visualizations and insights.
