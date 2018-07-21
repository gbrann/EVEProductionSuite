# EvE Production Suite - Version 1.1
Eve Online - Production Suite is a set of Google and GESI tools to quickly and easily manage production, budget and basic corporate 
management with installing servers or adding any RL costs to your game play. To do this we are using Google Sheets, Script Editor and
eventually moving this data to a Google Sites setup that pulls the information for the sheets in a nice, easy to use, format for the corp.

This project took us over 3 weeks of daily coding to create and even more to test and change. If you are feeling kind hearted than donations can be sent via Isk (in-game) to Shey Danu. Thank you so much, your helping me by donating. :)

# To Install:

1. Make sure you have a google account. You can create one by going to http://accounts.google.com

2. Goto: https://docs.google.com/spreadsheets/d/1eLYoBSuTzZtlimoShR-x7CQIN6rf-5xJthLmuiKBbuo/edit?usp=sharing

3. Inside Google Sheets - goto File -> Make a Copy

4. Close our Spreadsheet and work now on your own. 

5. We need to make some edits. Lets start with the Configuration Tab: This tab is critical. The first thing you need to do is type your Corporation Name into the B1 cell. 

6. Now we can move on to the Build Cost Calculator. To find your System Cost Index, visit the following website in a new tab:
   https://www.fuzzwork.co.uk/blueprint/costindex.php - we will be looking at the MANUFACTURING value of your system. Input this            percentage in cells B8-B12.

7. Next we will be selecting the type of structure you are using to calculate the structure bonuses you should expect to see. In
   cells C8-C12, you can use the drop down to select the correct structure.

8. We can now set the Player Tax, you can find this by attempting to build anything - look at the costs breakdown to see the Player-        Set Taxes you are currently paying. Input this percent in columns E8-E12. 

9. Now, lets take a look at your Corporate Wallets, you need to set Division Names 1-7. Division 1 is always your Master Wallet.            From here just type in the wallet names in cells C17-C22.

10. Finally, we need set the small details. What is your bonus % paid to members of your production team? Enter this value in G16.           What kind of markup do you want pass down to your clients? The markup % is based on the Universal Average value of an item. Set         this percent in G17. The last value we are looking at is the Ore Buyback %. Most people buy ore from thier corpmates at 95% Buy         Value. This percent is recorded in G18. You can now hide the Configuration Tab by right clicking on the tab and selecting "Hide         Sheet"

11. Cap Build Requirement Backend: Update this to show your ME levels in B Column, You can also double check your part requirement            numbers based on your in-game print. Make sure you update your AD-AE-AF columns which show what a complete BPC pack costs you,          where you aquire the pack and the build cost at your station of choice.

12. In the menu bar go to Tools -> Script Editor.

13. Verify you already have three files in your editor, GESI.gs, endpoints.gs and function.gs - if you do not, continue to step 8, if   you do, skip to step 14.

14. Copy the GESI files. You may need to name the project to save it, so use any name.

15. Copy the contents of GESI.gs into the Code.gs script file, replacing everything in the file, and save the script. (Can rename Code.gs to GESI.gs if you want)

16. Create a new script file (File -> New -> Script File) and name it endpoints.

17. Copy the contents of the endpoints.gs into the script file, replacing everything in the file, and save the script.

18. Create a new script file (File -> New -> Script File) and name it functions.

19. Copy the contents of functions.gs into the script file, replacing everything in the file, and save the script.

20. Go to File -> Project Properties and copy the Script ID.

21. Make a new app on the devsite https://developers.eveonline.com/applications/create.

    Content Type: Authentication & API Access

    PERMISSIONS: Select all esi-* endpoints.

    CALLBACK URL: https://script.google.com/macros/d/{SCRIPT_ID_COPIED_IN_STEP_FIVE}/usercallback

    Be sure to replace the {SCRIPT_ID_COPIED_IN_STEP_FIVE} in the URL with YOUR script ID!
    Also be sure to not include the { and } in your url; it should look something like this, but with your Script ID:
    https://script.google.com/macros/d/15lw-cjwWYnHgLU_tmx6KnyHtZ9aR9Q/usercallback

22. Replace the CLIENT_ID and CLIENT_SECRET variables in GESI.gs (towards the top with your info from the dev app) and save the script.

23. Replace YOUR_MAIN_CHARACTER_NAME with the name of your main (the character to default to if no name is given with a function)           character in the MAIN_CHARACTER constant, and save the script.

24. Close the script and refresh the spreadsheet.

25. There will now be a EvE Production Suite option in the menu bar. Click it and then click 'Authorize Sheet (CEO)'.

26. Give the script permission to do what it needs.

27. Click the EVE SSO button in the modal. Login -> select what character you want to authorize -> Authorize.
28. Close the modal.

29. Done.

# How to Use
The Google Sheet is designed to help manage production jobs. This is for indy based corps in Eve Online to track the corp assets, corp jobs and corp blueprints. No character data is pulled. 

The sheet is designed to be edited by a select few, with view access open to anyone who needs it. There are a total of 52 sheets inside the workbook. Every Capital ship has it's own sheet. By default these sheets are hidden and colored YELLOW. When I am using them, I unhide the sheet (click the bottom-left hamburger menu) so other members of my production team can have easy access to what is needed per job. RED colored tabs are background data tabs and unless otherwise told to, please don't change these tabs as it can cause the entire workbook to stop working. 

To update the data you simply goto the Orders sheet, and on top in I-1 is a large yellow box. This is like this for easy finding. Select this cell. Do not change the cell. Now, with the cell selected, open the EvE Production Suite menu and select 'Pull Data Update'. Give this a few moments to pull all the data, and wallah! Updated with current in-game information. :) Reminder: It is very important that you have the big yellow box selected or you will not update your sheet. 

To change your Current Order number - (this is critical as it effects all other sheets) simply change the number to how many orders you currently have to update the workbook to match current needs. Current Orders is found on the Order Sheet in the B Column.

When looking at your overall industrial needs, open the Corporate Stock sheet, and you will have a combination of every ore, material, and asset required for building. 

When working on a single project, i.e. a Thanatos, open that sheet (Colored Yellow, Hidden, and named for the Ship). It will show you what you need for just that one project. 

IT IS VERY IMPORTANT - Do NOT edit the RED CELLS. Green Cells are generally editable, with yellow cells designed as an "ALERT" for you to easily see data. 

# Upcomming Updates
1. Adding T2 Sub-Cap Ships
2. Adding Equiptment
3. Adding Ammo
4. Adding Jump Freighters
5. Updating the Buyback to a fully functional system based on AMC Spreadsheet (kinda)
6. Functional Updates to Stock, Build Sheets, etc. 
7. The Suite will be divided into several workbooks that all pull from eachother via Google Sites.

# Contact Info
In-game: Shey Danu
Discord: SheyDanu#0260 
Discord Server:  https://discordapp.com/invite/FJ2tRp4

# Copyright
EVE Online and the EVE logo are the registered trademarks of CCP hf. All rights are reserved worldwide. All other trademarks are the property of their respective owners. EVE Online, the EVE logo, EVE and all associated logos and designs are the intellectual property of CCP hf. All artwork, screenshots, characters, vehicles, storylines, world facts or other recognizable features of the intellectual property relating to these trademarks are likewise the intellectual property of CCP hf.
