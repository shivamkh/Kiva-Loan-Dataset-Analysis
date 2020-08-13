# Kiva-Loan-Dataset-Analysis
This is case study for Kiva Loan dataset done in Tableau 
1 Introduction
Kiva is the non-profit organisation that gives funds to people in the low-income countries (like the
students and entrepreneurs). Anyone can lend their money to the people (Crowd funded) in need as a
loan and later stage once the borrower repays the loan the donor can lend their money to new loans
or they can take back as per their requirement. Kiva manages this with filed partners and money
taken as an interest from the borrower is used in managing field partners.
This work focuses on analysing the Kiva loan dataset and focuses to answer the below questions:
1. Loan analysis based on gender
 most represented gender (gender prevalence in funded loan amounts as per
countries).
 repayment interval
2. Comparing loan amount for selected group of countries and comparing it to global trend.
3. How loan amounts are distributed by the sector Globally and for selected countries?
2 Data
The dataset for this visualisation is used from the Kaggle competition as there is some error while
trying to download from kiva.org directly. It contains 20 columns which provide whole lot of information
to analyse the loans given from kiva in detail. The main fields that are used while creating the
visualization are described below:
 Country -> Categorical variable: It gives the list of countries where loan is provided by kiva.
 borrower_gender -> Categorical variables: It specifies the gender of the borrower.
 repayment_interval -> Categorical variable: information about the status the loan is being
returned.
 funded_time -> Quantitative and continuous variable: The time at which the loan posted
to
 Kiva gets funded by lenders completely.
 loan_amount -> Quantitative and continuous variable: The amount disbursed by the field
agent to the borrower (USD).
 Sector-> Categorical variable: These are the major sectors in which the kiva is helping
people to support their requirements.
Other data fields also used to process the data to make the data usable as per the need of the
visualisation. There are many data fields in data which need the pre processing before they can be
used in the visualization. The pre-processing is done in the Tableau using the creating calculated
features and changing the data types of the fields.
The dataset contains good mixture of quantitative and categorical variables which makes it a complex
dataset to analyse. The fields contain the information encoded in complex way which is needed to be
decoded to use them for this visualisation for example the borrowe_gender field contains the
information in form of a list of words male and female (female, female, female, male). I wrote the logic
to convert this field in four categories male, female, both gender and no data. Similarly, date field is
given in string format which is needed to be converted in the Date and time field to utilize it in the
visualisation.
3 Tasks
Locate: The countries are located on world map where kiva is providing the loans. The map is filled in
accordance with the prevalence of the gender taking the loan.
Compare: Examining the similarities and dissimilarity between the loan amount provided to different
countries and different world regions. Also comparing the loan amounts globally and selected regions
based on the sectors and genders of the people the loan is provided to. 

4 Visual Encoding
Colour: Colour is used to encode the gender information.
Purple colour in the map shows the female gender and blue colour shows the male gender.
Green colour in the stacked bar chart for different sectors and the area chart comparing the sum
of loan amount given to different countries represent the element in sets. This set contains the
countries selected by the user and green colour shows the data for the countries in this set and
grey colour shows the data for the countries outside the set.
Brightness: The gender data is provided in a complex way and different countries have the
varied combination of male and female gender. So, I have encoded male as -1 and female as 1
and then averaged the quantities to get the prevalence of the gender for the country. So, the
country where there is the female dominance of borrowers like India those regions have darker
shades of purple colour and the regions having male prevalence have dark shade of blue while
other lighter shades of blue and purple shows the difference in prevalence of genders of the
borrowers in these regions like china has the lighter shade of blue as in china there is slight
prevalence from female borrowers.
5 Design
The visualization is divided in 5 parts where main controller for this visualisation is the world map from
where you can select particular country or the group of countries for which you want to compare the
gender prevalence and all the other features.
The pie chart is giving the information of the loan borrowers based on gender and it is selected as we
are describing the percentages of the loan borrowers and we have only 4 categories to compare
between hence the drawbacks of the pie chart can be neglected as it causes problem in case of large
number of categories which is not the case.
The repayment interval is comparison between the different statuses of the people when they are
returning their loans there are four categories, so I have used the stacked bar chart which shows the
percentages of the people from different genders in each status. This clearly helps to distinguish
between different statuses of people while returning the loan. This information can be used to study
the behaviour and situation of the people in these regions and they can be helped accordingly by
designing their interests and returning period of loan accordingly. Comparison using stacked bar chart
is easy as compared to combined one.
One more stacked bar chart is used to compare the loan amounts between the different sectors It is
interesting to notice that the agriculture is the most prevalent between the different countries which
seems fair as most of the countries are poor and people are working in agriculture sector. This chart
is also in coordination with all the other charts such that the sectors in this chart can be used to
increase the granularity to observe the detailed with all the other observations as well.
The area chart is used to compare the sum loan amounts for the individual country and set of
countries. I am creating a set in a way that the countries which are selected by the user becomes the
element of the set and the other countries will not be element of set and hence colour encoding is
applied accordingly.
I have added the links in the visualisation to explore the how the kiva as a organisation works. When
the user selects the country there is the link provided in the information section with the name of
country that redirects user to the page where the information is provided for current funding options is
available.
Strength:
This visualization provides the information to comprehend the gender prevalence and comparing the
sum of the loan amounts based on sectors and gender of people in detailed manner.
The visualisation is interactive it provides user the opportunity to explore the data as per requirement. 

This visualisation is scalable in the sense that data from the organisation site and can be attached
with the current visualisation and it will provide the exploration tool immediately.
Weakness:
I have used the limited visual encoding techniques to make the visualisation clear enough but more
visual encoding methods can be explored.
6 Links:
Data Source: https://www.kaggle.com/kiva/data-science-for-good-kiva-crowdfunding#kiva_loans.csv
References
[1] "What is Exploratory Data Analysis", [Online] https://towardsdatascience.com/exploratory-dataanalysis-8fc1cb20fd15
[2] "Data Science for Good: Kiva Crowdfunding", [Online]
https://www.kaggle.com/mrjezy/exploratory-data-analysis-of-kiva-loans 
