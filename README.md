
# AGRICULTURE DATA ANALYSIS

## Dashboard Overview: Rainfall · Temperature · Humidity · Yields Analysis (Power BI)

### Problem Statement

This dashboard helps agricultural analysts, farmers, and policymakers understand the relationship between climate conditions and crop productivity. By visualizing rainfall, temperature, humidity, and yield data across multiple dimensions — year, season, crop type, and location — stakeholders can:


Identify which crops perform best under specific climate conditions.
Pinpoint locations with the highest and lowest yields.
Recognize seasonal patterns that affect agricultural output.
Track year-over-year changes in climate and productivity trends.


Since Rabi season records the highest average yields (24.9K) while Kharif records the lowest (20.2K), and since Cotton leads crop yields (51K) while Paddy leads in rainfall reception (3.5K mm), actionable strategies can be built around these insights to improve yield forecasting and planning.


### Steps Followed


* Step 1 : Load data into Power BI Desktop; the dataset is a CSV file containing agriculture climate records from Karnataka, India (2005–2020).

* Step 2 : Open the Power Query Editor. Under the View tab, in the Data Preview section, enable "Column Distribution", "Column Quality", and "Column Profile" options for thorough data inspection.

* Step 3 : Change column profiling from the default 1,000 rows to "Column profiling based on entire dataset" to ensure all data quality checks are accurate.

* Step 4 : Inspect all columns for errors and null/empty values. Minor inconsistencies were addressed; core metric columns (Rainfall, Temperature, Humidity, Yield) were clean and ready for analysis.

* Step 5 : In the Report View, select a consistent theme under the View tab. A pink/purple color palette was applied across all four report pages for visual consistency and brand identity.

* Step 6 : The report is structured into four dedicated pages, each focusing on a single climate/agricultural metric:

#### Page 1 — Rainfall Analysis
#### Page 2 — Temperature Analysis
#### Page 3 — Humidity Analysis
#### Page 4 — Yields Analysis



* Step 7 : On each report page, four horizontal bar chart visuals were added to represent averages broken down by:
(a) Year (2005–2020)
(b) Season (Rabi, Kharif, Zaid)
(c) Crop Type (Paddy, Cotton, Ginger, Tea, Coffee, Coconut, etc.)
(d) Location (Bangalore, Raichur, Kasaragodu, Mangalore, Kodagu, Mysuru, etc.)

* Step 8 : A large title banner was added at the top of each page using a styled text box, clearly labeling each page (e.g., "RAINFALL ANALYSIS", "TEMPERATURE ANALYSIS").

* Step 9 : Each of the four visuals on every page was placed inside a styled card container with a contrasting border (purple/dark violet) and a soft pink background to match the overall theme.

* Step 10 : Chart title formatting was customized per page with unique color-coded titles:

#### Rainfall page → Purple titles
#### Temperature page → Golden/Olive titles
#### Humidity page → Teal/Cyan titles
#### Yields page → Green titles


This color differentiation helps users quickly distinguish the metric being displayed.

* Step 11 : Bar chart colors were assigned distinctively per metric and sub-visual:

PageBy YearBy SeasonBy CropsBy LocationRainfallPurple/VioletPeriwinkle BlueOlive/GoldSalmon PinkTemperatureOlive/GoldPeriwinkle BlueSalmon PinkDark PurpleHumidityCyan/TealSteel BlueOlive/GoldSalmon PinkYieldsLight GreenDark GreenLime GreenDark Green


* Step 12 : Data labels were enabled on all bar charts to display exact values (e.g., 3.5K mm rainfall for Paddy, 51K yield for Cotton), making the visuals self-explanatory without requiring axis reference.

* Step 13 : A scrollable view was retained for the "By Crops" and "By Location" charts since these contain more entries than fit in a single view — a scrollbar indicator is visible on the right side of these visuals.

* Step 14 : DAX measures were created for all average calculations across the four metrics. Example expressions:


DAX  Avg Rainfall = AVERAGE(agriculture_data[Rainfall])

  Avg Temperature = AVERAGE(agriculture_data[Temperature])

  Avg Humidity = AVERAGE(agriculture_data[Humidity])

  Avg Yield = AVERAGE(agriculture_data[Yield])


* Step 15 : A Season filter was applied using slicer visuals (Rabi, Kharif, Zaid) to allow dynamic filtering across all four pages.

