## Dynamic-Pricing-Of-Parking-Lots
This project demonstrates a dynamic pricing system for urban parking lots using real-time data streams. The goal is to automatically adjust parking prices throughout the day based on factors such as occupancy, demand, traffic, and other conditions, in order to maximize parking space usage and improve efficiency.

The system uses Pathway for real-time data processing, Pandas and Numpy for data analysis, and Bokeh along with Panel for interactive visualizations.

🚀 Tech Stack
Python 3.11+

Pathway: Real-time data streaming & transformation

Pandas & Numpy: Data analysis & processing

Bokeh & Panel: Interactive visualizations (in notebooks or web apps)

Mermaid: Architecture diagrams

🏗️ Project Architecture
mermaid
Copy
Edit
flowchart TD
    A[Parking Data Source (CSV/Stream)] --> B[Pathway Data Ingestion]
    B --> C{Data Cleaning \n & Feature Engineering}
    C --> D[Dynamic Pricing Model]
    D --> E[Real-time Pricing Output]
    E --> F[Visualization (Bokeh/Panel)]
    C --> G[Demand Calculation]
    D --> H[Competitor Price Check (Optional)]
    style H stroke:#f66,stroke-width:2px
📝 Architecture & Workflow Details:
🔹 Data Ingestion:
The system collects parking data from CSV files or streaming sources. The data includes:

Timestamp

Occupancy

Capacity

Traffic conditions

Queue length

Special events

Vehicle types

🔹 Preprocessing & Feature Engineering:
Time-based operations are performed using Pathway to parse timestamps and create data windows.

Additional features are created such as:

Occupancy percentage

Normalized demand

Vehicle type weights

🔹 Demand-based Pricing Model:
The pricing algorithm (Model 2) calculates demand based on occupancy, queue length, traffic, special events, and vehicle type.

Demand values are normalized either globally or within time windows to ensure smooth price changes.

Pricing is constrained within reasonable limits (from 0.5× to 2× of base price).

🔹 (Optional) Competitor Pricing:
The system can also include competitor parking prices (Model 3).

Pricing is adjusted according to nearby parking lots’ rates.

🔹 Real-time Visualization:
Real-time trends of parking prices are displayed through Bokeh & Panel dashboards.

You can visualize both individual parking lot prices and overall market trends.
