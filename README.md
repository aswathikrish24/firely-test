# firely-test
Repository with postman collections to test the firely server

# Test Execution
    **Newman**
    Install recommended version of nodejs from https://nodejs.org/en
    Install newman: npm install -g newman

    Command to run the test :
    newman run --working-dir data collection\FirelyServer.postman_collection -e environment\firely.postman_environment.json -d data\dataSet.json

    For additional reporting, add --reporters cli,json --reporter-json-export outputfile.json

