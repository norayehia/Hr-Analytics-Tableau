# Hr-Analytics-Tableau
Here’s how to perform various operations and create visualizations using Tableau:

### 1. Create a New Calculated Column for Attrition
To categorize employee attrition as binary values (1 for 'Yes', 0 for 'No'):
- Navigate to the **Data** pane.
- Right-click and select **Create Calculated Field**.
- Name the field `attrition01`.
- Enter the formula: `IF [Attrition] = 'Yes' THEN 1 ELSE 0 END`.
- Click **OK**. This adds a new column in your dataset where attrition marked as 'Yes' is represented by 1, and 'No' by 0.

### 2. Sum Values by Double-Clicking a Column
- To quickly sum values of any column:
- Double-click the desired column in the **Data** pane.
- Tableau automatically creates a sum measure and adds it to the view.

### 3. Calculate Attrition Rate
To compute the attrition rate as the ratio of attrited employees to the total number of employees:
- Right-click in the **Data** pane and choose **Create Calculated Field**.
- Name it `Attrition Rate`.
- Enter the formula: `SUM([attrition01]) / SUM([Employee Count])`.
- Click **OK** to add this calculation to your dataset.

### 4. Calculate Active Employees
To determine the number of active employees:
- Create a new calculated field named `Active Employees`.
- Enter the formula: `SUM([Employee Count]) - SUM([attrition01])`.
- This will subtract the sum of attrited employees from the total employee count.

### 5. Calculate Average Age
To find the average age of employees:
- Double-click the `Age` column to add it to the view as a sum.
- Right-click on the SUM(Age) field in the view or the **Marks** card.
- Hover over **Measure (Sum)** and change it to **Average**.
- This adjusts the calculation to compute the average age.

### 7. Create a PowerPoint-Style Background
- To set a custom background, such as an image:
- Go to **Map** in the top menu, then select **Background Images**, and choose your data source.
- Click **Add Image** to browse and select the desired image file.
- Adjust settings for the image to fit your layout as required.

### 8. Rename a Column
To rename a column in Tableau:
- Right-click the column in the **Data** pane.
- Select **Rename**, and enter the new name (e.g., change `attrition01` to `AttrCount`).

### Additional Visualization Steps

#### Creating a Department Pie Chart
To visualize department data as a pie chart:
- Drag the `Department` field to the **Color** mark on the **Marks** card.
- Change the chart type to **Pie** by selecting the pie chart icon in the **Show Me** pane.
- This will display the data as a pie chart, with slices colored differently for each department.
