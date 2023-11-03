# Call-Center-Trends
A PwC internship project that involved analyzing data for a call center to identify and visually show certain metrics and KPIs such as Average speed of answer, total number of calls, average length of calls, abandoned calls, and more.


<p align = "center">
<img  src="https://github.com/Fey-Lajide/Call-Center-Trends/assets/124121752/45ae6496-006d-4d94-b351-c36ce809646e.png" width="1720" height="650"> <BR/><BR/>
</p>

<H2> TABLE OF CONTENTS </H2>
⚡ DATA PREPARATION <br/><BR/>
⚡ DATA MODELLING <br/><BR/>
⚡ DATA VISUALIZATION <br/><BR/>
⚡ DATA ANALYSIS <br/><BR/>

<H2> DATA PREPARATION </H2>
<H3> DATA CLEANING </H3>
The following cleaning process was undergone to make the data suitable for modeling and analysis(DONE IN THE POWER QUERY ENVIRONMENT):<br/><BR/>

👯 It was noticed that the table had no headers and that the first role were the headers for the table, and so the first row was promoted using the "use first row as header" prompt. <br/><BR/>
👯 The datatype for the call id column was changed from numeric to text.<br/><BR/>
👯 A conditional column was added for the column: satisfaction rating to properly convert the rating number to ratings that are easier to analyse and visualize.<BR/><BR/>
----- 5 - Very Satisfied<BR/>
----- 4 - Satisfied <BR/>
----- 3 - Neutral<BR/>
----- 2 - Unsatisfied<BR/>
----- 1 - Very unsatisfied
<p align = "center">
<img  src="https://github.com/Fey-Lajide/Call-Center-Trends/assets/124121752/aa977bc3-897c-4afe-b4a9-e735d74c4dcd.png" width="620" height="550"><BR/><BR/>
</p>
<br/>
<p align = "center">
<img  src="https://github.com/Fey-Lajide/Call-Center-Trends/assets/124121752/58536416-a049-478b-a059-ea3e00c4235f.png" width="620" height="550"><BR/><BR/>
</p>
<br/><br/>
<H3> DATA TRANSFORMATION </H3>
The following measures were created using the DAX Functions. <br/><br/>
----- Agent Perfomance Quadrant = SUM(Sheet1[AvgTalkDuration])/[Total No of Answered Calls]<br/>
----- avg length of calls = [Length of Calls]/[Total No of Calls]<br/>
----- Avg Speed of Answer = SUM(Sheet1[Speed of answer in seconds])/[Total No of Answered Calls]<br/>
----- Length of Calls = SUM(Sheet1[Speed of answer in seconds])*SUM(Sheet1[AvgTalkDuration])<br/>
----- resolved cases = CALCULATE(COUNT(Sheet1[Call Id]), Sheet1[Resolved] = "Y")<br/>
----- Total Cases = COUNT(Sheet1[Resolved])<br/>
----- Total Neutral = CALCULATE(COUNT(Sheet1[Satisfaction rating]), Sheet1[Satisfaction Level] = "Neutral")<br/>
----- Total No of Abandoned Calls = CALCULATE(COUNT(Sheet1[Answered (Y/N)]), Sheet1[Answered (Y/N)] = "N")<br/>
----- Total No of Answered Calls = CALCULATE(COUNT(Sheet1[Answered (Y/N)]), Sheet1[Answered (Y/N)] = "Y")<br/>
----- Total Satisfied = CALCULATE(COUNT(Sheet1[Satisfaction rating]), Sheet1[Satisfaction Level] = "Satisfied")<br/>
----- Total Unatisfied = CALCULATE(COUNT(Sheet1[Satisfaction rating]), Sheet1[Satisfaction Level] = "Unsatisfied")<br/>
----- Total Very Satisfied = CALCULATE(COUNT(Sheet1[Satisfaction rating]), Sheet1[Satisfaction Level] = "Very Satisfied")<br/>
----- Total Very UnSatisfied = CALCULATE(COUNT(Sheet1[Satisfaction rating]), Sheet1[Satisfaction Level] = "Very Unsatisfied")<br/>
----- unresolved cases = CALCULATE(COUNT(Sheet1[Call Id]), Sheet1[Resolved] = "N")<br/><br/>

<p align = "center">
<img  src="https://github.com/Fey-Lajide/Call-Center-Trends/assets/124121752/759c1b0e-fb23-4f40-9cf2-09175b80cfbb.png" width="620" height="550"><BR/><BR/>
</p>

<h2> DATA MODELLING </h2>
There was no need for modeling, as only one table was supplied.
<br/><br/>
<p align = "center">
<img  src="https://github.com/Fey-Lajide/Call-Center-Trends/assets/124121752/47470dda-5cd2-4e9c-a444-b11797e7d281.png" width="420" height="500"><BR/><BR/>
</p>

<h2> DATA VISULAIZATION </h2>
The following visualization tools were used for their respective purposes:
<br><BR/>
🛠️ Cards: To visualize the average speed of answer, answered calls, abandoned calls, and average length of calls <BR/><BR/>
🛠️ Donut Chart: To visulize the overall customer satisfaction <BR/><BR/>
🛠️ Line Chart: To visualize calls per time. </BR><BR/>
🛠️ Slicer: For filtering agent and topic. </BR><BR/>
🛠️ 100% Stacked Bar Chart: To visualize resolved vs unresolved cases. <BR/><BR/>
🛠️ Scatter Plot: To show the agent quadrant (average call duration vs calls answered)

<BR/><br/>
<p align = "center">
<img  src="https://github.com/Fey-Lajide/Call-Center-Trends/assets/124121752/c5c91f77-689b-4d26-8585-3423d2655bb0.png" width="1720" height="650"><BR/><BR/>
</P>


<H2> DATA ANALYSIS </H2>
After telling a sales data story for LAJIDE BOOK AND STORES utilizing the processes listed above. It was time to make sense of what the visuals were telling. Here are some insights deduced from the reports:
<br/><br/>
📫 Copiers gave the highest profit in the profit for sub-category<br/><br/>
📫 The highest sales was recorded in 2018<br/><br/>
📫 The highest profit was recorded in the West region<br/><br/>
📫 Consumer had the highest profit was segment<br/><br/>
📫 Technology had the highest profit for category<br/><br/>
<br/><br/>
<p align = "center">
<img  src="https://github.com/Fey-Lajide/Sales-Insight/assets/124121752/c984958f-2d67-4d39-8407-3d221db6ea35png" width="1720" height="650"><BR/><BR/>
</P>
<p align = "center">
<img  src="https://github.com/Fey-Lajide/Sales-Insight/assets/124121752/2410f197-120e-4598-9ee8-8dee7aace542png" width="1720" height="650"><BR/><BR/>
</P>

<br/>


