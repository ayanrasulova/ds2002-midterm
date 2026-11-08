1. Data Quality Impact

Q: Describe a specific data quality issue you encountered in the supplied data. How did your cleaning decision change the outcome of your analysis? What would have happened if you had not caught it?

One data quality issue we found was that strawberry pop tarts appeared under four different SKUs, which were PT-12, SKU#459812, POPTART-STRAW, and PT_STRAWBERRY. We mapped these to the single canonical SKU PT-12, which let us analyze the sales together. The consolidated total was 5,198 units rather than treating the product as four separate items. This was able to change the outcome of the analysis as  a report focused on just one SKU could have missed sales recorded under the others, the demand look much lower and potentially leading to too little stock being ordered because of the initial misleading data

2. ETL Trade-offs

Q: You made choices about how to standardize SKUs, handle missing timestamps, and join weather data. Pick one decision and explain: what alternative approach could you have taken, and how might it have changed your results?

We chose to interpret transaction timestamps as Eastern time then convert to UTC for alignment with the weather data while keeping sales grouped by their local Eastern calendar date. An alternative approach we could have done would be grouping the sales by UTC dates instead, but that would shift some later timestamped Florida transactions into the next day, which would have made the daily sales totals less accurate and perhaps cause the sale spikes to misalign with the weather that was recorded for that day

3. Pipeline Trust

Q: The Walmart CDO argued that the biggest risk is not the model — it is the pipeline. Based on your experience in this project, do you agree or disagree? What was the most fragile part of your data pipeline?

A: W'd agree with the CDO. Our models were relatively simple, so nearly every way we could have gotten a wrong answer came from the data feeding them. The most fragile part of our pipeline was most likely category standardization, because it relied on rules we wrote by hand and only caught the variants we knew to look for. As a result, our Question 5 analysis filtered on "Entertainment" alone and left out 1,062 board game and playing card units, about 25% of the category. The gap was small this time, but nothing in the pipeline flagged it, and the same  miss could change a stocking decision on another dataset or store with more in that category. If we did this again, we would fix labels once in the cleaning step and check every category against an approved list, so an unknown label would stop the notebook instead of quietly dropping sales.

4. Business vs. Data

Q: For Question 5 (board games), your team had to make a recommendation with imperfect data. How did you weigh statistical evidence against business risk? Would you have decided differently with more time or more data?

5. Team Collaboration

Q: How did your team divide the work? What would you do differently if you had another week? What was the most valuable skill each team member contributed?

A: We were able to divide up the work effectively by communicating at the start of the project who would take ownership of which parts, which helped out a lot because we all had an idea of what to work on. We also created a group chat where we were able to have consistent communication and help each other out if needed. I think each group member was able to contribute flexibly according to their availability for that week, which made it much easier to coordinate and manage the project as a whole.
