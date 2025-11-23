# Meeting Notes 2025/9/5

*Initial Meeting, concept discussion*  
*700pm\~800pm Friday*  
*All members present*

Idea Discussion  
Athletics analyze \-\> advice

- AI or mapped approach  
- Collect data from various sources, and then create advice based on data  
- Computer vision related topics somewhat veto’ed due to concerns on data processing

KYC concept

- Conflicts with Johnny’s ongoing work

Criteria to avoid

- Ideas where quantity/complexity of work comes from outside of software engineering  
  - Ex. manual data processing required  
    - Heavily applies to many vision-based AI ideas  
  - Ex. excessive subject matter research  
- Not enough work for 5 people  
- Excessive imbalances in subject familiarity/passion  
  - May lead to group friction, issues of dependence on one member

# Meeting Notes 9/7

*Project Selection*  
*500pm\~630pm Sunday*  
*All members present*

**Goal**: Discuss previously considered ideas, vote for an idea topic

Discussion

- Everybody looked over all SE proposals in the provided list  
- Justin expanded on his original swimming idea  
  - Some existing datasets  
- Some discussion on suitability of swimming idea

Considered ideas:  
3\. Prism-AI  
8\. Crazy eights  
10\. Mixed Reality  
11\. Learning platform w/ eye tracking  
12\. OCD data analysis  
21\. Large event management platform  
25\. Cattleytics   
\* Swim analytics, training recs

Voting initially on any number of choices-  
Tie between 10, 12

Redid voting, only 3/5 people voted for most voted

Voted, 2 choices per person  
Reults:   
3\. Prism-AI   **1**  
8\. Crazy eights **0**  
10\. Mixed Reality **2**  
11\. Learning platform w/ eye tracking **0**  
12\. OCD data analysis **4**  
21\. Large event management platform **2**  
25\. Cattleytics **0**  
\* Swim analytics, training recs **2**

- Selected OCD data analysis platform  
- Finished group creation and project selection on gitlab

# Meeting Notes 9/18

*TA Meeting \#1*

**Notes**  
Begin: We show overview of our documents, Zhenia gave a quick verbal overview of the motivations from the MSE’s side for our project.  
Question 1: Our case is somewhat unique, integrating with an existing MSE monorepo

- Issues with deployment for MSE side,  
- Issues with potential difficult for grading and contribution measuring

Solution 1:

- Submodule our development  
- Issues with integration with their existing CI  
- Current plans: Discuss further with supervisor (Luke)

TA Suggested approach:

- Documentation only in our own repo, code all in MSE monorepo  
  - Potential difficulty in that project must succeed for integration with MSE repo  
- Overall best solution so far

Question 2: Any common misinterpretations of requirements from other groups we should be aware of?  
Answer 2: 

- Double check that checklist exists in document  
- We need to identify risks to project: not in sense of concrete risk of the software  
  - Risk in terms of completing the project/working as a team  
  - Is there some minimal MVP risk that if not completed will make the project mostly meaningless  
  - We should mitigate/address/solve the risk as part of MVP (PoC) to show project viability  
    - Zhenia suggests local implementation MVP  
    - Michael suggests basic boilerplate app/ui with integration with MSE monorepo  
      - Project business logic is lower risk afterwards  
    - Johnny suggests risk to be addressed as extracting text from receipts as part of our unique functionality

Question 3: Where should we be in terms of progress?  
Answer 3: Focus and progress should be on the upcoming due document

- Not so bad right now, requirements harder later  
- Focus on the current deliverable document  
  - But also don’t get too distracted by documentation  
    - Starting implementation earlier is good and important  
    - Iterative process, remember, not waterfall  
    - Particularly because existing code/technology we need to integrate with, our requirements must partially depend on existing implementation

Question 4: How do we get good grades in this course, particularly about documentation  
Answer 4: In general, feedback is harder/more thorough in revision 0, but marks are more weighted towards revision 1\.

- If TA sees that we implemented changes from revision 0, very easy to get good marks in revision 1  
- As long as everyone on the team is involved, and making progress on the docs, marks will be good  
- Need to come prepared with something to show for each meeting  
  - As long as contribution is shown from each team member at regular meetings, marks will be good

Question 5: Hypothetical already good implementation and results by january, what happens for rest of time till april?  
Answer 5: Stretch goals always exist, still documentation to write, testing procedures/results to do

Question 6: Pairing with other groups?  
Answer 6: Yes, peer reviews, after documentation is submitted

- We review documentation of other groups, and create 5 github issues on their repo  
- Zhenia suggests doing iwth other MSE capstone groups  
  - TA agrees as good idea  
    - Dr. Smith seems to lean towards this as well  
