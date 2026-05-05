Indian Roads Accident Analysis
-- Project Overview
This project contains a comprehensive MySQL database and a series of analytical views designed to study road accidents in India. The dataset includes details such as location coordinates, weather conditions, traffic density, and accident severity.

The goal is to provide a data-driven approach to understanding why accidents happen and how to mitigate risks in major metropolitan areas like Mumbai, Delhi, Pune, and Bangalore.

-- Key Features of the Analysis
The SQL script generates several analytical views to simplify data interpretation:

Temporal Trends: Analyzing accidents by day of the week and identifying spikes during festival seasons (e.g., Holi).

Environmental Impact: Correlation between low visibility (fog/rain) and accident frequency.

Severity Assessment: Distribution of accidents classified as Fatal, Major, or Minor.

Casualty Analysis: Calculating average casualties relative to the severity of the crash.

Risk Scoring: Utilizing a pre-calculated risk_score to identify the most dangerous road types and hours.

-- Database Schema
The main table indian_roads_dataset includes the following critical fields:

Spatial Data: city, state, latitude, longitude.

Environmental Data: weather, visibility, temperature.

Road Infrastructure: road_type (Highway/Urban/Rural), lanes, traffic_signal.

Accident Details: cause (Overspeeding, Drunk Driving, etc.), accident_severity, casualties.

-- How to Use
Import the Database:

Bash
mysql -u your_username -p indian_roads < your_dump_file.sql
Query the Views:
To see the most dangerous states:

SQL
    SELECT * FROM accident_count_by_state ORDER BY accidents DESC;
    ```
    To analyze accidents during festivals:
    ```sql
    SELECT * FROM festival_season;
    ```

##  Key Findings (Based on Data)
*   **Weather Patterns**: A significant portion of 'Fatal' accidents occurs during **foggy** conditions with **low visibility**.
*   **Driver Behavior**: Overspeeding and drunk driving remain the leading human causes of severe accidents.
*   **Peak Risks**: The data suggests higher risk scores during specific hours, often correlating with peak traffic density or late-night driving.

##  Conclusion
The analysis reveals that road safety in India is heavily influenced by a combination of **environmental visibility** and **driver discipline**. While "Urban" roads see a high frequency of minor accidents due to density, "Highways" are prone to higher severity and fatalities, especially under poor weather conditions. Implementing stricter speed monitoring during low-visibility windows and festival seasons could significantly reduce the casualty rate.



