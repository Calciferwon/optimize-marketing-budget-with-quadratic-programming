# optimize-marketing-budget-with-quadratic-programming
 
This repository contains a Python-based implementation of a quadratic programming (QP) model to optimize marketing budget allocation across multiple advertising channels. The model minimizes portfolio risk (variance) while ensuring the target number of acquisitions is achieved within budget and channel-specific constraints.

# Table of Contents
1. Overview
2. Features
3. Requirements
4. Installation
5. Usage
6. Example Output
7. Future Improvements

# Overview
Modern marketing campaigns rely on balancing high returns with manageable risk across various advertising channels. This project uses quadratic programming to:

1. Optimize budget allocation across channels such as Social Media, SEM, Email Marketing, and others.
2. Minimize risk, defined as the variability of performance across channels, while maximizing acquisitions.
3. Respect channel-specific constraints like minimum and maximum allocation limits.
The model incorporates expected returns and a covariance matrix to manage channel relationships and uncertainty in performance.

# Features
- Risk Minimization: Reduces total variance of the portfolio while meeting acquisition goals.
- Target Acquisition Constraint: Ensures the total acquisitions meet or exceed a predefined target.
- Channel Constraints: Handles minimum and maximum allocations per channel.
- Customizable Covariance Matrix: Adjust variance and covariance to reflect real-world channel performance.
- Python Implementation: Uses cvxpy for solving quadratic programming problems.

# Requirements
The code is written in Python and requires the following packages:

- Python 3.8+
- cvxpy: For formulating and solving the quadratic programming problem.
- NumPy: For matrix operations.
- Pandas (optional): For handling input data.
Install the dependencies using pip:
pip install cvxpy numpy pandas

# Installation
1. Clone the repository:
git clone https://github.com/your-username/marketing-budget-optimization.git
2. Navigate to the project directory:
cd marketing-budget-optimization

# Usage
1. Open the Python file containing the model code
2. Modify the input parameters in the script:

- Channels: Define the marketing channels and their constraints.
- Expected Returns: Specify the returns per dollar for each channel.
- Covariance Matrix: Adjust the variance and covariance values to reflect channel relationships.
- Target Acquisitions: Set the minimum number of acquisitions required.
- Budget: Set the total budget available for allocation.

3. Run the script
4. View the results:
- Optimal budget allocation for each channel.
- Expected acquisitions for each channel.
- Total acquisitions and minimized risk (variance).

# Example Output
When the model is executed, the output includes:

- Optimal Allocations: How much budget is allocated to each channel.
- Expected Acquisitions: Predicted acquisitions for each channel.
- Total Expected Acquisitions: Ensures it meets or exceeds the target.
- Minimized Total Variance (Risk): Represents the portfolio's risk level.

Example Output:
- Social Media: Allocation = $12000.00, Expected Acquisitions = 3360.00
- SEM: Allocation = $15000.00, Expected Acquisitions = 5100.00
- Content: Allocation = $10000.00, Expected Acquisitions = 2100.00
- Email: Allocation = $7000.00, Expected Acquisitions = 980.00
- Display: Allocation = $6000.00, Expected Acquisitions = 1080.00

Total Expected Acquisitions: 13825.00
Minimum Total Variance (Risk): 205000.000000

# Future Improvements
1. Dynamic Covariance Matrix:
- Automate covariance matrix generation based on historical performance data.
2. Interactive Inputs:
- Allow users to input constraints, returns, and budgets dynamically via a command-line interface or web app.
3. Visualization:
- Add visualizations to show allocation distribution and risk-return trade-offs.
