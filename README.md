Download Link: https://assignmentchef.com/product/solved-final-project-si507
<br>
<span style="font-size: 2.61792em; letter-spacing: -1px;">Project Overview</span>

The goal of the final project is for you to showcase what you’ve learned in 507 regarding:




<ul>

 <li>Accessing data via web APIs, including those that require authentication</li>

 <li>Accessing data via scraping</li>

 <li>Accessing data efficiently and responsibly using caching</li>

 <li>Using a database to store and access relational data</li>

 <li>Using basic python data structures and operations to analyze and process data in “interesting” ways</li>

 <li>Using unit tests to verify that data access, storage, and processing works as designed</li>

 <li>Using a presentation tool or framework to present data to a user</li>

 <li>Supporting basic interactivity by allowing a user to choose among different data presentation options</li>

</ul>




Here are a couple of examples that would be reasonable final projects:




<ul>

 <li>A program that lets a user choose a city and see the average ratings for different restaurant types (e.g., bar, breakfast, Indian, Mediterranean) from Google, Yelp, and OpenTable as plotly bar or scatter charts.</li>

 <li>A program that aggregates crime data from <a href="https://spotcrime.com/mi/ann+arbor/daily">https://spotcrime.com/mi/ann+arbor/daily</a> and allows a user to select one or more crime types to see a graph of crime frequency by month, either for a single year comparing across several years. Data is displayed using HTML tables within a Flask App.</li>

</ul>

<h1>Project Components</h1>

There are several components that your project must contain. Each of these are detailed in this section.

<h2>Data Sources</h2>

You must select data sources that, combined together, give you a “challenge score” of at least 8. Additionally, you must use <em>either </em>a Web API that requires authorization <em>or</em> a website where you crawl and scrape multiple pages as <em>one</em> of your data sources (these options are marked with ✣ below). Here’s how the scoring works:

<table width="656">

 <tbody>

  <tr>

   <td width="313">Data Source</td>

   <td width="197">Example</td>

   <td width="146">Challenge Score***</td>

  </tr>

  <tr>

   <td width="313">Web API you’ve used before</td>

   <td width="197">Twitter, iTunes, newsapi.org</td>

   <td width="146">2</td>

  </tr>

  <tr>

   <td width="313">Web API you haven’t used before that requires no authorization</td>

   <td width="197">Wikipedia, Google Books</td>

   <td width="146">3</td>

  </tr>

  <tr>

   <td width="313">Web API you haven’t used before that requires API key or HTTP Basic authorization ✣</td>

   <td width="197">Yelp Fusion, Open Movie Database</td>

   <td width="146">4</td>

  </tr>

  <tr>

   <td width="313">Web API you haven’t used before that requires OAuth ✣</td>

   <td width="197">Open Table, Reddit, Facebook, <a href="https://en.wikipedia.org/wiki/List_of_OAuth_providers">many more</a></td>

   <td width="146">6</td>

  </tr>

  <tr>

   <td width="313">Scraping a page/site you’ve worked with before**</td>

   <td width="197">nps.gov, si.umich.edu</td>

   <td width="146">1</td>

  </tr>

  <tr>

   <td width="313">Scraping a new single page**</td>

   <td width="197">So many!</td>

   <td width="146">4</td>

  </tr>

  <tr>

   <td width="313">Crawling [and scraping] multiple pages in a site you haven’t used before ✣</td>

   <td width="197">So many!</td>

   <td width="146">8</td>

  </tr>

  <tr>

   <td width="313">CSV or JSON file you haven’t used before with &gt; 1000 records</td>

   <td width="197">Dataset from <a href="https://catalog.data.gov/dataset?res_format=CSV">data.gov</a></td>

   <td width="146">2</td>

  </tr>

  <tr>

   <td width="313">Multiple related CSV or JSON files with at least one file containing &gt; 1000 records</td>

   <td width="197"><a href="https://www.kaggle.com/stackoverflow/pythonquestions/data">Python Questions from Stack Overflow</a></td>

   <td width="146">4</td>

  </tr>

 </tbody>

</table>







**: If you choose “scraping a new single page” you can only use this option for <em>one</em> of your project sources (i.e., you can’t scrape 2 pages you haven’t scraped before and count it as 8 challenge points).




***: The challenge scores listed here are a guideline, but specific sources may be determined to be more or less challenging depending on the details of the source and how you’re planning to use it.




✣: You <em>must</em> use at least one of these options as one of your data sources.




From each source, also need to capture at least 100 records (for CSV/JSON sources you need to capture at least 1000), and each record must have at least 5 “fields” associated with it.




If you have a source you’d like to use that you don’t think fits neatly into one of these categories, consult with your GSI.

<h2>Data Access and Storage</h2>

You will need to create a database to store your data. Your database must have at least two tables, and there must be at least one relation (primary key – foreign key) between the two tables.  Your data processing code (see below) must draw data from the database (i.e., not from the API/web page/CSV or from the cache).




If you are working with APIs or web pages you must <em>also</em> cache the raw results (JSON or HTML) you fetch from the source. Your code that writes data into your database must go through the cache when building the database.




As part of grading, we may use your code to rebuild the database (so this should be an option supported by your code) or ask you demonstrate this capability.

<h2>Data Processing</h2>

This is largely up to you, but you need to do whatever is necessary to support the data presentation(s) your program provides. This will probably involve things like creating dictionaries to collect sums or averages within a category (e.g., instances of crime by type, review scores by restaurant type).

<h2>Unit Testing</h2>

You must write unit tests to show that the data access, storage, and processing components of your project are working correctly. You must create at least 3 test cases and use at least 15 assertions or calls to ‘fail( )’. Your tests should show that you are able to access data from all of your sources, that your database is correctly constructed and can satisfy queries that are necessary for your program, and that your data processing produces the results and data structures you need for presentation.

