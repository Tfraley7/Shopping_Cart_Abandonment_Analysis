

<body>

<h1>Shopping Cart Abandonment Analysis & Machine Learning Model Report</h1>

<h2>Executive Summary</h2>
<p>This report provides an in-depth analysis of shopping cart abandonment trends using transactional data and predictive modeling. The goal was to identify key abandonment patterns, estimate revenue loss, and develop a machine learning model to predict abandonment likelihood. The findings provide actionable insights to help reduce cart abandonment rates and improve conversions.</p>

<h2>Key Findings from Data Analysis</h2>

<h3>Abandonment Overview</h3>
<ul>
    <li><b>Total Sessions:</b> 884,474</li>
    <li><b>Total Abandoned Sessions:</b> 90,424</li>
    <li><b>Abandonment Rate:</b> 10.22%</li>
    <li><b>Revenue Lost Due to Abandonment:</b> $16,472,644.30</li>
</ul>

<h3>Abandonment by Price Range</h3>
<p>Price ranges $200-$500 had the highest abandonment rate. Lower-priced products (e.g., $0-$20) had relatively fewer abandoned sessions.</p>

<h3>Abandonment by Product Category</h3>
<p>Electronics and Computer Components were among the most frequently abandoned categories. Categories with high-value items showed higher abandonment trends, indicating possible hesitation due to cost.</p>

<h3>Session Behavior and Abandonment</h3>
<p>Longer session durations correlated with higher abandonment rates, suggesting users hesitate or get distracted. High interaction counts (views, cart additions) without purchases were strong indicators of abandonment.</p>

<h2>Machine Learning Model Development</h2>

<h3>Data Preparation & Feature Engineering</h3>
<p>To develop a predictive model for abandonment, the dataset was transformed from an event-level structure to a session-level dataset with aggregated features:</p>
<ul>
    <li><b>Session Duration:</b> Total time spent in a session.</li>
    <li><b>Num Events:</b> Total user interactions within a session.</li>
    <li><b>Num Products Viewed:</b> Unique products viewed.</li>
    <li><b>Num Cart:</b> Number of items added to the cart.</li>
    <li><b>Num Purchases:</b> Number of completed purchases.</li>
    <li><b>Target Variable:</b> Abandoned = True if the session contained cart events but no purchase event.</li>
</ul>

<h3>Model Selection & Training</h3>
<p>Random Forest Classifier was selected due to its ability to handle structured data and extract feature importance.</p>
<ul>
    <li><b>Train/Test Split:</b> 80% training, 20% testing.</li>
    <li><b>SMOTE (Synthetic Minority Oversampling):</b> Used to balance the dataset due to class imbalance.</li>
    <li><b>GridSearchCV:</b> Used for hyperparameter tuning.</li>
</ul>
<p><b>Best Parameters Found:</b> max_depth=30, min_samples_split=2, n_estimators=200</p>

<h3>Model Evaluation</h3>
<ul>
    <li><b>Accuracy:</b> 97%</li>
    <li><b>Precision for Abandonment Prediction:</b> 55%</li>
    <li><b>Recall for Abandonment Prediction:</b> 92%</li>
</ul>
<p>Feature Importance Analysis:</p>
<ul>
    <li>Num Cart – Strongest indicator of abandonment.</li>
    <li>Session Duration – Longer sessions correlate with higher abandonment.</li>
    <li>Num Events – More interactions without purchases indicate hesitation.</li>
    <li>Num Products Viewed – High browsing without commitment suggests indecision.</li>
</ul>

<h2>Business Recommendations</h2>

<h3>Reducing Cart Abandonment</h3>
<ul>
    <li>Target Price Ranges $200-$500: Implement time-limited discounts or installment payment options.</li>
    <li>Intervene in Long Sessions: Introduce chatbot assistance or personalized recommendations.</li>
    <li>Streamline Checkout: Reduce the number of steps to complete a purchase and enable guest checkout.</li>
</ul>

<h3>Leveraging Predictive Model</h3>
<ul>
    <li>Real-time Abandonment Alerts: Use the model to flag high-risk sessions and trigger personalized offers.</li>
    <li>A/B Testing on Cart Interventions: Test different strategies (discount pop-ups, urgency timers) to improve conversions.</li>
    <li>Optimize Marketing Efforts: Retarget users who abandon carts with personalized follow-ups.</li>
</ul>

<h2>Conclusion</h2>
<p>This study successfully analyzed shopping cart abandonment trends and developed a machine learning model that predicts abandonment with high accuracy. By leveraging these insights, businesses can implement targeted strategies to reduce abandonment rates and recover lost revenue.</p>

<p><b>Next Steps:</b></p>
<ul>
    <li>Integrate the predictive model into live session tracking.</li>
    <li>Continuously refine features and hyperparameters for improved accuracy.</li>
    <li>Implement business interventions and measure their impact on conversion rates.</li>
</ul>

<h2>Appendix (Supporting Data & Visuals)</h2>
<ul>
    <li>Detailed Abandonment by Price Range (Table)</li>
    <li>Top Abandoned Product Categories (Table)</li>
    <li>Session Duration vs. Abandonment Trends (Chart)</li>
    <li>Feature Importance Chart from the Model</li>
</ul>

</body>
</html>
