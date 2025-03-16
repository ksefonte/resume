# Portfolio Projects
## Freight Monitoring for Team Global Express | 2024 - 2025

#### Problem Statement/Challenge:
- Team Global Express provides a web interface (ASP.Net) allowing customers to download reports pertaining to fees,delivery KPIs (DIFOT) and volume. These reports are capped to 1-month increments and presented in .PDF or .XLS formats with images embedded. Navigating this space is necessary for users to maintain daily visibility over their business, but it is cumbersome and prohibitive for any large scale data analysis. The goal was to retreive all of the necessary data from TGE and use it to make inferences about short term and long term delivery trends.

#### Scope of Work:
- End to end design, implementation and operation once deployed. Updating the code, debugging and providing user-experience improvements as needed.

#### Team Size and Collaboration:
- Sole developer, collaborated with other teams to fine-tune metrics displayed to users, provding meaninful output.

#### Tools and Environment:
- Python(ScikitLearn,Pandas,BeautifulSoup), SQLite, Git

#### Key Contributions:
- Investigated TGE web app, uncovering URL-based authorisation headers that could be used to programatically iterate through report endpoints.
- Developed webscraping functions to iterate through different reports for a variable date range above the 30 day limit.
- Built ETL pipeline with local SQLite database to de-duplicate and store data provided by the webscraping functions.
- Implemented ML (Random Forest) model trained on historic data,  used to provide a 'Real' ETA estimate for packages.
- Integrated daily results reporting with Slack for easy access by the wider team, providing a list of outstanding consignments flagged as 'late' according to RF model. Secondary webscraping functionality to provide further fields as necessary for late orders.

#### Metrics and KPIs:
- Reduced need for manual report compilation daily for 1-33 staff members, saving an estimated 5 hours a week.

#### Learning and Development:
- Learned how to use a webscraping library (bs4)
- Learned how to implement SQLite database with high volume I/O during webscraping activities.

#### Stakeholders and Impact:
- Internal stakeholders noted time saved on tracing day to day packages
- Secondary field-extraction via BS4 exposed an increase in freight consignments impacted by uncharacteristic (slow) handling behaviours, leading to an investigation by the customer into the service provider.