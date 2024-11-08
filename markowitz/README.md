# Markowitz Portfolio Optimization with Interactive Visualization

(TO DO IN WINTER)

This project implements the Markowitz Portfolio Optimization Model to construct an optimal portfolio based on historical financial data. The optimization will calculate the Efficient Frontier, which represents the best possible portfolios offering the highest return for a given level of risk. Additionally, we will create interactive visualizations using Plotly to explore the risk-return tradeoff and analyze portfolio allocations dynamically.

## Features

	•	Data Collection: Fetch historical price data for selected assets using yfinance.
	•	Portfolio Optimization:
	•	Minimize portfolio risk for a given target return.
	•	Maximize portfolio return for a given risk level.
	•	Efficient Frontier Visualization: Interactive graph displaying optimal portfolios.
	•	Portfolio Allocation Analysis: View how weights of different assets change along the Efficient Frontier.
	•	Custom Constraints:
	•	No short-selling (weights >= 0).
	•	Fully invested portfolio (weights sum to 1).
	•	Interactive Dashboard: Use Plotly to dynamically adjust target returns and view portfolio risk/return and allocations.

## Project Setup

1. Clone the Repository

Clone the repository to your local machine using the following command:

git clone <repository-url>
cd Markowitz-Portfolio-Optimization

2. Install Required Dependencies

Ensure you have Python installed (version 3.7 or higher). Install the required libraries using pip:

pip install -r requirements.txt

Alternatively, you can manually install the required Python libraries:

pip install yfinance pandas numpy cvxpy plotly

3. Fetch Historical Data

The project uses the yfinance library to fetch historical financial data for the assets you want to analyze. Edit the src/fetch_data.py file to specify your list of assets (tickers) and the date range.

Example of editing the tickers:

# Example: src/fetch_data.py
tickers = ["AAPL", "MSFT", "GOOGL", "AMZN"]
start_date = "2018-01-01"
end_date = "2023-01-01"

Run the script to download data:

python src/fetch_data.py

4. Run Portfolio Optimization

The src/optimization.py file contains the logic for solving the Markowitz optimization problem. Edit the script to adjust parameters, such as target returns or constraints, and run it to calculate the Efficient Frontier and portfolio allocations.

Run the script:

python src/optimization.py

5. Interactive Visualization

Visualize the Efficient Frontier and portfolio allocations using the interactive dashboard. The src/visualize.py file generates an interactive Plotly chart.

Run the script:

python src/visualize.py

6. Explore Outputs

	•	Efficient Frontier: View the risk-return tradeoff and dynamically analyze portfolio allocations.
	•	Portfolio Weights: Examine how asset weights change along the Efficient Frontier.

## Tools and Libraries

	•	Python: Core programming language.
	•	Libraries:
	•	yfinance: To fetch historical financial data.
	•	numpy: For numerical computations.
	•	pandas: For data manipulation.
	•	cvxpy: For portfolio optimization (convex programming).
	•	plotly: To create interactive visualizations.

## Folder Structure

Markowitz-Portfolio-Optimization/
├── data/                # Folder for storing fetched financial data
├── notebooks/           # Jupyter notebooks for analysis and testing
├── src/                 # Python scripts for optimization and visualization
│   ├── fetch_data.py    # Script to fetch historical data
│   ├── optimization.py  # Markowitz optimization logic
│   └── visualize.py     # Code for interactive visualizations
├── README.md            # Project overview and setup instructions
└── requirements.txt     # List of dependencies

Future Enhancements

	•	Add real-time data fetching for dynamic portfolio optimization.
	•	Incorporate transaction costs into the model.
	•	Use machine learning to predict future asset returns for input into the model.
	•	Implement rebalancing strategies for maintaining optimal portfolios over time.