* Step 16 : A Location filter and Crop Type filter were also added as slicers to enable granular, cross-page filtering so analysts can drill into specific regions or crops.

* Step 17 : The report was published to Power BI Service for sharing and collaboration.



### Snapshot of Dashboard (Power BI Desktop)

#### Page 1 — Rainfall Analysis

![image alt](https://github.com/user-attachments/assets/91bfa78b-9a63-4fa2-a3dd-e4e21a6fedae)

#### Page 2 — Temperature Analysis

![image alt](https://github.com/user-attachments/assets/455fb683-6aa5-400a-861c-f90263dce6fb)

#### Page 3 — Humidity Analysis

![image alt](https://github.com/user-attachments/assets/a6a0942b-4db3-4327-8d28-a28122d8b7f7)

#### Page 4 — Yields Analysis

![image alt](https://github.com/user-attachments/assets/8b320c91-faa8-481a-b7fd-d24df559737b)


## Results

A four-page report was created on Power BI Desktop and published to Power BI Service.

The following inferences can be drawn from the dashboard:


### [1] Rainfall Analysis

* Average Rainfall by Year:

Rainfall fluctuated between 2,740 mm (2020) and 3,199 mm across the observed years.
The year 2010 recorded one of the higher average rainfalls at 3,174 mm.


* Average Rainfall by Season:


Rabi: 3,105 mm
Kharif: 3,097 mm
Zaid: 3,070 mm
→ All three seasons receive broadly similar rainfall, with Rabi slightly higher.


* Average Rainfall by Crops:


Paddy receives the highest average rainfall — 3.5K mm
Arecanut & Cardamum — 3.3K mm
Coffee & Tea — 3.1K mm


* Average Rainfall by Location:


Bangalore leads with 3.8K mm
Raichur, Kasaragodu, Mangalore — 3.2K mm
Kodagu receives the least — 3.0K mm



### [2] Temperature Analysis

* Average Temperature by Year:


Temperature ranged from a low of 41°F (2020) to a high of 73°F (2015).
Most years averaged around 68–73°F.


* Average Temperature by Season:


Kharif: 72°F
Zaid: 72°F
Rabi: 61°F (cooler season)
→ Kharif and Zaid are the hottest seasons; Rabi is significantly cooler.


* Average Temperature by Crops:


Ginger grows in the highest temperature zones — 79°F
Tea & Cashew — 74°F
Coffee grows in cooler zones — 62°F


* Average Temperature by Location:


Bangalore records the highest — 3.8K (scale-adjusted)
Kodagu records the lowest — 3.0K



### [3] Humidity Analysis

* Average Humidity by Year:


Humidity remained remarkably consistent across all years — ranging from 55 to 56%.


* Average Humidity by Season:


Rabi: 56%
Zaid: 56%
Kharif: 56%
→ Humidity is virtually uniform across all seasons.


* Average Humidity by Crops:


Cotton, Pepper, Coffee, Blackgram, Paddy, Coconut — all at 56%
Arecanut & Cardamum — slightly lower at 55%


* Average Humidity by Location:


All major locations (Davangere, Raichur, Hassan, Kodagu, Mysuru, Gulbarga, Mangalore, Madikeri) maintain a consistent 56% humidity.
→ Humidity is a stable variable across this dataset with minimal variation.



### [4] Yields Analysis

* Average Yields by Year:


Yields varied significantly: from 16.4K (2010) to 28.7K (2010 peak).
The highest single-year average yield reached 28.7K.


* Average Yields by Season:


Rabi: 24.9K (highest)
Zaid: 22.0K
Kharif: 20.2K (lowest)
→ Rabi season produces the best yields overall.


* Average Yields by Crops:


Cotton: 51K — by far the highest yielding crop
Coconut: 34K
Ginger: 26K
Tea: 23K
Blackgram: 16K
Coffee: 13K
Paddy: 10K — lowest yield despite high rainfall


* Average Yields by Location:


Kodagu: 29K — top yielding district
Mysuru: 28K
Madikeri: 25K
Kasaragodu & Raichur: 24K
Bangalore: 22K — despite highest rainfall and temperature readings
→ Kodagu and Mysuru are the most productive agricultural districts in this dataset.



## Tools & Technologies Used

ToolPurposePower BI DesktopDashboard development & DAX measuresPower Query EditorData cleaning & transformationPower BI ServicePublishing & sharingCSV DatasetSource data (Karnataka agriculture, 2005–2020)

