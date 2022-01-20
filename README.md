
 This is a Tableau web data connector for PCAOB Form AP filings (https://pcaobus.org/oversight/standards/implementation-resources-PCAOB-standards-rules/form-ap-auditor-reporting-certain-audit-participants)
 
 Steps:
 1) Make Sure you have anaconda installed on your computer. If not you can download it here: https://www.anaconda.com/products/individual
 2) Create a folder where you want to store all the files needed for this task and remeber the PATH where you create this folder
 3) Download formap.ipynb from this repository and place it in the above folder
 4) Download config.ini file from this repository and place it in the above folder
 5) Open a command prompt from anaconda
 6) Go to the drive where the folder is located by typing E: (Your folder might be in C: D: etc)
 7) Browse to the folder that you created in step 2 by typing: cd PATH
 8)  Type "conda create -n jupytab-notebook-env python=3.7" NOTE: MAKE SURE YOU ARE IN THE FOLDER THAT YOU CREATED IN STEP 2
 9) Type "conda activate jupytab-notebook-env"
 10) Type "pip install jupytab" and answer y when prompted with y/n command
 11) Type "pip install ipykernel"
 12) Type "pip install requests"
 13) Type "python -m ipykernel install --user --name jupytab-simulation-demo"
 14) Type "jupyter notebook" 
 15) A browser page opens that lets you open files in the folder that you created. Open formap.ipynb file that you downloaded in step 3
 16) On the "Kernel" -> "Change Kernel" menu , you should see "jupytab-simulation-demo" as an option. Go ahead and select it.
 17) In the first cell type the PATH that you created in step 2 
 18) Open a new command prompt as in step 5
 19) Repeat steps 6-7
 20) Run the second cell and check if you get any errors. For any packages that you get the "Package not Found Error" do: conda install PACKAGENAME in command prompt where jupytab-notebook-env is active
 21) Open a new command prompt from anaconda as in step 5
 22) Repeat steps 6-7
 23) In command prompt Type "conda create -n jupytab-server-env python=3.7" NOTE: MAKE SURE YOU ARE IN THE FOLDER THAT YOU CREATED IN STEP 2
 24) Type "conda activate jupytab-server-env"
 25) Type "pip install jupytab-server" and answer y when prompted with y/n command
 26) Type "jupytab --config=config.ini"
 27) look for: "please open: "http://xxxxxxxxxxxxxx" and copy the address
 28) Open Tableau and under "Connect" Look for "To a Server", then choose "Web Data Connector"
 29) Paste the address above (http://xxxxxxxxxxxxxx) at the space on top of the page
 30) then you will see your jupyter notebook
 31) click on that and then select "Explore in Tableau"
 32) Click "update" if data does not appear and you should see all the fields

TADAAA! The Form AP data is in tableau without having to manually download it on your computer!

 
 
 
 
 
 References
 1) https://github.com/CFMTech/Jupytab#configuration-file 
 2) https://towardsdatascience.com/interactive-simulation-with-tableau-and-jupytab-c26adb1be564
 
