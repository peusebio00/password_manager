# password_manager

Program built in Python using the TKInter GUI module

Core functionality:
  - Functions as a password manager - the user is allowed to input a desired website/platform (e.g. Instagram, Tiktok, Amazon, etc), their own email address as well as a     user-chosen password. Once every field is filled out (all required, if anything is left blank then an exception will be caught and inform the user that all fields       must be filled out), then the user may click on the "Add" button to add the above information to a JSON file, where all the aforementioned data will be saved;

Additional functionalities:
  - Generate a random, safe password:
     "Generate" button found by the Password Entry field which allows the user to generate a random password with a combination of a randomised number between 8 and 10 letters, and a randomised number between 2 and 4 for both numbers and symbols, which will then all be shuffled to randomly generate a safe password (which is then also immediately saved onto to the user's clipboard, making it ready for pasting) - example of randomly generated password: e8*3s!mUlCn6Fh;
      
  - Searching for already existing details:
     Right next to the Website Entry field, there is a "Search" button which requires the user to type in the desired website for which details they want to retrieve; Once the button is pressed, the program will look through a Python dictionary (containing the JSON file's information) for a key that matches the website input;
     
     Exceptions are also used to prevent the program from crashing in case:
        a) The user hasn't inputted any sort of information into the password manager yet and thus a JSON file has not yet been created (which will cause a pop up message to display "No Data File Found"), or:
        b) The JSON file already exists but the user hasn't yet added any details for the specific desired website (e.g. User types in "Facebook" and tries to search for the matching details, but hasn't yet added "Facebook" details to the password manager/JSON file - which will cause a pop up message to display "Details for {website in question} do not exist in file.")
