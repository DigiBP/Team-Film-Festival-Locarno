# Team-Film-Festival-Locarno


# Clinical Trial Recruitment
A clinical trial is a research study conducted in human beings with the goal of answering specific questions about new therapies, vaccines or diagnostic procedures, or new ways of using known treatments. Clinical trials are used to determine whether new drugs, diagnostics or treatments are both safe and effective. Carefully conducted clinical trials are the fastest and safest way to find treatments that help people.

After researchers test investigational new therapies or procedures in the laboratory and in animal studies, those with the most promising possibilities are moved into human clinical trials. Clinical trials are broken down into different phases. During a trial, more and more information is gained about the potential treatment, its risks and how well it may or may not work, along with aspects related to quality of life.

Clinical trials are categorized as Phase I to IV trials. They are generally described as follows:

**Phase I (small number of participants, normally between 10-50 healthy volunteers, or very sick patients for whom treatment options are lacking)**

Phase I studies are designed to allow scientists and medical doctors to understand what effects an investigational compound has in human subjects. The goal is to study what happens to the compound in the body from a safety and tolerability point of view after it is swallowed, injected or infused. .Study participants are monitored for the occurrence and severity of any side effects that they may experience.

**Phase II (once the initial safety of the study drug has been confirmed in Phase I trials, Phase II trials are performed on larger groups of patients, generally 50-500 depending on the type of disease)**

Phase II studies are designed to begin to evaluate the safety and efficacy of an investigational medicine in patients, and often used to determine if different dosages of the treatment have different effects. The patients are given various doses of the compound and closely monitored to compare the effects and to determine the safest and most effective dosing regimen. In many instances, multiple Phase II studies are conducted to test the compound in a variety of patient populations or indications.


**Phase III (carried out on large patient groups, 300–3,000 or more depending upon the disease being studied)**

Phase III studies are designed to confirm the safety and efficacy of an investigational medicine. Large numbers of patients are generally involved in order to adequately confirm benefit and safety. These studies, as in the earlier phases, may involve one or more ‘treatment arms’, which allow for the safety and efficacy of the new investigational drug to be compared to other available treatments, or to be tested in combination with other therapies. Information obtained from Phase III studies is used to determine how the compound is best prescribed to patients in the future.

**Phase IV (also known as Post-Marketing Surveillance Trials)**

Phase IV studies take place after the medicine has received regulatory approval (market authorization) and are designed to provide broader efficacy and safety information about the new medicine in large numbers of patients, subpopulations of patients, and to compare and/or combine it with other available treatments. These studies are designed to evaluate the long-term effects of the drug. Under these circumstances, less common adverse events may be detected.

Therefore as we can clearly see there is a need for participants to be recruited for the Clinical Trials. 

# Team

Riad Beqiri, Janick Marti, Pawanpreet Kaur, Navneet Kaur

# Links to Deliverables

