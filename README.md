# Infosys-Stock-Price-Prediction
Stock price prediction of Infosys Limited by analysing historical data using AWS services.

This repository contains the necessary code and resources to predict Infosys Company's stock prices. The prediction is achieved by utilizing Amazon S3 Bucket for data storage, Amazon SageMaker for building, deploying the predictive model and is visualised using Amazon Quicksight.

⚠️ Important Disclaimer: Please Read Before Proceeding ⚠️

The stock price prediction results presented in this project are for educational and illustrative purposes only. They are based on historical data and machine learning algorithms, which may not accurately reflect future market behavior. The financial markets are complex and subject to various unpredictable factors that can impact stock prices. This project's predictions should not be used for making actual stock picking or investment decisions. It's crucial to consult with financial professionals and conduct thorough research before making any investment choices. Remember that all investments carry risks, and past performance is not indicative of future results.

Introduction

Stock price prediction is a common problem in financial analysis. In this project, I aim to predict the stock prices of Infosys Company using historical stock price data. 

Three essential components of stock data are:
* Volume: The total number of shares traded during a given period.
* Opening Price: The price at which a stock starts trading when the market opens.
* Closing Price: The price at which a stock ends trading when the market closes.

I will be using historical stock price data covering the period from January 2, 1996 to August 14, 2023, (BSE Data).

Data Collection: You can download the historical stock price data as a CSV file from your preferred company's website/ official websites of the stock exchanges or can use the provided CSV file in this repository➡️(https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/blob/main/INFOSYS%20STOCK%20(HISTORICAL%20PRICES).csv).
Certainly, I'll provide you with a detailed step-by-step guide based on your instructions for setting up Amazon SageMaker, creating a model for stock price prediction, and obtaining the predicted output. 

### Step-by-Step Guide: Stock Price Prediction Using Amazon SageMaker

1. **Accessing Amazon SageMaker Console**
   - Go to the [Amazon SageMaker Console](https://console.aws.amazon.com/sagemaker/).
   - Click on "Get started" to initiate the process.

2. **Setting Up SageMaker Domain**
   - On the SageMaker Dashboard, click on "Set up SageMaker Studio Domain."
   - Choose a unique domain name and click "Next."
     
   <img width="917" alt="user profile, 1" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/dcc9e66f-b129-4366-bf8c-576a516bb199">

3. **Creating Execution Role**
   - Under "Execution Role," click "Create a new role."
   - Select "Any S3 bucket" and click "Create role."
   - Leave other settings as default and click "Submit."
   
<img width="718" alt="role" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/55e4893b-b1c2-440a-848d-e69511486550">

4. **Domain Status Check**
   - Wait for the domain status to change to "InService."
   - Once it's in "InService," click on the name of the domain.
     
<img width="956" alt="domain 3" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/db7869ea-4800-407c-9c26-c2651a098f1d">

5. **Launching SageMaker Studio**
   - Click the "Launch Studio" button.
   - Wait for a while (it took around 7 minutes for me) until the canvas icon appears.

6. **Accessing Canvas Dashboard**
   - Click the canvas icon to access the Canvas dashboard.

7. **Importing CSV File**
   - In the Canvas dashboard, head to the "Datasets" item bar.
   - Import the CSV file containing historical stock price data.
     
<img width="959" alt="infy 4" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/76bd772a-b681-43c1-9a91-8921660bb4f6">

8. **Creating a Model**
   - Go to "My Models" and click on "Create model."
   - Provide a name for your model and click "Create."

9. **Selecting Dataset**
   - Choose the imported dataset for the model and click the "Select dataset" icon.
     
<img width="955" alt="S3 5" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/b184ee67-4e10-48f1-80af-edb597103322">

10. **Selecting Prediction Target**

<img width="959" alt="MODEL 7" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/00cdd7e8-557b-47c6-b9ed-fd495c795173">

   - In the "Select column" section, choose "MarketClose" (as that's the value we want to predict).

<img width="960" alt="stock pricee 9" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/b50ff499-4301-4327-b095-201298ebf0fa">

11. **Configuring Time Series Model**
   - Hover your cursor over the "Model Type" section and select "Configure time series model."

12. **Setting Model Parameters**
   - Configure the time series model as per your requirements.
   - Follow the instructions and select appropriate options.
<img width="493" alt="time series 10" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/d60b11cc-2a9e-421e-b2b6-068f5b1c3972">


13. **Initiating Model Building**
   - Click on "Quick build" to initiate the model building process.
     
<img width="950" alt="preview of data 11" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/46d79408-ba35-4ce1-9d22-617d2f847ac6">

   - Now, wait patiently as the model is being built (this can take around 14-20 minutes).
     
<img width="960" alt="analysis 12" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/02bff168-6580-4269-9e00-149cf1182cb5">

14. **Predicting Using the Model**
   - Once the model building is complete, select "Predict" to generate predictions.
     
https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/533c25a1-1314-4524-a927-99b78bc9cdd0

   - You will be presented with the output data based on the model's predictions.

![single_prediction_results](https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/104a96df-2af7-4fcf-a20d-8083eb7ff6b2)



Remember that these steps provide a general guideline based on your description. The exact options and buttons might vary slightly depending on updates and changes to the Amazon SageMaker interface. Additionally, the accuracy of your predictions will depend on the quality of the model, the features you've selected, and the nature of the stock market data.
Certainly, here's a detailed step-by-step guide for uploading the CSV file and JSON file to an S3 bucket and then using Amazon QuickSight to visualize the data:

### Step-by-Step Guide: Uploading Data to S3 and Visualizing with Amazon QuickSight

1. **Uploading Files to S3 Bucket**

   - Go to the [Amazon S3 Console](https://s3.console.aws.amazon.com/s3/).
   - Click on "Create bucket" to create a new bucket or select an existing one.
   
2. **Uploading CSV File**

   - Click on the created bucket.
   - Click on the "Upload" button.
   - Select your downloaded CSV file (https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/blob/main/prediction_results.csv) and click "Next."
   - Keep default settings and click "Next."
   - Review and click "Upload."

3. **Uploading JSON File**

   - Similarly, upload the JSON File  (https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/blob/main/manifest-file%2C%20(quicksight).json) you have to the same bucket using the "Upload" button (type the name of your bucket instead of 'your-bucket-name' in the JSON File)
   - Follow the same process as with the CSV file.
     
<img width="959" alt="s3 bucket" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/a22a8275-6b34-43ef-8754-2d8fa24c4d94">


4. **Creating an Amazon QuickSight Dataset**

   - Go to the [Amazon QuickSight Console](https://quicksight.aws.amazon.com/).
   - Click "Datasets" on the left-hand menu.
   - Click "New dataset" and choose "S3."

<img width="947" alt="2" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/606a2bc4-0852-49d8-8a38-74723767f2c3">

   - Choose your S3 bucket.
   - Select the uploaded CSV file and click "Connect."

<img width="954" alt="3" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/1a2935f2-792b-4646-94c8-9e38fd0348d6">
   

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

<img width="960" alt="4" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/a2ef0acc-9602-446d-ac7f-e097275a7fc8">

<img width="440" alt="5" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/174a67bf-9832-4fc0-80a6-07db7c141aa7">

   - Drag and drop columns onto the visual's fields.
   - Adjust settings, labels, and formatting as needed.
     
<img width="959" alt="7" src="https://github.com/Meldindavidsabu/Infosys-Stock-Price-Prediction/assets/80899101/4447e89e-9892-496e-845a-2da8860d129b">

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
