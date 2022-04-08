# Election Audit Application
## Overview of Election Audit
A Colorado Board of Elections official has requested an application to automate elections audits after a recent local congressional election.  The requirements for the output are as follows:

1. Calculate the total number of votes.
2. Get a complete list of candidates who received votes and calculate the total number and the percentage of votes each candidate received.
3. Determine the winner of the election based on popular vote.
4. Calculate the total count and percentage of voter turnout by county
5. Determine which county had the largest number of voters overall
6. Output the results both to the terminal when the application executes and to a text file

The data source, election_results.csv, is a CSV file formatted as follows:
* Value 1 is a unique record identifier
* Value 2 is the name of the county where the vote was cast
* Value 3 is the name of the candidate for whom the vote was cast
* The field delimiter in the CSV file is a comma
* There is no text qualifier
* There are no blank rows in the file
    
## Audit Resources
* Software:  Python 3.9.7, Visual Studio Code 1.66.1
* Data source:  [election_results.csv](https://github.com/curt0230/election-analysis/blob/main/resources/election_results.csv)
* Data text file output:  [election_analysis.txt](https://github.com/curt0230/election-analysis/blob/main/analysis/election_analysis.txt)

## Audit Results
Final analysis of the election results shows that:

* The total number of votes was 369,711
* Three counties were included in the polling area:
    * Jefferson, which represented 10.5% of the total vote with 38,855 votes
    * Denver, which represented 82.8% of the total vote with 306,055 votes
    * Arapahoe, which represented 6.7% of the total vote with 24,801 votes
* Three candidates received votes:
    * Charles Casper Stockham, who received 23.0% of the total vote with 85,213 votes
    * Diana DeGette, who received 73.8% of the total vote with 272,892 votes
    * Raymon Anthony Doane, who received 3.1% of the total vote with 11,606 votes
* The winner of the election based on popular vote was Diana DeGette with 73.8% of the total vote, or 272,892 votes

Command output:  
![terminal_output.png](/resources/terminal_output.png)

## Audit Summary
Any collection of election results formatted in the same manner as the original source file can be analyzed using this script, including future elections for this district or elections in other districts where the results are reported at the county level.  The script could be modified to take in additional inputs, which would allow for scaling to both lower-level districts such as local school board elections or higher level elections such as those for federal congressional districts.  This type of modifiction would require collecting additional catagories that would then be added as key-value pairs in the dictionaries.  Then, data could be summarized to the various catagories and formatted sections for the new catagories could be added to the screen and text file outputs.

An additional metric of interest may be to output which candidate won each district individually.  This would be a small modifiction that wouldn't require additional inputs but might give candidates and their parties greater insight into which areas their campaigns were more or less effective and where they should focus their efforts for the next election.

