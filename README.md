# Python_Data_Project_Nutritionix_API
BeautifulSoup (Web-scraping), Request(API calls), Pandas, and Numpy Used for This Project.


![Project1_IMG1](/Project1_IMG1.jpg)

Import pandas (data frame), requests (request API and get a response), BeautifulSoup (webscraping), numpy (data manipulation)

The first function TopRest_Menu gets urls, name parameters.
This function basically parser HTML to get menu name from different stores in YELP.
It returns menu name.
Menu_Price function is same, but parser HTML to get menu's price.
It returns price of the menu.

![Project1_IMG2](/Project1_IMG2.jpg)

Adds two returns (menu name, price) into data frame 1.

![Project1_IMG3](/Project1_IMG3.jpg)

API_Query function accepts query_food parameter which has the name of menu on the data frame 1.
This function has api_id, api_key given by Nutritionix API.
The function returns the result of the query in a JSON (JavaScript Object Notation) format.

![Project1_IMG4](/Project1_IMG4.jpg)

API_Analysis function accepts foods, price from the data frame 1.
Name is used for querying the nutritional facts to the API.
Inside the function, it has several nutritions lists but empty because it will be appended by each iteration in a for-loop. Also, calories per gram does not exist in the API, but I made a formula using Numpy.
Then, there is another for-loop iterations to add price in the each list.
After all, this functino returns another data frame (data frame 2)

![Project1_IMG5](/Project1_IMG5.jpg)
Unfortunately, the API has a limitation because I am using a developer mode for free. API calls cannot exceed over 200. Thereby, I limited the number of parameters in the list before querying the API call.

![Project1_IMG6](/Project1_IMG6.jpg)

I created the other data frame to merge into one from data frame 1 and data frame 2.
Then, I also dropped duplicated foods name.

![Project1_IMG7](/Project1_IMG7.jpg)
Then, df3.describe() executed and shows a meaningful analysis result.
df3.to_csv('df3_csv) lets the data frame 3 to be saved as a csv file.

This project can be utilized by health professionals to advise their patients for diet to warn how dangerous fast food is. Also, individuals who are interested in diet can utilize this analysis.
