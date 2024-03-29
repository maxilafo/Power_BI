__This project was part of the DataCamp competition [Supply Chain Analytics - Just In Time](https://app.datacamp.com/learn/competitions/supply-chain-analytics).__

The purpose of this project was to create an interactive dashboard with performance related information, in order to get insights and summarize them
<p align="center">
<a href="https://ibb.co/v3cthvr"><img src="https://i.ibb.co/ZBfZS1w/Landing-Page.png" alt="Landing-Page" border="0"></a>
<a href="https://ibb.co/B4SStcw"><img src="https://i.ibb.co/0BddcmQ/Pages-Collage.png" alt="Pages-Collage" border="0"></a>
</p>

## About this project

<div style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'>
    <p>The data was very clean, I only had to correct the value &quot;Dominican Republic&quot; in the &quot;Customer Country&quot; column due to some special character in the space.</p>
    <p>I found inconsistencies between the Order Date and the Ship Date columns. The shipping date should always be after the order date, so the difference should always be positive. However, this is not the case as we found negative differences.</p>
    <p>There are also very large differences that do not correspond to reality. For example, a delivery of a pair of boots with a delay of 950 days, which is very unlikely.</p>
    <p>I called this difference &ldquo;Shipment Delay&rdquo;</p>
    <p align="center"><a href="https://ibb.co/9vkXvf0"><img src="https://i.ibb.co/Qc3BcqV/distribution.png" alt="distribution" border="0"></a></p>
    <p><strong><u>Identifying the outliers</u></strong></p>
    <p>I&apos;ve calculated the average and standard deviation of the shipment delay</p>
    <p>AVG = 24.54<br>STD = 94.77</p>
    <p>I decide to look at all outliers that are more than one standard deviation away from the mean, which is 120 days, rounded up.</p>
    <p>While it&rsquo;s still a long delay for a company who stated a maximum of 10 days for warehouse product fulfillment, I leave room for possible extraordinary causes that generate these delays.</p>
    <p>The ideal scenario would be to get in touch with the stakeholders to find out more about the issue and the causes in order to get the most reliable data possible.</p>
    <p><strong><u>Handling outliers</u></strong></p>
    <p>If I delete the rows, it will affect the sales metrics, or the count of orders, which must be accurate.<br>But regarding metrics related to the effectiveness of the shipments, I filtered the outliers out. I stuck to percentage or ratios KPIs.</p>
    <p>For example:</p>
    <p>N&deg; of shipments: I considered them all</p>
    <p>% On-Time Delivery: I filtered the outliers</p>
</div>

## EXECUTIVE SUMMARY
<div style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'>
    <p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong>GENERAL</strong></p>
    <p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'>In the last quarter of 2017, I see a very strong drop in the company&apos;s activity. It can be caused by external factors, such as the entry of new competitors, lack of stock supply, economic crisis, etc. Given that the company has a very diverse product portfolio, it is difficult to explain such a sharp overall drop in sales. A drop in consumption due to the economic downturn is the most likely explanation, but we need more information to make a more detailed diagnosis and make proposals to reverse the trend.</p>
    <p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong>SALES</strong></p>
    <ul class="decimal_type" style="list-style-type: disc;">
        <li>Total gross sales amount to 6.18 million dollars, of which 80% is attributable to NA, Europe and the LATAM markets.</li>
        <li>The main country customers are USA (15%), MX (8%) and FR (7.7%), which are also the most consistent.</li>
        <li>The Fan Shop division leads the way with 47% of total sales, followed by Apparel and Golf.</li>
        <li>The average margin is 64%, driven by golf margin (80%), footwear (80%) and apparel (68%).</li>
        <li>The top 5 products account for over 60% of total sales, with the &quot;Field &amp; Stream Sportsman 16 Gun Fire Safe&quot; being the star product with 18.62% of total sales.</li>
    </ul>
    <p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong>INVENTORY</strong></p>
    <p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'>The ratio of supply to demand should be slightly positive to ensure that there is capacity to meet demand, but to minimize storage costs. On the other hand, negative ratios should be avoided.</p>
    <ul class="decimal_type" style="list-style-type: disc;">
        <li>The overall ratio is 7%, which is good. The highest is Technology with 19.50% and the lowest is Health and Beauty with 37.93%.</li>
        <li>The unit storage cost varies between 1.38 and 1.15, with an average of 1.24. It should be as low as possible.</li>
        <li>The average monthly storage cost is around USD 2568, without considering the 4th quarter of 2017, when the figure drops to USD 2,400.</li>
        <li>I don&apos;t observe any kind of general stationary on demand.</li>
        <li>The dataset doesn&apos;t provide quality information to calculate the inventory turnover rate.</li>
    </ul>
    <p style='margin-top:0in;margin-right:0in;margin-bottom:8.0pt;margin-left:0in;font-size:11.0pt;font-family:"Calibri",sans-serif;'><strong>SHIPMENTS</strong></p>
    <ul class="decimal_type" style="list-style-type: disc;">
        <li>The overall on-time delivery rate is 55%, which is a very low rate for customer satisfaction.</li>
        <li>Over time, delivery times have increased significantly, from an average of 4 days at the start of 2015 to 74 days at the end of 2017.</li>
        <li>Health and Beauty is the product category that performs better, with an OTD rate of 66.7% and an average delivery time of 3.39 days, and Technology comes last with a rate of 43.7% and a delivery time of 9.16 days.</li>
        <li>Both country warehouses (Puerto Rico and USA) perform in a similar way and I don&apos;t observe any difference in customer destination.</li>
    </ul>
</div>
