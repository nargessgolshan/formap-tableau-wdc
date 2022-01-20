
 This is a web data connector for PCAOB Form AP filings (https://pcaobus.org/oversight/standards/implementation-resources-PCAOB-standards-rules/form-ap-auditor-reporting-certain-audit-participants)
 
 Steps:
 1) Make Sure you have anaconda installed on your computer. If not you can download it here: https://www.anaconda.com/products/individual
 2) Create a folder where you want to store all the files needed for this task and remeber the PATH where you create this folder
 3) Download formap.ipynb from this repository and place it in the above folder
 4) Download config.ini file from this repository and place it in the above folder
 5) Open a command prompt (type cmd in windows search box)
 6) Go to the drive where the folder is located by typing E: (Your folder might be in C: D: etc)
 7) Browse to the folder that you created in step 2 by typing: cd PATH
 8) then type "jupyter notebook" in command prompt
 9) A browser page opens that lets you open files in the folder that you created. Open formap.ipynb file that you downloaded in step 3
 10) In the first cell type the PATH that you created in step 2 
 11) Open a new command prompt as in step 5
 12) Repeat steps 6-7
 13) Type "conda create -n jupytab-notebook-env python=3.7"
 14) Type "conda activate jupytab-notebook-env"
 15) Type "conda install -c conda-forge jupytab" and answer y when prompted with y/n command
 16) Type "conda install ipykernel"
 17) Type "conda install requests"
 18) Type "python -m ipykernel install --user --name jupytab-simulation-demo"
 19) Go to the browser page that you opened in step 10
 20) On the "Kernel" -> "Change Kernel" menu , you should see "jupytab-simulation-demo" as an option. Go ahead and select it.
 21) Run the second cell and check if you get any errors. For any packages that you get the "Package not Found Error" do: conda install PACKAGENAME in command prompt where jupytab-notebook-env is active
 22) Open a new command prompt as in step 5
 23) Repeat steps 6-7
 24) In command prompt Type "conda create -n jupytab-server-env python=3.7"
 25) Type "conda activate jupytab-server-env
 26) Type "conda install -c conda-forge jupytab-server" and answer y when prompted with y/n command
 37) Type "jupytab --config=config.ini"

 
 
 
 
 
 References
 1) https://github.com/CFMTech/Jupytab#configuration-file 
 2) https://towardsdatascience.com/interactive-simulation-with-tableau-and-jupytab-c26adb1be564
 
