# Predictive_Maintainance

A project done for the course Statistical Methods under <b>Dr. Sapna Shah</b> 
<h3>Team members</h3>
<ul>
<li><b>NAMAN CHHAPARIA I040</b> Github: <a href="https://github.com/NamanChh">NamanChh</a></li>
<li><b>ROHAN AJAY I050</b></li>

</ul>
<h2>Abstract</h2>
# Predictive Maintenance Dataset Description

## Dataset Overview
The dataset provided by the UCI repository is synthetic and mirrors real predictive maintenance scenarios encountered in industries. It comprises 10,000 data points stored as rows, each containing 14 features in columns.

## Features
1. **UID:** Unique identifier ranging from 1 to 10,000.
2. **Product ID:** Consists of a letter L, M, or H indicating low (60% of products), medium (30%), and high (10%) quality variants, along with a variant-specific serial number.
3. **Air Temperature [K]:** Generated using a random walk process and later normalized to a standard deviation of 2 K around 300 K.
4. **Process Temperature [K]:** Generated using a random walk process normalized to a standard deviation of 1 K, added to the air temperature plus 10 K.
5. **Rotational Speed [rpm]:** Calculated from a power of 2860 W, overlaid with normally distributed noise.
6. **Torque [Nm]:** Torque values are normally distributed around 40 Nm with a standard deviation of 10 Nm and no negative values.
7. **Tool Wear [min]:** Quality variants H/M/L add 5/3/2 minutes of tool wear to the used tool in the process.
8. **Machine Failure:** Label indicating whether the machine has failed in a particular data point for any of the following failure modes:
   - **Tool Wear Failure (TWF):** The tool will be replaced or fail at a randomly selected tool wear time between 200 - 240 mins.
   - **Heat Dissipation Failure (HDF):** A process failure occurs if the difference between air and process temperature is below 8.6 K and the tool's rotational speed is below 1380 rpm.
   - **Power Failure (PWF):** The product of torque and rotational speed (in rad/s) equals the power required for the process. If this power is below 3500 W or above 9000 W, the process fails.
   - **Overstrain Failure (OSF):** If the product of tool wear and torque exceeds 11,000 minNm for the L product variant (12,000 M, 13,000 H), the process fails due to overstrain.
   - **Random Failures (RNF):** Each process has a 0.1% chance to fail regardless of its parameters. If at least one of the above failure modes is true, the process fails, and the 'machine failure' label is set to 1.

### Note
It is not transparent to the machine learning method which failure mode has caused the process to fail.

<br>This model achieves a <b>Character Accuracy of 94.36% and Layout Accuracy of 81.83%</b>. Accuracy can be further increased by training our model on such similar documents.