<h2>Data Presentation</h2>

Use a tool or framework to present data to users on demand. The data should be presented in some way <em>other</em> than print( ) statements that output to the terminal. Your program must be able to produce at least 4 different graphs/displays/presentations. These can be different groupings of data, different graph types, or can differ in other ways (if you’re not sure if they’re “different” enough, check with your GSI).




The two options we cover in class that you are most likely to want to use include:




<ol>

 <li>Provide an interactive command line prompt for user to choose data/visualization options. Display selected graphs using plotly.</li>

</ol>




<ol start="2">

 <li>Create a Flask App that uses HTML links/form elements to prompt for the user to choose data/visualization options. Display selected data using HTML tables (or other elements, as long as the output looks good).</li>

</ol>




<ol start="3">

 <li>If you’re feeling ambitious, you can figure out how to use plotly with Flask.</li>

</ol>







If you wish to use a different data presentation approach, you should check with your GSI.

<h1>What to Submit</h1>

You will be submitting two key things: the project proposal, that will help us give you feedback if your scope needs adjusting, and the final code.

<h2>Proposal</h2>

Due Nov 19

Describe the idea of what you are going to do and list the data sources (tech points) you are going to use. Submit a half page to one page single spaced proposal describing your project plan. Your proposal should include:




<ol>

 <li>The description of what your program is intended to do. What is its purpose and who is it aimed at?</li>

 <li>The data sources you intend to use, along with your self-assessment of the “challenge score” represented by your data source selection.</li>

 <li>The presentation options you plan to support (what information are you intending to display to users).</li>

 <li>The presentation tool(s) you plan to use.</li>

</ol>







Your GSI will review your proposal draft and potentially provide feedback (if the proposal is fine, you may not get much feedback!).




After submitting your proposal, any significant changes (e.g., to data sources or presentation plans) will require submission of a Final Project Proposal Revision via Canvas. Follow instructions there for how to notify your GSI that you have submitted a revision. It is strongly recommended that you discuss any proposed changes with your GSI before submitting a revision.




If you change your proposal plan without submitting a revision and obtaining authorization, you risk losing lots of points on your final project grade.

<h3>Proposal Rubric (30 points)</h3>

<table width="624">

 <tbody>

  <tr>

   <td width="106"> </td>

   <td width="130">Poor</td>

   <td width="18"> </td>

   <td width="155">OK</td>

   <td width="43"> </td>

   <td width="134">Good</td>

   <td width="38"> </td>

  </tr>

  <tr>

   <td width="106">Data sources</td>

   <td width="130">Sources are not identified, or are described very poorly.</td>

   <td width="18">0</td>

   <td width="155">Sources are identified, but some information is missing</td>

   <td width="43">4-8</td>

   <td width="134">Sources are clearly identified, with URLs linking to a description of the source</td>

   <td width="38">10</td>

  </tr>

  <tr>

   <td width="106">Data source challenge score</td>

   <td width="130">Data source challenge score is not provided</td>

   <td width="18">0</td>

   <td width="155">Data source challenge score is provided by has errors or does not meet criteria (total &gt;=8)</td>

   <td width="43">4-8</td>

   <td width="134">Data source challenge score is provided, correct, and meets criteria</td>

   <td width="38">10</td>

  </tr>

  <tr>

   <td width="106">Presentation options identified</td>

   <td width="130">Not identified</td>

   <td width="18">0</td>

   <td width="155">Presentation identified, but are not clear, are not sufficiently different, or do not meet criteria (options &gt;= 4)</td>

   <td width="43">4-8</td>

   <td width="134">Presentation options are identified, different, and meet criteria</td>

   <td width="38">10</td>

  </tr>

  <tr>

   <td width="106">Presentation tools identified</td>

   <td width="130">Not identified</td>

   <td width="18">0</td>

   <td width="155">Tools are identified, but there are some issues with clarity.</td>

   <td width="43">4-8</td>

   <td width="134">Tools are identified and are appropriate</td>

   <td width="38">10</td>

  </tr>

 </tbody>

</table>

<h2></h2>

<h2>Final Project Submission and Demo</h2>

Due Dec 9




Via Canvas, You must submit a link to a GitHub repository containing your final submission. Your GitHub repo must contain a README.md file that gives an overview of your project, including:




<ul>

 <li>Data sources used, including instructions for a user to access the data sources</li>

 <li>Any other information needed to run the program (e.g., pointer to getting started info for plotly)</li>

 <li>Brief description of how your code is structured, including the names of significant data processing functions (just the 2-3 most important functions–not a complete list) and class definitions. If there are large data structures (e.g., lists, dictionaries) that you create to organize your data for presentation, briefly describe them.</li>

 <li>Brief user guide, including how to run the program and how to choose presentation options.</li>

</ul>




Your GitHub repo must <em>also</em> contain a requirements.txt file that can be used by the teaching team to set up a virtual environment in which to run your project.




<strong>Do <em>not</em> check in any private or secret information (e.g., API keys, passwords), but if you are using an API that requires authentication, please submit authentication information through canvas so that we don’t have to apply for an account. </strong>

<h2>Demo Sessions</h2>

You will sign up to give a short (&lt; 5-minute) demo to your GSI, following a script that we will provide as the deadline approaches. We are planning to hold demo sessions during the class and discussion session at the last week of class (Week of Dec 9). You will get notified if we decided to change the form of demo. Note that the project is due at 11:59pm on Monday, 12/9, so you should have your project finished by the Tuesday morning class.




If you are unable to attend a demo session during the scheduled times, please contact the teaching team as soon as possible to make alternative arrangements.

<h3></h3>


