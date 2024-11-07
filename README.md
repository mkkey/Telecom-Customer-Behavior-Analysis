# Megaline Customer Behavior Analysis

## Introduction

This project is a comprehensive statistical data analysis of Megaline's customer behavior. Megaline, a telecom operator, offers two prepaid plans: **Surf** and **Ultimate**. The goal of this project is to analyze which plan brings in more revenue to help the company adjust its advertising budget accordingly.

The analysis focuses on examining customer usage patterns, identifying statistical trends in calls, texts, and data usage, and evaluating key factors affecting revenue generation for both plans. By employing various statistical techniques, the project aims to uncover significant differences in plan usage and revenue, ultimately aiding Megaline in making informed business decisions.

## Features

The project includes the following components:

1. **Data Preprocessing**:
   - Loading and inspecting datasets related to calls, messages, internet usage, plans, and user information.
   - Cleaning data by handling missing values, converting data types, and enriching data with additional calculations.

2. **User Behavior Analysis**:
   - Analyzing customer behavior in terms of call durations, number of messages sent, and internet data usage.
   - Comparing usage patterns between the Surf and Ultimate plans.
   - Visualizing distributions and trends using histograms, bar plots, and box plots.

3. **Revenue Calculation**:
   - Calculating monthly revenue for each user by considering the monthly fees and additional charges for exceeding plan limits.
   - Determining which plan generates more revenue on both per-user and overall bases.

4. **Statistical Hypothesis Testing**:
   - Testing hypotheses to determine if there are significant differences in average revenue between:
     - Users of the Surf and Ultimate plans.
     - Users from the NY-NJ area and users from other regions.
   - Utilizing t-tests to assess statistical significance.

5. **Visualization**:
   - Creating insightful plots to illustrate user behavior and revenue patterns.
   - Visualizations include histograms, scatter plots, bar charts, and box plots.

## Technologies Used

- **Python**: Core programming language for analysis.
- **Pandas**: Data manipulation and analysis.
- **NumPy**: Numerical computations.
- **Matplotlib**: Data visualization.
- **SciPy**: Statistical hypothesis testing.
- **Jupyter Notebook**: Interactive environment for writing and running code.

## Dataset

The project uses five datasets stored in CSV files within the `data/` directory:

1. **Calls Data (`megaline_calls.csv`)**:
   - `id`: Unique call identifier.
   - `call_date`: Date of the call (YYYY-MM-DD).
   - `duration`: Call duration in minutes (float).
   - `user_id`: Unique user identifier.

2. **Messages Data (`megaline_messages.csv`)**:
   - `id`: Unique message identifier.
   - `message_date`: Date the message was sent (YYYY-MM-DD).
   - `user_id`: Unique user identifier.

3. **Internet Data (`megaline_internet.csv`)**:
   - `id`: Unique session identifier.
   - `mb_used`: Data used during the session in megabytes (float).
   - `session_date`: Date of the internet session (YYYY-MM-DD).
   - `user_id`: Unique user identifier.

4. **Plans Data (`megaline_plans.csv`)**:
   - `plan_name`: Name of the calling plan.
   - `usd_monthly_pay`: Monthly charge in US dollars.
   - `minutes_included`: Monthly minute allowance.
   - `messages_included`: Monthly text allowance.
   - `mb_per_month_included`: Data volume allowance in megabytes.
   - `usd_per_minute`: Price per minute after exceeding the package limits.
   - `usd_per_message`: Price per text after exceeding the package limits.
   - `usd_per_gb`: Price per extra gigabyte of data after exceeding the package limits (1 GB = 1024 MB).

5. **Users Data (`megaline_users.csv`)**:
   - `user_id`: Unique user identifier.
   - `first_name`: User's first name.
   - `last_name`: User's last name.
   - `age`: User's age (years).
   - `city`: User's city of residence.
   - `reg_date`: Subscription date (YYYY-MM-DD).
   - `churn_date`: Date the user stopped using the service (if applicable).
   - `plan`: Name of the calling plan.

## Usage

The project is structured to guide you through the analysis process:

1. **Data Preparation**:
   - Load datasets into pandas DataFrames.
   - Inspect data for missing values and data types.
   - Convert date columns to datetime objects.
   - Enrich data by calculating additional fields (e.g., service duration, age groups).

2. **Analyzing User Behavior**:
   - Aggregate data per user per month.
   - Calculate metrics like total calls made, total minutes used, messages sent, and data consumed.
   - Visualize distributions and averages using plots.

3. **Calculating Revenue**:
   - Determine extra usage beyond plan limits.
   - Calculate additional charges for minutes, messages, and data.
   - Compute total monthly revenue per user.

4. **Visualizing Revenue and Usage Patterns**:
   - Plot revenue trends over time for both plans.
   - Visualize user growth per plan.
   - Compare average revenue per user.

5. **Statistical Hypothesis Testing**:
   - Formulate null and alternative hypotheses regarding average revenues.
   - Use t-tests to compare average revenues between plans and regions.
   - Interpret p-values to accept or reject hypotheses.

6. **Drawing Conclusions**:
   - Summarize findings from the analysis.
   - Provide recommendations based on the data.

## Conclusions

- **Plan Popularity**:
  - The **Surf** plan is more popular, with a larger and faster-growing user base compared to the **Ultimate** plan.

- **Revenue Generation**:
  - **Ultimate** users contribute more revenue per user due to higher monthly fees.
  - Despite having fewer users, the Ultimate plan's higher per-user revenue balances overall earnings.

- **User Behavior Patterns**:
  - **Calls**: Both plans show similar call usage patterns, with average monthly call durations around 400-430 minutes.
  - **Messages**: Ultimate plan users send more messages on average, benefiting from higher message allowances.
  - **Data Usage**: Ultimate users tend to consume slightly more data, aligning with the plan's generous data allowance.

- **Statistical Findings**:
  - There is a statistically significant difference in average monthly revenue between the Surf and Ultimate plans.
  - Users in the NY-NJ area generate different average revenue compared to users from other regions, indicating regional variations.

- **Recommendations**:
  - **Marketing Strategy**: Focus on promoting the Ultimate plan to increase its user base and capitalize on higher per-user revenue.
  - **Regional Promotions**: Develop targeted marketing campaigns for regions showing different usage and revenue patterns.
  - **Plan Adjustments**: Consider adjusting plan offerings based on user behavior to maximize customer satisfaction and profitability.

## Project Structure

- **`megaline_analysis.ipynb`**: The main Jupyter Notebook containing the step-by-step analysis.
- **`datasets/`**: Directory containing all the datasets used in the project.