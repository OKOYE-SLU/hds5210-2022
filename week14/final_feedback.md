# Feedback on Final

Overall, I think you did a good job demonstrating most of the skills we learned this semester.
1. You hit a challenge in the first step, reading your JSON file into a data frame. One thing to remember is that Pandas can actually read JSON in specific formats.  In this case, your JSON is a list of dictionaries -- Pandas can read this with `pd.read_json(file)` directly.  No need to iterate through the way you were trying. 
 * The reason you got an error is because not every entry in your JSON had a value for the shortInt attribute.  So, when you said `price[i]['shortInt']` and there was no `shortInt` attribute for that item, Python complained.  If you wanted to safely do this the way you tried, then `price[i].get('shortInt')` would have worked and returned `None`
2. I didn't understand the use of the `insurance coverage` column and how you used that to join the data together at the end.  It looks like that was used just as a way to join the data, but didn't really mean anything.
3. The project asked you to use functions to modularize your code. You did this in one place, but not generally.

Nice work finishing up the semester.

* Data Access and Formats (5): 5
* Data Merging (5): 2
* Data Aggregation and Pivoting (5): 5
* Data Transformation (5): 5
* Data Visualization (5): 5
* Problem Applicability (5): 5
* Modularity / Style (15): 10
* Documentation and Processionalism (15): 15
