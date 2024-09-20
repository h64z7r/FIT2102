java c
FIT2102   Programming   Paradigms 2024 
Assignment   1:   Functional   Reactive   ProgrammingDue Date: Friday, 30 August 2024, 11:55   PMWeighting: 30% of your   final mark for the   unitInterview: During Week 7
Overview: Students will work independently to create a game   using   Functional Reactive   Programming (FRP) techniques.   Programs will be implemented   in TypeScript. and use   RxJS Observable streams to   handle animation,   user   interaction,   and other similar stream   behaviours. The goal is to demonstrate a good understanding of functional programming techniques as explored in the first five weeks of the unit, including written documentation of the design decisions   and   features.
Submission instructions
Submit a zipped file named _ame>.zip which extracts to a folder named _  
● It must contain all the code for your program along with   all   the   supporting   files as well as   the report. 
●       It should   include sufficient documentation that   we   can   appreciate   everything   you   have done. 
●       You also need to   include a report   describing   your   design   decisions. 
●       The only external library   should   be   RxJS   libraries   supplied with   the   starter   code. 
The   marking   process will look something like   this: 
1.      Extract _.zip  
2.      Navigate   into the folder named _  
3.      Execute npm   install   and npm   run   dev 
4.    Open http://localhost:5173 in a browser 
Please ensure that you test this process before submitting. Any   issues during this   process will   make your marker unhappy, and   may   result   in a   deduction   in   marks. 
Late submissions will   be   penalised at 5%   per calendar day,   rounded   up.   Late   submissions   more than seven days will receive zero marks   and   no   feedback. 
Git   Instructions 
We will   be   using Git for the assignment,   however, this will   mostly   be self directed.      There are   no   requirements on   how   many commits you   need to the   repo.   However,   we do recommend following good practices, and   having   frequent   commits   with 
meaningful commit   messages.   If any   issues arise with academic   integrity or 
submission, this will   be used as evidence if you   have   completed your   own work   on 
time,   if you   have   no commits, this will likely   make   it   harder for you to clear yourself of   any   possible academic   integrity   issues, so we highly recommend you follow good            practices. 
The assignment   uploaded to   moodle, will   be used for marking,   unless there   are 
exceptional circumstances which prevented you from uploading to   moodle,   at which   point, we will   be   marking the   last version committed to Git   before the due   date. 
The   instructions for the setup are   posted on   Ed, and follow them to   setup   the   repo   and access the skeleton   code.   
Task description 
In this assignment, we will use the   RxJS Observable stream   explored   from   Week   3            to create the classic Guitar Hero game in an SVG   canvas.   You   will   be   provided   with         a starter code bundle similar to the applied   sessions,   including   instructions   on   usage. 
The   image above and the Wikipedia   page are   meant to give you   an   idea   of the   gameplay,   but yours   needn’t   look the same or work   in   precisely the same way,      especially with   regard to graphics. Note that only a subset of the features discussed in the link will be part of the requirements.  
You will also need to write a report, as described below  .  
Requirements 
The game must be implemented in a good functional reactive programming  
style. to get marks. A subset of the game’s features will   be   required   to   get   a   passing   grade. A greater subset of features will   be   required to get a higher   grade.   To   achieve   the   maximum   marks for this assignment, you will   have to use a   little   creativity   and 
add some non-trivial functionality of your own choice. 
Minimum requirements 
All of these   requirements   must   be   reasonably executed to achieve a passing   grade 
-          A game   board with four   columns 
-          Circles appear from the top of the   board   and   move down in   a   continuous   manner, where each circle aligns with a   music   note. 
-          Notes can   be   played   by   using   keys for each   note when   the   circles   align with   the   bottom   row. 
○       You can   use any   keys you want to,   but   this   must   be   documented   somewhere easy to find for your marker. 
- Notes are read from the file   provided   as   input to   the   main   function   (see Note Specificationfor specification) 
-          The timing of the   notes   must align with the   given   CSV   file. 
-          The   notes not for the current   instrument, will   need to   be   played   in the 
background (i.e., without   being displayed on the gameboard) at   the   correct   time. 
-          Notes   demonstrate   reasonable   behaviour 
○       Appear heuristically (a simple   heuristic will   suffice)   across   all four   columns 
○       Notes disappear when   they   have   been   played 
-          Each   note   is   played for the correct   duration   in which they   are   played. 
○       If the   key   press, does   not correctly   align   with   a   note,   it   will   be   played   for   a random duration   between 0 and   0.5s 
-            Each time a   key   is   pressed 
○       The correct note   must   be   played   if the circles align with the   bottom   row 
○       Otherwise, a random note   is   played. -          Scores   must   be   kept track during the game,   for   both   hitting   and   missing   notes. 
-          The game should end when   the   song   finishes   playing. 
-          A short   1-2   page   PDF   report detailing your design decisions   and   use   of   functional   programming techniques discussed in the course   notes 
Full Game   requirements 
Meets   minimum   requirements and   has additional features 
-          If the   note   is longer than   one   second, the   notes   must   have   tails,   where   the   tail   represents the length   of the   note. 
-          The   user must   hold down the   correct   key for the   length   of the tail   to   ensure   it   is ‘correctly’   played 
○       The score will update, iff the   note   is   played for the   correct   duration 
○       If the player lets   go   of the   key   too   early,   the   note   stops   playing 
-          A score   multiplier must   be   included, starting at   1x   and   increasing   by   0.2   for   every   10 consecutive   notes   hit   (e.g.,   10   notes =   1.2x, 20   notes =   1.4x),   and   resetting to   1x when a   note   is   missed. 
-          Smooth   and   usable   gameplay. 
- See video for an   idea of appropriate gameplay. Note: This is not a full implementation but is meant to showcase what a game might look like.  
Additional requirements 
See the Additional Information and How to get a High HD sections. 
Report 
Your report should   be 300–600 words   in length,   plus   up to   200 words   for   each significant additional feature, where you should: 
-          Include basic   report formatting   headings/paragraphs   and   diagrams as necessary  
- Summarise the workings of the code and highlight the   interesting   parts   (don’t just describe what the code does, we can read the   source   code!) 
-          Give a high   level   overview   of your design decisions and justification  -          Explain   how the code follows   FRP   style   and   interesting   usage   of Observable 
-          How state   is managed   throughout   the   game while maintaining purity and why  
-          Describe the usage   of   Observable   beyond   simple   input   and why  
- Important:   Need to   explain why you   did   things 
-          Do not include screenshots of code unless you have an exceptional reason  
-          This should   be concise and straightforward,   you   may   use   dot   points 
Your marker will be instructed to stop reading if your report is too long, and only mark the first 600 (+200 per feature) words.  
Plagiarism 
We will   be checking your code against the   rest of the class   and the   internet   using   a   plagiarism checker.    Monash applies strict   penalties to students who   are   found   to have committed   plagiarism. Additionally, we will be conducting an   interview, which      gives you a chance to explain your code and   help   us   understand   your   code   better.      As long as you wrote your own code, there   is   nothing to   worry   about   during   the interview   process. 
AI statement 
As   per the AI statement on Moodle, use of generative AI   in this   unit   is   unrestricted.   However, all code generated with AI must be   properly cited in   the   form   of code comments stating what   has   been generated and the scope of its   use.   You   must   be   able to demonstrate   understanding of all code submitted as   part of your assignment,   inability to explain any submitted code   may result   in   an   academic   integrity   case. 
Definition of a   Note 
There are two types   of   notes: 
1.       user_played   == True: This   is   the   note   which   will   be   played   by   the   user   during the game. 
○       Appearance: In the game,   notes are   represented as   coloured 
circles that travel down the screen.   Each   note will   be   in a 
column,   however, the column does   not   need to   have one-to-one   mapping with an individual   pitch value. 
○       Columns: The game screen   is   divided   into   four   columns,   each   associated with a different   button or   key. 
● Musical Correspondence: 
○       Sound Trigger: When a   note   reaches the   designated   row      at   the      bottom of the screen, the   player must   press the corresponding               button or key.   If done correctly and   in time代 写FIT2102 Programming Paradigms 2024 Assignment 1: Functional Reactive ProgrammingJava
代做程序编程语言,   this   action   "plays"   the   note,   meaning   it triggers the associated   musical sound. 
○       Timing: The timing of pressing   the   button   or   key   is   crucial.   The   game typically rates the accuracy of the   player's timing, which      affects the score and the quality of the   performance. 
2.      user_played   ==   False: The   note   will   be   played   by   your   code, but   will   not   be shown to the   user in the game,   but   played   using the   music   library. 
Note Specification   CSV 
Each note is specified by five columns: user_played, instrument_name, velocity,   pitch, start   (s), end   (s). 
●       If   the   user_played   column   is   True, this   note   should   appear   in   the   game,   otherwise, the   note should   be   played   in the   background. 
●       The   instrument_name   will   be   the   instrument   for   which   the   note   should   be played   in from the sample   library 
●       The   velocity   of   the   note   represents   the volume,   between   0   and   127. Note:   the API   requires this to   be   in the   range   [0,1] 
● The   pitch   of   the   note. 
● start   (s): start   time   in   seconds, which   is   when   the   note   should   be   played 
● end   (s):    end time in seconds, which is when   the   note   should   be   stopped. 
How to   play   a   note: 
To   play a note, you can use the given samples   dictionary.   This   is   already   set   up   in               the skeleton code and   is   unlikely to   be changed.   Each   instrument from the   CSV,   can   be used as the key in the dictionary. You can   use the   triggerAttack   Release 
function. This takes four arguments: 
1.       The tone to play, which can be specified   using   the   pitch   from   the   CSV 
2.      The duration of the   note   in seconds 
3.      The   start   time,set   to   undefined, to   start   playing   the   note   instantly. 
4.      The volume of the   note, which corresponds to the velocity,   in the range   [0,1] 
An   example   of   playing   notes   is   shown   in   the   given   midi_example   .ts   file, which   you can   refer to,   but   is also   provided   below. 
Additional   Information:   Marking Criteria and Suggestions This section   is   not essential for completing the assignment, and   is   provided   purely   for context and additional   information to answer common questions   students   may      have. 
Marking (30   marks total) 
The goal of this assignment   is to assess your understanding   of   FRP   and   Functional   Programming. The   marking   has   three   broad sections: 
1.      Implementation of game features 
2.      Usage and understanding of proper functional   programming style 
3.      Usage and understanding of RxJS   and   Observable 
It   is●important to   realise that: 
demonstrating application of functional   programming ideas from our lectures   and applied sessions. 
○       You can receive   up to a Distinction for   perfectly   implementing the 
Minimum requirements and demonstrating an excellent 
understanding of how to use Observable to write   clean,   clear functional   UI   code. 
●       To achieve a High Distinction, you will   need to   implement   the Full game requirements  
●       To achieve the maximum possible marks, you will   need   to   implement   the   full   game requirements   plus some   aspect of additional functionality, as 
described   below. 
Note that it is essential to follow the submission instructions, as deductions may be applied for failing to follow the submission instructions.  
We will mark 5 sections – Report, Functional Programming style, Code Quality, 
Observable and RxJS usage, and Game Features (including advanced features) –   that are individually weighted. 
Code that does   not   use Observable will not get a   passing grade;   games   that   use   imperative,   impure, or mutable code will be   heavily   penalised. 
The rubric and marking   guide   are   provided here. 
Report   (4   marks) The report   is intended to demonstrate your theoretical   understanding of functional         reactive   programming,   highlight design decisions, and help your marker   appreciate   the work that you   have   put   into this assignment. 
Important considerations for the report: 
●       Need to display   understanding   of course   material 
●       Reports must demonstrate   knowledge of   FRP to   achieve   a   passing   mark 
●       Marks can be awarded for students identifying issues with the code and how they can be addressed  
●       Avoid filler in the   report,   but   include enough   information to   show your   marker   that you   have understood the core   concepts 
Functional   Programming style. (8   marks) 
This section   is about   using what we   have covered   in lectures and   tutorials.   This 
invo●lves concepts   like: 
●       Reusable functions, avoiding   duplicate   code 
● Purity / referential transparency 
● Fluent   interfaces and fluent coding style 
●       Manipulation of different complex types   and   generic   types 
● HOF, curried functions 
● Function composition/chaining 
To achieve the maximum available marks, it is important to not only use  
advanced functional programming concepts, but do so in a useful way – for   example,   improving the readability of the code or following a declarative 
programming style.    For   example, simply currying   all your functions will   not   receive   marks unless they are partially applied   somewhere   and   used   appropriately 
You   may also attempt to   use   Lambda Calculus concepts   in your   code;   however,   be            careful as they can often just   make things   hard to understand –   it will   be   important to   explain their usage   in your report, so your marker   can   better   appreciate   your work. 
Deductions will be applied for improper usage of types,   including   unjustified   “any”   types. 
Code Quality   (8   marks) 
This section   loosely covers anything to do with   how readable   and   understandable   your code   is. Applying a good functional   programming style. tends to   increase the 
readability of your code. It is important that your code can be easily understood to help your marker appreciate your work.  
Some examples of what we look   at   are 
●       Appropriate line lengths   (<80 characters) ●       Documentation and commenting (should   explain why   the   code   is   the way   it   is) 
●       Logical structuring of functions and variables,   including   overall flow   of   program   logic 
●       Appropriate variable naming 
●       Consistent and understandable   formatting 
Using a linter and formatter may   help greatly with   this   section. See below for tips and suggestions.  
Observable and   RxJS   usage (8   marks) 
This section covers usage of FRP –   did   you   use   Observable   well? 
Some   important considerations: 
●       Must manage game state in Observable,   and   use   the scan and merge operators to get a passing mark (please refer to the   Asteroids   example) 
●       Must   handle creation of a   stream   of   notes   using   Observables   and   an   appropriate set of operations 
●       Usage of Observable as per   discussed   in   the   lectures,   applied   sessions, 
workshop, and   in the Asteroids example, while   maintaining   purity,   is sufficient   for a high mark   in this section   if implemented very well and without   issues 
● To achieve the maximum marks available, we want to see interesting and creative uses for Observable and RxJS operators (original work)  
○       This can   involve   implementing custom Observables   and   research   into   the RxJS operators documentation  
○       Refer to the marking guide for   a   breakdown   of what   is   required. 
Side effects should   be contained as   much   as   possible 
●       Using additional   RxJS operators that   are   not   covered   in   class,   or   using   the      ones we   introduce   in   interesting and   novel ways, will   be awarded additional   marks (given that they are appropriate   and   useful) 
Game   Features (2   marks) 
This section   is about whether your game fulfils the requirements, and   the   overall   complexity   of   your   game   (and   thus   the   implementation). 
Adding features should   not come at the expense of the other   criteria –   a well 
implemented game with fewer features   may and, often will, achieve a   higher   mark   than a less well implemented   game with   more features. 
Important: You will   receive   marks for implementing game features,   but this mark will also cap your total mark. 
●       The   maximum   mark   possible for implementing minimum game requirements is 70 (Distinction) 
●       The   maximum   mark   possible for implementing full game requirements is   90   (HD) 
●       To achieve the maximum available   marks   (90+), you   must   implement 
advanced requirements  
Some   marking considerations: 
● Extra features   must follow   FRP 
●       Advanced requirements can be not just gameplay   but   extra   FRP   features   too 
●       Tests: for full   marks, tests   need to   be comprehensive and   not just   simple/random test cases – they should guide development 
●       Bugs and other gameplay   related   issues will not be   deducted   from   this   section and be deducted from   the   total   mark 
●       The total   mark cap will   be   increased when   implementing additional features.   It   is possible to achieve an   HD by implementing   the   minimum   game 
requirements and some full game   requirements 
To achieve the maximum available marks, features should be significant and change how state is managed in interesting ways. Discussed further below. 
Bonus   marks are available for particularly   novel,   impressive, or advanced features.   Note that   marks cannot exceed   100% of the total available   marks. 

         
加QQ：99515681  WX：codinghelp