- Need to implement some other groups modules

Question 7: Reimbursement workings  
Answer 7: Reminder of allocated $125 budget, and likely reimbursed at start of the next term

Meeting Notes 9/26  
*Meeting with MSE representative, technical discussion*

**Notes**  
Questions:

1. Tech stack  
2. Repo walkthrough and how monorepo is organized  
3. How are github actions setup and ci/cd in general  
4. How is development progress tracked?  
5. How is testing validated  
6. How do deployments to production work with the existing cloud hosting  
7. How do we get access to databases, etc, necessary to start development  
8. Database schema documentation

Answers:

1. [https://github.com/McMaster-Engineering-Society/Documentation/blob/main/MESInfratechGuidebook.md](https://github.com/McMaster-Engineering-Society/Documentation/blob/main/MESInfratechGuidebook.md)  
   1. ^Internal documentation  
   2. Existing database is MongoDB  
2. [https://github.com/McMaster-Engineering-Society/Documentation/blob/main/RepoSetup.md\#folder-structure](https://github.com/McMaster-Engineering-Society/Documentation/blob/main/RepoSetup.md#folder-structure)  
   1. ^ More internal documentation  
3. .  
4. Kanban board:  
   1. [https://github.com/orgs/McMaster-Engineering-Society/projects/15/views/1](https://github.com/orgs/McMaster-Engineering-Society/projects/15/views/1)  
5. Testing consists of testing code locally   
   1. (with screencapture recording?)  
   2. Development preview for production  
6. Our capstone team will have a staging branch within the monorepo, which will be pr’d into the main staging and then prod when needed  
7. Postgres database, we setup our own systems  
   1. MSE owns production database  
8. No documentation, so shown: Existing db is mongoDB document based  
   1. Most relevant part to our project is user profiles  
      1. Role-based access, list of assigned roles per user

Additional information:

- There are pre-styled react components available for us in the monorepo  
  - Allowed to add, do not change/remove from them  
- Slices architecture as a restriction  
  - Explained here: [https://github.com/McMaster-Engineering-Society/MES-Website-App-Router/tree/staging/src/slices/hatch/book-by-time](https://github.com/McMaster-Engineering-Society/MES-Website-App-Router/tree/staging/src/slices/hatch/book-by-time) (also internal)

Meeting Notes 9/30  
*Split up work for deliverable package 2*

530pm\~630pm  
All members present

**Notes**

- Basing SRS based on srs.pdf, with removals/additions as suitable for our project  
- Hazard analysis assigned to one person  
  - Likely Johnny, as he is remote  
- SRS kind of linear? In work progress

Michael  
Thomas  
Justin

**System description**

- System context  
- User characteristics  
- Stakeholders  
- Naming conventions,  
- Relevant facts (misc. information not necessarily formal constraints, stakeholders, or requirements)

   
**Problem Description**

- description  
- Terminology, definitions (zhenia)  
- Goal Statements  
- Mandated constraints

***Specific system parts (postponed)***

- *Database (schema, hosting, etc)*  
- *Authentication*  
- *Frontend*  
- *Backend?*  
  - *diagrams, etc, stacks that have been predetermined*

**Requirements (all)**

- functional  
- nonfunctional

- Plan to be done at least description sections by TA meeting on thursday

Meeting Notes 10/2  
*TA Meeting \#2*

Discussion regarding SRS and Hazard Analysis development

**Notes** (most base comments are from TA)

- Should be based on a template, with additions and removals  
  - Log the additions and removals done  
- General format for our SRS document seems mostly fine  
  - Technical specifications, problem, system description are suitable to the project  
- For specific system/technical section  
  - Consider use case diagram  
- **Rubrics can be found on avenue**  
  - Subitems in SRS section need to be accounted for too  
- Potential blind spots/missing items:  
  - Requirements must be traceable (from rubric)  
    - Traceability matrix required  
  - SpecMath  
    - A part of the requirements should be presented in a formal mathematical way  
      - FSM (finite state machine) of user process would be suitable  
- Hazard Analysis  
  - Regarding FME table  
    - Should be traced/related back to requirements in SRS  
      - Can add column for above  
- Safety or security concerns discussed with supervisor?  
  - No formal discussion, but authentication should be conducted so that only club execs can access their financials, etc  
  - Item in rubric for identifying safety/security standards relevant for project  
    - Data handling, privacy, etc standard, we should have at least 1 relative one  
- Technology, solution related stuff should still not be included  
  - With the exception of mandated constraints imposed by MSE client, etc.  
- Next meeting is 3 weeks from now (due to reading week)  
  - Nothing to really worry about in terms of completion other than SRS, HA, peer review until next meeting

Meeting Notes 10/23  
*TA Meeting \#3*  
5:50\~6:20

Discussion regarding upcoming deliverables: VnV, PoC, Design documents

**Notes**

- VnV  
  - System testing goals should come from functional and nonfunctional requirements from SRS  
    - What tests can be done automatically? Which ones need to be done manually  
  - Go through most of the ones required for the PoC should be good  
  - Ideally cover every single requirement in vnv  
    - Can have one test case cover multiple requirements  
- Anything another group/we may have forgotten/will forget to include?  
- Template we are using might be outdated  
  - VnV updated 2 weeks ago, should be good (version 2.4)  
- Software Validation section (3.7)  
  - More about requirements validation than the system/software  
  - Verification vs Validation  
    - Validation: Do we have the right requirements?  
      - Do not need to specify if not required for the project. It **is probably required** for us: will need to check in with MES  
    - Verification: Do we meet the requirements?  
- Whats the expectation for us in terms of development and documentation progress?  
  - TA question: how’s PoC development?  
    - Not going  
      - It should be  
    - Dr. Smith likely most interested in receipt parsing part of the PoC  
      - Should be ready to demonstrate this functionality as part of the PoC, would be a good milestone  
  - What should be prioritizing? What needs to be done for the PoC  
    - Depends on the team, but overall PoC demo is the goal, the overall progress of the project is ok to deprioritize  
      - Demonstration of ability to complete the rest of the project  
    - Should **definitely** include what is included in previously planned PoC documentation  
    - For stuff like UI, just design mockup is fine  
    - For technical stuff like receipt photo processing, the technical code is important  
    - Example: what would you expect in terms of functionality for a financial data app?  
      - Frontend form for inputting data  
      - Backend transmission of data, to database to store  
      - Communication with server to store data  
      - All of the above can be considered expected functionality for this type of app, would be included in a corresponding PoC  
  - Can PoC plan still be changed?  
    - Yes, we can alter past documents and planning to suit ongoing project needs  
    - Can list/describe changes in Demo Plan (section 1 in PoC Team Contrib doc?)?

      

## Meeting Notes 11/6/25

TA Meeting

Notes  
**POC**

- General plan for PoC development is approved  
- TA suggests Dr. Smith will be mostly concerned with OCR as the PoC focus  
  - Prioritize that, flesh it out properly  
- Can we take code from previous groups?  
  - Is there concerns of plagiarism, etc?  
  - TA: not sure, will check with professors  
  - Previous supervisor OK with reusing previous group’s work  
- Any concerns regarding progress tracking/deadlines because we develop in the MES repo?  
  - **Team contribution document**  
    - **Not filled out**  
    - **AKA Team productivity report**  
    - **docs/projectmngmt/poc\_report**  
    - 

**Design Documents**

- How to define a module?  
  - Think of it as a class from any OOP language  
  - But it can be more than that \- an abstract data type  
    - Can be a function, a class, a library, a package  
  - For our purposes, specify the used functions from the module to specify it  
- Anything else?  
  - Read the fine print of the rubric  
    - Some sections can be left blank and you will not lose marks  
      - Ex. section 12 \+ no reflection  
  -


## Meeting Notes 11/20/25

POC Demo and Meeting

Notes  
Biggest Risk at the moment:

- User authentication and role based access control

Biggest Risk solved: 

- Receipt OCR  
  - Structural Parsing  
  - Latency

Professor Smith

- Likes the things being done   
- What are plans for extras?  
  - User manual, Video  
    - Teach the administrators and users how to use the product  
  - Maybe we can do something more interesting?  
    - We can talk about the technology we’ve used as part of our extras  
      - Ex. economic analysis w/ regard to free tier, tiers for apis we’re using  
    - Kind of show off what we’ve done  
    - The business case and why we’ve made the decisions regarding free tier, etc.  
    - If we did any special techniques with regard to OCR? \-\> report about it as an extra document\!  
  - Replace the User Manual\!  
    - Boring, no one reads them, redundant with the user video  
  - Financial report liked  
- Part 2 meeting: How is the team functioning, is it functioning well?  
  - Will assume it is going well due to lack of data from Team charter/compositions/performance document  
- Keep the information brief and critical next time, NO SLIDES\!\!\!

TA question

- How accurate is OCR?  
  - Pretty good, we’ve all independently tried different receipts

- Could we pursue OCR accuracy analysis for extra document?  
  - Dr. Smith: Fine, if it’s interesting, beyond what would simply be done in the verification report  
    - Usability testing could also be something to look at  
- 