- [As-Is Process](https://github.com/DigiBP/Team-Film-Festival-Locarno/blob/main/Models/AS-IS%20DBP%20Clinical%20Trial%20Recruitment.bpmn)
- [To-Be Process](https://github.com/DigiBP/Team-Film-Festival-Locarno/blob/main/Models/BPM%20_Main.bpmn)
- [DMN Check out form](https://github.com/DigiBP/Team-Film-Festival-Locarno/blob/main/Models/Check%20filled%20out%20form.dmn)


# "As-Is Process"

![Project Documentation](https://github.com/DigiBP/Team-Film-Festival-Locarno/blob/main/Project%20Documentation/AS-IS%20Process.png)

**Black Box “Trial Participant”:** 
The participant is our external participant to our process and the key actor. 
The potential participant is aimed to be recruited for the clinical trial and most interactions are going to concern him/her.

**Black Box: “Doctor”:**
The Doctor is the one who will conduct a health check with the potential participant in order to manifest his eligibility for the clinical trial. He actually could be an internal participant but since the doctor is going to do the health check manually and we as HR Team do not actually know what and how it is going to be executed by the doctor we decided to keep it as a blackbox.

**Pool “Clinical Trial Department”:**
The Pool is the Clinical Trial Department which is responsible for all topics concerning Clinical Trials.

**Lanes “Human Resource Team”:**
Within the Pool we decided to have one lane (not fully necessary) to identify the specific team within the department. In our case it is the Human Resource (HR) Team which is responsible for the process. 

**Start Event “Filled out form”:**
The process starts when a potential participant fills out the form and sends it out. The current system notifies the HR Team via mail that the form is filled out.

**Manual Task “Check filled out form”:**
In this step, an HR Team member checks out the filled out form manually and compares it to the eligibility criterias. 

**Exclusive Gateway “Is the participant eligible?”**
According to the comparison of the eligibility criterias it is then decided if the potential participant is eligible for the Clinical Trial or not.

**Manual Task “Inform person”**
If the potential participant is not eligible to undergo the clinical trial then he will be informed by the HR team via telephone call.

**Manual Task “Contact Particpant”**
In this step the HR Team calls the potential participant and asks if he is still interested to participate in the Clinical Trial.

**Error Event “Particpant not interested”**
This occurs when the potential participant informs the HR Team during the Call that he is not interested anymore. If that is the case the recruitment process is ended.

**Manual Task “Schedule Doctors Appointment”:**
If the participant is interested in the Clinical Trial then the HR Team member asks the potential participant about his availability in order to schedule a doctors appointment. The Doctors Appointment is then going to be scheduled and entered in the calendar of the doctor.

**Event-based Gateway**
This gateway is always followed by catching message events from the doctor in which he confirms the status of the eligibility.

**Intermediate Catching Message Event “Not qualified”**
On this catching event the HR Team will receive a message from the doctor that the person is not qualified for the clinical trial and therefore the recruitment is going to be cancelled.
Intermediate Catching Message Event “Does not show up”
On this catching event the HR Team will receive a message from the doctor that the person did not show up for the clinical trial health check and therefore the recruitment is going to be cancelled.

**Intermediate Catching Message Event “Qualified”**
On this catching event the HR Team will receive a message from the doctor that the person is qualified to participate to the clinical trial. 

**Manual Task “Give further instructions”**
After the HR Team received the message that the participant is qualified they contact the participant and provide them further details to Clinical Trial. After this step the recruitment process is completed.

# Challenges:

Derived from the use case we have the challenge to really recruit the right people for the treatment. Further more it is mentioned to leverage the patients history and past trial results.
Thirdly there is currently a lot of manual work involved in the data collection and analysis.
The last point mentioned from the use case was that there is a need to improve data quality control by using digital data.

After talking to my friend which is an employee of an company executing Clinical Trials he stated that one key issue is really that there is no real pre-screening happening. Every potential participant is having a health check with the doctor so that they can guarantee their participation. But with the pre-screening in e.g. form of a google forms the “lazy” potential participant does not engage with the Trial and therefore stays away. Further more he states that they are still doing a lot manually without any automatization due to budget reasons. Therefore they have some assistants from HR which are executing all the steps manually.
Our Goal
By using service tasks and decision model logic our goal is to automate almost every step which is done from the HR team. Further more we want to establish a digital database in which all the participants (eligible) are stored even for future clinical trials so that we really ensure that the right people are recruited. What we want to cover but are not quite sure how we want to face this issue is the leveraging of the past trials results and the patients history.

# Methodologies
To develop a good project there is always the need of having good methods and tools.

Therefore we want to share with you what we used for what.

For the As-Is Process we decided to use Camunda Modeler to model a Business Process Model based on the opinion of employees from this field as well as from internet research.

For Decision Making Logic we used Camunda (DMN) and MAKE.

The Automatisation happened with MAKE and we integrated HubSpot for meeting scheduling.

# Risks 
Every project is connected to risks, so we decided to include 3 key risks in order to have them present and to prevent them:

![ProjectDocumentation](https://github.com/DigiBP/Team-Film-Festival-Locarno/blob/main/Project%20Documentation/Risks.png)
Accordingly we had a Risk Matrix with two high risks and one medium risk.
![ProjectDocumentation](https://github.com/DigiBP/Team-Film-Festival-Locarno/blob/main/Project%20Documentation/RiskMatrix.png)

# Data Privacy (Disclaimer):
For this project we are aware that the process is handling personal sensitive data according to the Federal Act on Data Protection (FADP). We are aware of the risks that could occur such as breach of secrecy, breach of confidentiality, violation of integrity and missing availability.

    Following definitions apply according to FADP Art. 3:

    a. personal data (data): all information relating to an identified or identifiable person;
    b. data subjects: natural or legal persons whose data is processed;
    c. sensitive personal data: data on:

        1. religious, ideological, political or trade union-related views or activities,
        2. health, the intimate sphere or the racial origin,
        3. social security measures,
        4. administrative or criminal proceedings and sanctions;
    
    d. personality profile: a collection of data that permits an assessment of essential characteristics of the personality of a natural person;
    e. processing: any operation with personal data, irrespective of the means applied and the procedure, and in particular the collection, storage, use, revision, disclosure, archiving or destruction of data;
    f. disclosure: making personal data accessible, for example by permitting access, transmission or publication;
    g. data file: any set of personal data that is structured in such a way that the data is accessible by data subject; …

Usually there should be the aim to avoid inappropriate handling of sensitive personal data and only use them under given consensus.

As we saw in the Lecture 7th Lecture of the Course Digitalisation of Business Processes we could have used Pryv to ensure the data pivacy and data protection.

Nevertheless we have decided to use Camunda, Make and especially Google Sheets with the argumentation that we are operating in a developing (DEV) environment with fictional data. 

# “To be process”:

This is the To be Process, our running BPM:

![Project Documentation](https://github.com/DigiBP/Team-Film-Festival-Locarno/blob/main/Project%20Documentation/To-be%20Process.png)

The first part of the BPM consists of two MessageStartEvents.

On one hand there's an automatic start event, which triggers when a google Forms Application is submitted. The Application Data is Saved as a File.  The Task GetApplicationData is invoked by a external Integromat Worker which subscribes to the task. Next, the Applications are evaluated and sorted into eligible and not eligible. This is done Via DMN:
![grafik](https://github.com/DigiBP/Team-Film-Festival-Locarno/blob/main/Screenshots/3.PNG)

For demonstartion purposes we defined three critical Attributes, which decide the eligibility. For this example Participants are only eligible, when they are between 20 and 40 years old, when they dont smoke and when they dont suffer from Diabetes.  Of Course these Rules change depending on the scope and subjet of the clinical trial. The DMN is modeled with the hit policy "unique", which means every possible Outcome has to be defined. The Output variable "Eligible" is saved in a separate file,the Eligibility List. Ontop of the elegibility, each participant is also assigned an ID in this file, which is implemented via Integromat.

The Make Application Looks like this:

![grafik](https://user-images.githubusercontent.com/115709906/209114343-cfa428d9-8328-488f-b263-beaba2af76c1.png)

A Watcher from Google Sheets looks for Changes in the Google Forms Response Sheet. As soon as a new Forms is filled out. The Startmessage event
 "Google" Forms will be activated by a Message Reuqest.


![grafik](https://user-images.githubusercontent.com/115709906/209115673-e645a4bd-769c-4cac-9447-046075005f55.png)



**Black Box “Trial Participant”:** 
The participant is our external participant to our process and the key actor. 
The potential participant is aimed to be recruited for the clinical trial and most interactions are going to concern him/her.

**Black Box: “Doctor”:**
The Doctor is the one who will conduct a health check with the potential participant in order to manifest his eligibility for the clinical trial. He actually could be an internal participant but since the doctor is going to do the health check manually and we as HR Team do not actually know what and how it is going to be executed by the doctor we decided to keep it as a blackbox.

**Pool “Clinical Trial Department”:**
The Pool is the Clinical Trial Department which is responsible for all topics concerning Clinical Trials.

**Lanes “Human Resource Team”:**
Within the Pool we decided to have one lane (not fully necessary) to identify the specific team within the department. In our case it is the Human Resource (HR) Team which is responsible for the process. 

**Start Events**

**Start Event “Filled out form”:**
The process starts when a potential participant fills out the Google Forms and submits it. 

**Service Task “Get Application Data”:**
In this step, an HR Team member checks out the filled out form manually and compares it to the eligibility criterias. 

**Data Object “Application Data”:**
…

**Business Rule Task “Decide if Eligible”:**
…
 

**Data Object “Eligibility List”:**
…

**Exclusive Gateway:**
… 

**Service Task “Contact participant”**
…

**Event-based Gateway**

**Intermediate Catching Message Event “Not qualified”**
On this catching event the HR Team will receive a message from the doctor that the person is not qualified for the clinical trial and therefore the recruitment is going to be cancelled.

**Intermediate Catching Message Event “Does not show up”**
On this catching event the HR Team will receive a message from the doctor that the person did not show up for the clinical trial health check and therefore the recruitment is going to be cancelled.

**Intermediate Catching Message Event “Qualified”**
On this catching event the HR Team will receive a message from the doctor with the report attached that the person is qualified to participate to the clinical trial. 

**Task “Give further instructions”**
…

#  Vision:

If we would have more time we would have enhanced the model and especially with additional tasks such as going after the potential participants which did not show up for the doctors appointment. 

In addition to that we could include more flexibility for drop outs during the recruitment process with an event subprocess i.e.: 

![](https://github.com/DigiBP/Team-Film-Festival-Locarno/blob/main/Project%20Documentation/FleixlbeEventSubprocess.png)

If we would want to switch then to the productive environment we would have to fulfill all the data privacy and data protection regulations in order to stay compliant.  In order to do this we should then switch to pryv or other tools supporting this. 
