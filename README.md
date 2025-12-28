# Sports Reference Matrix
Matrix for Engineering Internship Prompt


**Project Logic:**
This script processes team-record data and generates a matrix showing how many times each team (rows) defeats its opponent (columns).

The challenge of this project was converting a nested dictionary into a pivot table (matrix).

I used a nested 'for' loop to traverse the provided JSON. This transformed the data into a list of flat records so I could leverage the pandas library's '.pivot()' function to reshape the data. This allowed each unique team to serve as both a row and a column header. I cast the win counts to an integer instead of a float for a cleaner visual. Additionally, because teams do not play themselves, I used '.fillna('--')' to preserve the visual style specified in the prompt. I had to map an object to ensure the dataframe could support both numeric and the '--' character for terminal display. 


For simplicity, I kept the output in the terminal. 

**Prerequisites:** Ensure Python 3 and the Pandas library are installed.
```
bash
pip install pandas

```
**Execution**: Run the script from your terminal to see the formatted matrix:
```
bash
python sports_reference.py
```
