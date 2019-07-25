# COPDgene PIC-SURE Jupyter Examples

This repository serves as a starting point to accessing phenotype data on the PIC-SURE COPDgene-dev instance.

While this is a development environment, it houses real COPDgene data. 

Let me rephrase that, the data in this environment is NOT test data, it is real data on actual COPDgene study participants.

This repository itself contains no actual patient data, and contains no actual credentials.

You are responsible to obtain proper authorization tokens from the https://copdgene-dev.hms.harvard.edu site and to ensure that your use of the data meets all requirements governed by the CODPgene data policies.

To use this repository, you need a working docker environment that is compatible with docker-compose. Managing your docker infrastructure and packages is outside the scope of this repository.

The Jupyter Notebook server that is created as a result of this docker-compose stack has no authentication, authorization or encryption in front of it. Securing it is your responsibility. Minimally this will require running it only on a locally hosted docker engine on a local VM that is only accessible from your local workstation(using docker-machine usually meets this requirement).

Do not start the server unless you understand the security concerns around it and the requirements to secure the data from misuse.

To start the server just run:

`docker-compose up -d`

On startup this will copy the example notebooks to a gitignore'd jupyter-notebook-working folder within the repo. This is because Jupyter saves the output of your queries into the notebook files themselves by default. This will prevent you from accidentally committing private study specific data to GitHub.

Once the stack has started, point your web browser at the ip address of the server that is running docker.

You can then go through the appropriate examples based on your authorized consent groups within the COPDgene study.

The reason there are 3 sets of examples is so that all types of users can run the examples without modification.

You do still need to put your token as retrieved from https://copdgene-dev.hms.harvard.edu into a file named COPDgene_token.txt in the folder for your specific set of examples before they will run successfully.

To obtain your token go to the following link:

https://copdgene-dev.hms.harvard.edu/psamaui/login/?redirection_url=/psamaui/userProfile


