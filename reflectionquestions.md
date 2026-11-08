1. Data Quality Impact

Q: Describe a specific data quality issue you encountered in the supplied data. How did your cleaning decision change the outcome of your analysis? What would have happened if you had not caught it?

One data quality issue we found was that strawberry pop tarts appeared under four different SKUs, which were PT-12, SKU#459812, POPTART-STRAW, and PT_STRAWBERRY. We mapped these to the single canonical SKU PT-12, which let us analyze the sales together. The consolidated total was 5,198 units rather than treating the product as four separate items. This was able to change the outcome of the analysis as  a report focused on just one SKU could have missed sales recorded under the others, the demand look much lower and potentially leading to too little stock being ordered because of the initial misleading data

2. ETL Trade-offs

Q: You made choices about how to standardize SKUs, handle missing timestamps, and join weather data. Pick one decision and explain: what alternative approach could you have taken, and how might it have changed your results?

3. Pipeline Trust

Q: The Walmart CDO argued that the biggest risk is not the model — it is the pipeline. Based on your experience in this project, do you agree or disagree? What was the most fragile part of your data pipeline?

4. Business vs. Data

Q: For Question 5 (board games), your team had to make a recommendation with imperfect data. How did you weigh statistical evidence against business risk? Would you have decided differently with more time or more data?

5. Team Collaboration

Q: How did your team divide the work? What would you do differently if you had another week? What was the most valuable skill each team member contributed?

A: We were able to divide up the work effectively by communicating at the start of the project who would take ownership of which parts, which helped out a lot because we all had an idea of what to work on. We also created a group chat where we were able to have consistent communication and help each other out if needed. I think each group member was able to contribute flexibly according to their availability for that week, which made it much easier to coordinate and manage the project as a whole.