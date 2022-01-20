
 This is a Tableau web data connector for PCAOB Form AP filings (https://pcaobus.org/oversight/standards/implementation-resources-PCAOB-standards-rules/form-ap-auditor-reporting-certain-audit-participants)
 
 Steps:
 1) Make sure you have anaconda installed on your computer. If not you can download it here: https://www.anaconda.com/products/individual
 2) Create a folder where you want to store all the files needed for this task and remeber the PATH where you create this folder
 3) Download formap.ipynb from this repository and place it in the above folder
 4) Download config.ini file from this repository and place it in the above folder
 5) Open a command prompt from anaconda
 6) Go to the drive where the folder is located by typing E: (Your folder might be in C: D: etc)
 7) Browse to the folder that you created in step 2 by typing: cd PATH
 8) Type "conda create -n jupytab-notebook-env python=3.7" NOTE: MAKE SURE YOU ARE IN THE FOLDER THAT YOU CREATED IN STEP 2
 9) Type "conda activate jupytab-notebook-env"
 10) Type "pip install jupytab ipykernel requests" and answer y when prompted with y/n command
 11) Type "python -m ipykernel install --user --name jupytab-simulation-demo"
 12) Type "jupyter notebook" 
 13) A browser page opens that lets you open files in the folder that you created. Open formap.ipynb file that you downloaded in step 3
 14) On the "Kernel" -> "Change Kernel" menu , you should see "jupytab-simulation-demo" as an option. Go ahead and select it.
 15) In the first cell type the PATH  that you created in step 2 in os.ch("PATH") and path="PATH" 
 16) Open a new command prompt as in step 5
 17) Repeat steps 6-7
 18) Run the second cell and check if you get any errors. For any packages that you get the "Package not Found Error" do: pip install PACKAGENAME in command prompt where jupytab-notebook-env is active
 19) Open a new command prompt from anaconda as in step 5
 20) Repeat steps 6-7
 21) In command prompt Type "conda create -n jupytab-server-env python=3.7" NOTE: MAKE SURE YOU ARE IN THE FOLDER THAT YOU CREATED IN STEP 2
 22) Type "conda activate jupytab-server-env"
 23) Type "pip install jupytab-server" and answer y when prompted with y/n command
 24) Type "jupytab --config=config.ini"
 25) look for: "please open: "http://xxxxxxxxxxxxxx" and copy the address
 26) Open Tableau and under "Connect" Look for "To a Server", then choose "Web Data Connector"
 27) Paste the address above in step 25 (http://xxxxxxxxxxxxxx) at the space on top of the page
 28) then you will see your jupyter notebook
 29) click on that and then select "Explore in Tableau"
 30) Click "update" if data does not appear and you should see all the fields

TADAAA! The Form AP data is in tableau without having to manually download it on your computer everytime it updates and clean it in tableau for variable types and keep only those variables that you need!

 
 
 
 
 References
 1) https://github.com/CFMTech/Jupytab#configuration-file 
 2) https://towardsdatascience.com/interactive-simulation-with-tableau-and-jupytab-c26adb1be564
 
