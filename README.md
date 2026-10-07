# Sales and Revenue Analysis

This repository contains my solution for Homework 2. The project focuses on inspecting, tidying, joining, and analyzing sales, shipment, and company revenue data using Python and Pandas.

## Repository Structure

- `data/` contains the CSV datasets used in the analysis.
- `src/` contains the Jupyter notebooks for Tasks 0–5.
- `WRITEUP.md` contains the written responses and explanations for the assignment.

## Running the Analysis

The notebooks are organized by task and should be viewed in numerical order:

1. `Task 0.ipynb` – Initial data inspection and raw visualization
2. `Task 1.ipynb` – Reshaping the revenue dataset
3. `Task 2.ipynb` – Checking key uniqueness and join cardinality
4. `Task 3.ipynb` – Joining orders and shipments and comparing customer means
5. `Task 4.ipynb` – Creating the final analysis-ready table
6. `Task 5.ipynb` – Creating the final visualization

The analysis uses Python with Pandas and Matplotlib. The CSV files required by the notebooks are located in the `data/` directory.

## Generative AI Usage

I used ChatGPT as a support tool while completing this assignment. It was used to:

- Explain tidy-data concepts and the three tidy-data rules.
- Explain join cardinality and why the orders-to-shipments relationship is one-to-many.
- Help reason about the choice of left joins when combining the datasets.
- Explain why repeated shipment records can duplicate order amounts and revenue values after a join.
- Review and troubleshoot Python/Pandas syntax for reshaping, joining, grouping, and removing duplicates.
- Assist with Matplotlib visualization syntax.
- Help organize and edit the wording of the written explanations and README.

I reviewed the generated suggestions and am responsible for the final code, analysis, and explanations included in this repository.
