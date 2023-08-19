# firely-test
Repository with postman collections to test the firely server

# Test Execution
The collection consists of tests for create endpoint and deletion of the created resources.
Clone the repository
# Newman
    Install recommended version of nodejs from https://nodejs.org/en
    Install newman: npm install -g newman

    Command to run the test:
    newman run --working-dir data collection\FirelyServer.postman_collection -e environment\firely.postman_environment.json

    Command to run one of the test with multiple test data in iteration:
    newman run collection\FirelyServer.postman_collection --folder Invalid_data_collection -d data\dataSet.json

    For additional reporting, add --reporters cli,json --reporter-json-export outputfile.json

# Postman
    Install Postman
    In settings, point the working directory to the data folder in the cloned repository.
    Import the collection and environment variables.
    
    Run the entire collection:
    Select the environment variable.
    Choose the collection folder and Run.
    
    To run in iteration with test data:
    Choose Invalid_data_collection folder and use "Run folder" option.
    Run manually by selecting Data file as dataSet.json which resides in the data folder.

