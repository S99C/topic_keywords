# Topic Keyphrases <br>
A repository for extracting most recent and relevant keyphrases for input topics.

## Requirements<br>
1. Get topic inputs from user [Required].
2. Get the top number of url to fetch per topic from SERP result. [Required]
3. Scrape them 
4. Fetch the top 'n' keyphrases from it.
5. Save the result in a file.

## Solving approach <br>
1. Read input from user using an excel file for topic and number of urls to fetch.
2. Use googlesearch module to get the SERP results for those topics and store them in a Data Frame.
3. For each url, request the page and store them as an BeautifulSoup object.
4. Invoke TextRank model from "pke" module and use that on the concatinated text (content of all the result join as a single text) and fetch top "n" keyphrases (default using -20, can be changed).
5. Save the output keyphrases with score into an excel file.

## User Manual<br>
### Steps
1. Clone this repository and create a new virtual environment.
2. Activate the virtual enviromnent.
3. Install all the dependencies using ```pip install -r requirements.txt```.
4. Input the topics and respective url fetching count in the "Output Dashboard.xlsx" file in "topics" and "Number of Results" column and save the file, do not close it at this stage.
5. Open the "input.xlsx" file, update and save it and you may close both files now.
6. If any confusion persists, you may follow the brief video description.

https://user-images.githubusercontent.com/79993232/138594617-dfec414a-f814-4de3-9e4e-f8d0c4ce7e55.mp4

5. Open the "experiments.ipynb" file in the same directory and click on "Run All" and wait for the program to compute and write to "output.xlsx" file in the same directory.

7. Once all the cells have run and "output.xlsx" has been generated you can open and visulize the keyphrase and check their scores in any spreadsheet handling software like MS Excel from the "Output Dashboard.xlsx" file.

<img width="946" alt="data_dash" src="https://user-images.githubusercontent.com/79993232/138594796-10c76e82-6342-4e5a-805a-41ef6f282ba1.PNG">

## References
1. [PKE module documentation](https://boudinfl.github.io/pke/build/html/index.html)


