# A3: U.S. COVID Trends

## 1. Overview
In many ways, we have come to understand the gravity and trends in the COVID-19 pandemic through quantitative means. Regardless of media source, people are consuming more epidemiological information than ever, primarily through reported figures, charts, and maps.

This assignment is your opportunity to work directly with the same data used by the _New York Times_. While the analysis is guided through a series of questions, it is your opportunity to use programming skills to ask more detailed questions about the pandemic.

You'll load the data directly from the [New York Times GitHub page](https://github.com/nytimes/covid-19-data/), and you should make sure to read through their documentation to understand the meaning of the datasets.

## 2. Critical Analysis & Reflection: Before You Code
As you know, the first step in a data science project is to investigate the domain. Accordingly, please begin this assignment by carefully reviewing [New York Times GitHub page](https://github.com/nytimes/covid-19-data/) and
reading this [FAQ](https://www.nytimes.com/interactive/2020/us/about-coronavirus-data-maps.html) about the data. Working with _Data Feminism_ (Catherine D'Ignazio and Lauren Klein, 2020) and the _Envisioning Cards_, consider the following questions:
* What is the _New York Times_' goal?
* Where does the data come from? Is the data reliable?
* Who are the direct and indirect stakeholders?
* What values are implicated by this dataset and system?
* What issues related to "power" arise because of this dataset?

After reading and considering these questions, please provide written responses to these two questons:
* **R0a** Drawing on _Data Feminism_, the _Envisioning Cards_, and your study of the data, describe and discuss the _New York Times_' project. Discuss the social aspects of this project, focusing on stakeholders, values, and power.
* **R0b** Review the visualizations that are found at the bottom of this [FAQ](https://www.nytimes.com/interactive/2020/us/about-coronavirus-data-maps.html). Document two _important_ questions that a person living in the U.S. could answer with these visualizations. Discuss the importance of these questions.

Note: Please write your answers below under the heading "Your Responses and Reflections."

## 3. Coding and Critical Analyis & Reflect: While You Code

### Getting Started
You should start this assignment by opening up the `analysis.R` script. The script will guide you through an initial analysis of the data.

You will also find a file, named `rolling_windows.R`. Studing the code in the file will be helpful for some aspects of this assignment.

* **Coding prompts.** Complete the coding prompts in `analysis.R`.  Your goal is correct code that is readily understandable.
* **Reflection prompts.** Throughout the script, there are prompts labeled `REFLECTION`. Please write 1-3 sentences for each of these prompts below. Please strive for concise, clear, inclusive, and insightful writing. As appropriate, your writing should:
   - Provide evidence (e.g., facts from the datasets, points from the New York Times documentation, etc.)
   - Give justification for your opinions
   - Genuinely reflect on your views.  

## 3. Critical Analysis & Reflection: After You Code
**R6a** Consider the many visualizations that can be created with this data set (see [FAQ](https://www.nytimes.com/interactive/2020/us/about-coronavirus-data-maps.html)) for many examples, which in the next few weeks,
you will be able to create. Also, step back and reflect on the hard work that you have completed.

Now, drawing on _Data Feminism_ and/or the _Envisioning Cards_, comment on the importance of this data set. 

**R6b** Please briefly comment on one of these or similar questions:
* What, if anything, made you curious?
* What, if anything, surprised you about your R coding work?
* What might you do the same or differently on your next data wrangling project?

## Reflection Prompts

**R0:** Critical Analysis & Reflection: Before You Code
* **R0a** This project provides information on COVID-19, specifically tracking positive cases of COVID-19 in the United States as well as other countries. The data that the New York Times collects is meant to educate those examining the data on how the virus is spreading. The project uses data released by countries, counties, states, and health officials, where staff members of the New York Times work to verify this data. The New York Times has data on cases, deaths, hospitalizations, and test positivity which can all measure the spread of COVID-19. This data is helpful to people because it provides factual, detailed information about covid that is updated daily. This data is important as those using it will become more educated about the severity of covid and can educate others. Further, this data demonstrates which locations covid seems to be impacting more.
* **R0b**
   - Question 1: One question a person in living in the U.S. can answer using these visualizations is knowing how many current cases there are throughout the U.S. as well as seeing the percentage of current test positivity. This is important information for people to have access to because they can understand the current risk of contracting covid and plan their life accordingly. Also, people who know these statistics are more likely to understand how harmful covid is and has been over the past three years. People viewing this data can also see current hospitalizations, deaths, and I.C.U statistics which further educates people on how truly scary and harmful covid is, especially to certain populations.
   - Question 2: Another questions a person living in the U.S. can answer with these visualizations is recognizing how vaccinated one’s state is, as well as county. Further, people can better understand how certain communities are struggling to receive COVID-19 vaccinations, which is very important in order to understand the many inequalities different communities in America face. People can also compare the data on vaccinated states to levels of positive tests in each area to gain better insight on the benefits of getting a covid vaccination.

**R1:** Loading Data
* **R1a** The states, national, and counties datasets contains similar information regarding date, cases, and deaths. The states and counties datasets both contains a column of state names and fips, with the counties dataset also including names of counties. The national dataset only has columns including date, cases, and deaths. Further, the fips codes that are includes in the counties and states datasets are geographic indicators that make it easier for analysts to combine data.

**R2**: Exploratory Analysis
* **R2a** I learned that the state with the current lowest cases is actually American Samoa, which is a U.S. territory. This means that the states dataset also includes covid information on U.S. territories not just the 50 states.
* **R2b** The location with the most cases is not the same as the location with the most deaths. The location with the most cases is Los Angeles, and the location with the most deaths is New York, New York. The main reasons for this difference is that New York likely has a more diverse population including broader age groups and more at risk people. Further, New York may have had a harder time responding to the virus and therefore more difficulties for the people of New York to receive healthcare.

**R3**: Grouped Analysis
* **R3a** There are more than 50 observations in the lowest_in_each_state variable because it is possible that more than one county in a state had the same number of lowest deaths. Also, the counties dataset includes information on U.S. territories which would automatically cause more than 50 observations.

**R4**: Joins
* **R4.a** The source of the inconsistency would be between the counties dataset and the states dataset. This is because no inconsistencies were found in comparing the state totals to the national totals, however; inconsistencies were found in comparing counties and states. Information on county cases has not been recorded since May 13, 2022, so the inconsistency would have occurred before that date. By using this information we could further filter the data by date and continue checking for inconsistences until the date (or dates) is narrowed down.

**R5**: Independent Exploration
* No prompts

**R6**: Critical Analysis & Reflection: After You Code
* **R6a** This data set is extremely important for everyone to have access to. One significant reason for this is considering different political and social beliefs that have formed tension regarding COVID-19 and combatting it. Different people and groups have different beliefs concerning COVID-19, with some extremist groups even believing that this virus does not exist. I believe that this data set providing by the New York Times is extremely necessary as it is factual and unbiased data that showcases how damaging this virus has been. It is extremely important to have sources of information that are true in order to educate oneself and reject extreme false perspectives. Furthermore, these datasets are equally important for use in the future and for future generations. Having these datasets in the future will educate and remind people of the losses that occurred due to COVID-19 and hopefully help us learn from our mistakes.
* **R6b** I was very surprised about my ability to complete this R coding project. When I first started working on the 3rd and 4th sections of this project I was really lost and spent hours staring at my screen trying to figure out what to code. However, I realized a few days later when I looked at the prompts again that I could solve the questions, it just required me to relax and take a breath, which was very fulfilling.
