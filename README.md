<h1>Energy Bill Calculator - Python Application</h1>

<h2>Description</h2>
This repository contains a **Python-based Energy Bill Calculator** that helps users estimate their monthly electricity costs based on power consumption and local energy rates. The program takes **appliance usage data, kilowatt-hour (kWh) rates, and time-of-use pricing** into account to generate an accurate bill estimate.
<br />

<h2>Key Features & Functionalities</h2>

- <b>Dynamic Energy Cost Calculation:</b> Computes total electricity cost based on **kWh usage and local rates**.
- <b>Appliance Power Consumption Analysis:</b> Allows users to input **multiple appliances**, their power ratings, and daily usage.
- <b>Time-of-Use Pricing Support:</b> Adjusts calculations based on **peak, off-peak, and standard rates**.
- <b>Customizable Tariff Plans:</b> Users can input their own **utility provider's rates** for accuracy.
- <b>Graphical Breakdown of Energy Usage:</b> Provides **data visualization using Matplotlib** (if enabled).
- <b>CSV Export Feature:</b> Saves consumption details for **record-keeping and comparison**.

<h2>Environments Used</h2>

- <b>Windows 10 / 11</b> (Development & Testing)
- <b>Python 3.x</b> (Core Programming)
- <b>Matplotlib & Pandas</b> (Data Analysis & Visualization)
- <b>VS Code / PyCharm</b> (Code Development)

<h2>Project Walkthrough:</h2>

<p align="center">
Launching the calculator: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Energy Calculator UI"/>
<br />
<br />
Inputting appliance details:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="User Input"/>
<br />
<br />
Analyzing energy consumption: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Data Analysis"/>
<br />
<br />
Visualizing energy usage trends:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Graph Output"/>
</p>

<h2>Step-by-Step Implementation</h2>

<h3>1. Installation & Setup</h3>
<ul>
    <li>Install Python 3.x and ensure it's added to your **system path**.</li>
    <li>Install required dependencies using:
        <pre><code>pip install matplotlib pandas</code></pre>
    </li>
    <li>Clone this repository and navigate to the project folder.</li>
</ul>

<h3>2. Running the Energy Calculator</h3>
<ul>
    <li>Launch the script using:
        <pre><code>python energy_calculator.py</code></pre>
    </li>
    <li>Enter appliance details (**power rating, daily usage hours, number of devices**).</li>
    <li>Select energy pricing type (**flat rate or time-of-use pricing**).</li>
    <li>Review estimated costs and **view graphical analysis (optional).**</li>
</ul>

<h3>3. Understanding the Calculation Logic</h3>
<ul>
    <li>The script calculates energy consumption as:
        <pre><code>Total Energy (kWh) = Power (W) × Hours Used ÷ 1000</code></pre>
    </li>
    <li>The total bill is derived using:
        <pre><code>Bill Amount = Total Energy × Rate per kWh</code></pre>
    </li>
    <li>If **time-of-use pricing** is enabled, rates vary based on usage time.</li>
</ul>

<h3>4. Exporting Data for Analysis</h3>
<ul>
    <li>Users can save reports in CSV format for later analysis.</li>
    <li>Use Pandas to generate structured reports with:
        <pre><code>df.to_csv("energy_report.csv", index=False)</code></pre>
    </li>
</ul>

<h2>Example Output</h2>

```plaintext
----------------------------------------------
Energy Bill Calculator - Python Version
----------------------------------------------
Enter the number of appliances: 2

Appliance 1: Refrigerator
Power Rating (W): 150
Hours Used Per Day: 24
Number of Units: 1

Appliance 2: TV
Power Rating (W): 100
Hours Used Per Day: 5
Number of Units: 1

Energy Consumption Breakdown:
- Refrigerator: 108 kWh/month
- TV: 15 kWh/month

Total Energy Usage: 123 kWh
Energy Cost (at $0.12/kWh): $14.76

Report saved as "energy_report.csv"
