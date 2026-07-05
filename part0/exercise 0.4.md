# Exercise 0.4: New Note Flow
# FLOWCHART DAIGRAM
    Participant browser
    Participant server

 User types a note and clicks 'Save'


       │
       ▼
       
1. BROWSER -> SERVER (POST)                     
    URL: /exampleapp/new_note                           
    Payload: text= BE HAPPY!!!                 

        │
        ▼

3. SERVER -> BROWSER                                   
    - Server adds the note data into the array       
    - Sends 302 redirect codeback to client                    
    - Tells browser: "reload /exampleapp/notes now"      

      │
      ▼
      
      
4. BROWSER -> SERVER (GET request)                     
    - Browser request the main HTML page to reload                
    - Server sends back the notes HTML file
               

          |
          ▼
      

5. BROWSER -> SERVER (GET)                    
    - browser sees whether it needs styling, asks for /exampleapp/main.css
    - Server replies with main.css stylesheet
                          

      │
      
      ▼
   
   
7. BROWSER -> SERVER (GET)
    - browser requests /exampleapp/main.js to execute frontend logic                 
    - Server sends main.js file
    - browser runs the script and triggers a request to fetch data
                             

       │
      
       ▼
      
      
 8. BROWSER -> SERVER (GET)                   
   -  Browser asks for the updated list of notes from exampleapp/data.json                
   -  Server sends fully updated JSON array which inludes the new note as well
   -  script takes the data and redraws the list on the screen
      
