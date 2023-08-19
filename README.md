# firely-test
Repository with postman collections to test the firely server

# Folder structure is as follows:
firely-test
    |_collection
    |   |_postman-collectionFile
    |_data
    |   |_dataFile1
    |   |_dataFile2
    |   |_dataFile3
    |_environment
    |   |_envFile1
    |_ReadmeFile

# Test Execution
    The tests can be run in 2 ways
    Newman
    Install recommended version of nodejs from https://nodejs.org/en
    Install newman: npm install -g newman

    Command to run the test :
    newman run --working-dir data collection\FirelyServer.postman_collection -e environment\firely.postman_environment.json -d data\dataSet.json

    For additional reporting, add --reporters cli,json --reporter-json-export outputfile.json

