# firely-test
Repository with postman collections to test the firely server

# Test Execution
    **Newman**
    Install recommended version of nodejs from https://nodejs.org/en
    Install newman: npm install -g newman

    Command to run the test:
    newman run --working-dir data collection\FirelyServer.postman_collection -e environment\firely.postman_environment.json
┌─────────────────────────┬────────────────────┬────────────────────┐
│                         │           executed │             failed │
├─────────────────────────┼────────────────────┼────────────────────┤
│              iterations │                  1 │                  0 │
├─────────────────────────┼────────────────────┼────────────────────┤
│                requests │                 15 │                  0 │
├─────────────────────────┼────────────────────┼────────────────────┤
│            test-scripts │                 30 │                  0 │
├─────────────────────────┼────────────────────┼────────────────────┤
│      prerequest-scripts │                 30 │                  0 │
├─────────────────────────┼────────────────────┼────────────────────┤
│              assertions │                 40 │                  0 │
├─────────────────────────┴────────────────────┴────────────────────┤
│ total run duration: 3.2s                                          │
├───────────────────────────────────────────────────────────────────┤
│ total data received: 23.79kB (approx)                             │
├───────────────────────────────────────────────────────────────────┤
│ average response time: 130ms [min: 15ms, max: 769ms, s.d.: 175ms] │
└───────────────────────────────────────────────────────────────────┘
   

    Command to run one of the test with multiple test data in iteration:
    newman run collection\FirelyServer.postman_collection --folder Invalid_data_collection -d data\dataSet.json

┌─────────────────────────┬───────────────────┬───────────────────┐
│                         │          executed │            failed │
├─────────────────────────┼───────────────────┼───────────────────┤
│              iterations │                 5 │                 0 │
├─────────────────────────┼───────────────────┼───────────────────┤
│                requests │                 5 │                 0 │
├─────────────────────────┼───────────────────┼───────────────────┤
│            test-scripts │                10 │                 0 │
├─────────────────────────┼───────────────────┼───────────────────┤
│      prerequest-scripts │                10 │                 0 │
├─────────────────────────┼───────────────────┼───────────────────┤
│              assertions │                20 │                 0 │
├─────────────────────────┴───────────────────┴───────────────────┤
│ total run duration: 797ms                                       │
├─────────────────────────────────────────────────────────────────┤
│ total data received: 3.27kB (approx)                            │
├─────────────────────────────────────────────────────────────────┤
│ average response time: 64ms [min: 16ms, max: 205ms, s.d.: 71ms] │
└─────────────────────────────────────────────────────────────────┘

    For additional reporting, add --reporters cli,json --reporter-json-export outputfile.json

