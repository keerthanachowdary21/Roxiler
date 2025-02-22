# MERN Stack Coding Challenge

This repository contains the implementation of a MERN (MongoDB, Express.js, React.js, Node.js) stack application that fulfills the requirements of the coding challenge. The application fetches data from a third-party API, processes it, and provides various APIs to interact with the data. The frontend displays the data in a table and visualizes it using charts.


# Screenshots

### Default month selected
![Screenshot 2023-11-14 204454](https://github.com/iompawar/roxiler-mern-coding-challenge/assets/88156970/098a15ac-3ee5-4a8f-8bd6-c69bbe3eac0c)

### Nov selected
![Screenshot 2023-11-14 204826](https://github.com/iompawar/roxiler-mern-coding-challenge/assets/88156970/f07b4574-a463-46e9-86cf-13d16e7b4df4)

### Searching transaction 
![Screenshot 2023-11-14 205025](https://github.com/iompawar/roxiler-mern-coding-challenge/assets/88156970/89be55d5-33cd-4d1d-a2cd-daf80d514c69)

### Searching transactions based on price
![Screenshot 2023-11-14 205139](https://github.com/iompawar/roxiler-mern-coding-challenge/assets/88156970/076a864e-008e-4fb1-a97a-8bdba74534ad)

### Statistics of default month
![Screenshot 2023-11-14 205238](https://github.com/iompawar/roxiler-mern-coding-challenge/assets/88156970/e5f64dd7-a950-4c40-99d7-95b9d12a655e)

### Statistics of Sep
![Screenshot 2023-11-14 205608](https://github.com/iompawar/roxiler-mern-coding-challenge/assets/88156970/a9802003-8757-43f3-af00-26d4c218e079)

### Pie Chart of default month
![Screenshot 2023-11-14 205736](https://github.com/iompawar/roxiler-mern-coding-challenge/assets/88156970/10877fd0-21e6-45c1-b9d6-5ae06465a193)

### Pie Chart of Sep
![Screenshot 2023-11-14 205838](https://github.com/iompawar/roxiler-mern-coding-challenge/assets/88156970/4a046e87-e52a-4e25-80fc-2951163b86d7)

### Bar Chart of default month
![Screenshot 2023-11-14 205959](https://github.com/iompawar/roxiler-mern-coding-challenge/assets/88156970/b8cdf9bd-988b-402d-99d2-9e67947d8929)

### Bar chart of Jun
![Screenshot 2023-11-14 210121](https://github.com/iompawar/roxiler-mern-coding-challenge/assets/88156970/0615630b-5abd-4edf-9513-29df467f5c15)

## Backend Task

### Data Source
- **Third Party API URL**: [https://s3.amazonaws.com/roxiler.com/product_transaction.json](https://s3.amazonaws.com/roxiler.com/product_transaction.json)
- **Request Method**: GET
- **Response Format**: JSON

### APIs

1. **Initialize Database**
   - **Endpoint**: `GET /api/initialize-database`
   - **Description**: Fetches data from the third-party API and initializes the database with seed data.
   - **Response**: Success message with the number of records inserted.

2. **List Transactions**
   - **Endpoint**: `GET /api/transactions`
   - **Query Parameters**:
     - `month`: Month to filter transactions (e.g., "January", "February", etc.).
     - `search`: Search text to match against product title, description, or price.
     - `page`: Page number for pagination (default: 1).
     - `perPage`: Number of items per page (default: 10).
   - **Description**: Returns a paginated list of transactions filtered by month and search text.
   - **Response**: List of transactions with pagination details.

3. **Statistics**
   - **Endpoint**: `GET /api/statistics`
   - **Query Parameters**:
     - `month`: Month to filter statistics (e.g., "January", "February", etc.).
   - **Description**: Returns total sale amount, total sold items, and total not sold items for the selected month.
   - **Response**: JSON object with statistics.

4. **Bar Chart Data**
   - **Endpoint**: `GET /api/bar-chart`
   - **Query Parameters**:
     - `month`: Month to filter bar chart data (e.g., "January", "February", etc.).
   - **Description**: Returns the number of items in different price ranges for the selected month.
   - **Response**: JSON object with price ranges and item counts.

5. **Pie Chart Data**
   - **Endpoint**: `GET /api/pie-chart`
   - **Query Parameters**:
     - `month`: Month to filter pie chart data (e.g., "January", "February", etc.).
   - **Description**: Returns the number of items in each category for the selected month.
   - **Response**: JSON object with categories and item counts.

6. **Combined Data**
   - **Endpoint**: `GET /api/combined-data`
   - **Query Parameters**:
     - `month`: Month to filter combined data (e.g., "January", "February", etc.).
   - **Description**: Combines the responses from the statistics, bar chart, and pie chart APIs.
   - **Response**: JSON object with combined data.

## Frontend Task

### Features

1. **Transactions Table**
   - Displays a list of transactions for the selected month.
   - Includes a dropdown to select the month (default: March).
   - Supports search functionality to filter transactions by title, description, or price.
   - Implements pagination with "Next" and "Previous" buttons.

2. **Transactions Statistics**
   - Displays the total sale amount, total sold items, and total not sold items for the selected month.

3. **Transactions Bar Chart**
   - Visualizes the number of items in different price ranges for the selected month.

4. **Transactions Pie Chart**
   - Visualizes the number of items in each category for the selected month.

### Mockups

The frontend follows the provided mockups but allows for custom design changes to improve the look and feel.

## Getting Started

### Prerequisites

- Node.js
- MongoDB
- React.js








