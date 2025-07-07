# Capstone-project
Real-time dynamic pricing for parking lots using Pathway and Bokeh. Automatically adjusts prices based on demand, with live interactive visualizations.
Dynamic Parking Pricing with Real-Time Data
Overview
This project implements real-time dynamic pricing for parking lots using Python, Pathway, and Bokeh. The system adjusts parking prices automatically based on live demand factors such as occupancy, queue length, and special days, and visualizes results interactively.

Tech Stack
Python (pandas, numpy)

Pathway (real-time data processing)

Bokeh + Panel (interactive visualization)

Google Colab (notebook environment)

Architecture Diagram
text
flowchart TD
    A[CSV Data] --> B[Data Cleaning (pandas)]
    B --> C[Pathway Streaming Pipeline]
    C --> D[Pricing Models]
    D --> E[Bokeh Visualization Dashboard]
Project Architecture & Workflow
Data Preparation:
Raw parking data is cleaned and converted to numeric types using pandas. Categorical fields (like traffic condition) are mapped to numbers, and missing values are handled.

Streaming Pipeline:
Pathway ingests the cleaned data as a real-time stream, applies windowing and aggregation (per parking lot, per day), and computes features needed for pricing.

Pricing Models:

Model 1: Simple occupancy-based price formula.

Model 2: Demand-based price model using occupancy, queue length, traffic, special day, and vehicle type.

Visualization:
Bokeh and Panel are used to create an interactive dashboard that shows real-time price changes for each parking space, with both models plotted for comparison.

Getting Started
Clone this repository.

Open the Colab notebook (your_notebook_name.ipynb).

Run all cells (dependencies are installed automatically).

The dashboard will appear in the notebook output.

Data
The dataset (dataset.csv) contains all required columns and is documented in the notebook.

Results
Real-time price plots for each parking lot.

Visual justification for dynamic pricing decisions
