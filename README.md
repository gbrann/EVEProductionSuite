# EVEProductionSuite
Eve Online - Production Suite is a set of Google and ESI tools to quickly and easily manage production, budget and basic corporate 
management with installing servers or adding any RL costs to your game play. To do this we are using Google Sheets, Script Editor and
eventually moving this data to a Google Sites setup that pulls the information for the sheets in a nice, easy to use, format for the corp.

This project took me over 60 hours to create and even more to test and change. If you are feeling kind hearted than donations can be sent via Isk (in-game) to Shey Danu. Thank you so much, your helping me by donating. :)

To Install:

1. Make sure you have a google account. You can create one by going to http://accounts.google.com
2. Goto: https://docs.google.com/spreadsheets/d/16eg1WitkXGIhFX9WWsYfj2T40yP1MjJz0ByM1kQqLbY/edit?usp=sharing
3. Inside Google Sheets - goto File -> Make a Copy
4. Close our Spreadsheet and work now on your own. 
5. We need to make some edits. 
    -Orders: Update A1 to have your Corp Name in the title. 
    -Budgeting: Update the budgets titles and what your tracking on this page. By default I'm tracking 3 of my wallet budgets, Expenses,        Operations and Market. Buyback, and Production budgets are automaticly tracked and pulled. 
    -Cap Build Requirement Backend: Update this to show your ME levels in B Column, You can also double check your part requirement            numbers based on your in-game print. Make sure you update your AD-AE-AF columns which show what a complete BPC pack costs you,          where you aquire the pack and the build cost at your station of choice.
6. In the menu bar go to Tools -> Script Editor.
7. Verify you already have three files in your editor, GESI.gs, endpoints.gs and function.gs - if you do not, continue to step 8, if you do, skip to step 14.
8. Copy the GESI files. You may need to name the project to save it, so use any name.
9. Copy the contents of GESI.gs into the Code.gs script file, replacing everything in the file, and save the script. (Can rename Code.gs    to GESI.gs if you want)
10. Create a new script file (File -> New -> Script File) and name it endpoints.
11. Copy the contents of the endpoints.gs into the script file, replacing everything in the file, and save the script.
12. Create a new script file (File -> New -> Script File) and name it functions.
13. Copy the contents of functions.gs into the script file, replacing everything in the file, and save the script.
14. Go to File -> Project Properties and copy the Script ID.
15. Make a new app on the devsite https://developers.eveonline.com/applications/create.
    Content Type: Authentication & API Access
    PERMISSIONS: Select all esi-* endpoints.
    CALLBACK URL: https://script.google.com/macros/d/{SCRIPT_ID_COPIED_IN_STEP_FIVE}/usercallback
    Be sure to replace the {SCRIPT_ID_COPIED_IN_STEP_FIVE} in the URL with YOUR script ID!
    Also be sure to not include the { and } in your url; it should look something like this, but with your Script ID:
    https://script.google.com/macros/d/15lw-cjwWYnHgLU_tmx6KnyHtZ9aR9Q/usercallback
16. Replace the CLIENT_ID and CLIENT_SECRET variables in GESI.gs (towards the top with your info from the dev app) and save the script.
17. Replace YOUR_MAIN_CHARACTER_NAME with the name of your main (the character to default to if no name is given with a function)           character in the MAIN_CHARACTER constant, and save the script.
18. Close the script and refresh the spreadsheet.
19. There will now be a EvE Production Suite option in the menu bar. Click it and then click 'Authorize Sheet (CEO)'.
20. Give the script permission to do what it needs.
21. Click the EVE SSO button in the modal. Login -> select what character you want to authorize -> Authorize.
22. Close the modal.
23. (Optional) Repeat step 12 to authorize other characters.
24. Done.
