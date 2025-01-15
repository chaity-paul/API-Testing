Project Overview
This project demonstrates how to test RESTful APIs using Postman for manual testing and Newman for automated command-line execution. The tests include the following HTTP methods:

GET: Retrieve data from the server.
POST: Submit data to the server.
PUT: Update existing data on the server.
Test results are generated in both CLI format and HTML format for easy analysis.

Getting Started
To get started with the project, you need to have Postman, Newman, and Node.js installed on your local machine.

Prerequisites
Node.js and npm: Ensure that Node.js and npm (Node Package Manager) are installed on your machine. You can download and install them from here.

Verify installation by running:
bash
Copy
Edit
node -v
npm -v
Postman: You can download Postman from here.

Newman: Install Newman globally to run the Postman collections from the command line.

bash
Copy
Edit
npm install -g newman
Newman HTML Reporter (optional for HTML reports):

bash
Copy
Edit
npm install -g newman-reporter-html
Testing Methodology
The API tests are organized in Postman collections, with each collection corresponding to different API endpoints. The methods tested include:

GET: Verifies that the server responds correctly to a request to retrieve data. Validates status codes, response time, and response body.
POST: Tests the creation of new resources on the server. Validates status codes, request body, and response body.
PUT: Tests updating an existing resource. Validates status codes, request body, and response body.
Each of these methods is thoroughly tested with different scenarios to ensure correct functionality.

Running Tests with Newman
Once you have set up your environment and installed the required dependencies, you can run the API tests using Newman.

Steps to Run Tests
Clone this repository to your local machine:

bash
Copy
Edit
git clone https://github.com/your-username/your-repository.git
cd your-repository
Run the Newman Command to execute the Postman collection:

bash
Copy
Edit
newman run Test.postman_collection.json -e test.postman_environment.json -r cli,html
Test.postman_collection.json: The Postman collection file that contains the API tests.
test.postman_environment.json: The environment file that defines the variables required by the collection (e.g., base URLs, authentication tokens).
Generate Test Reports: After running the command, you will get the results in the terminal (CLI report) and an HTML report (newman-run-report.html) that can be viewed in your browser.

Test Reports
The test results are generated in the following formats:

CLI Report: Output directly in the terminal window with test status and summary.
HTML Report: A comprehensive, visually formatted report generated in an HTML file. This file is stored in the directory where the tests were executed and can be opened in any browser.
Example of HTML Report File Name:
newman-run-report.html
Conclusion
This repository demonstrates how to use Postman for manual API testing and Newman for automating those tests through the command line. The project tests common HTTP methods (GET, POST, and PUT) to ensure that the API behaves as expected. The results are generated in both CLI and HTML formats for ease of use.

Feel free to contribute by submitting issues or pull requests to improve the tests or add additional scenarios.

Optional Additions:
You can add additional sections for Licenses, Contributions, or Acknowledgments as needed.
Include specific API details like endpoint descriptions, authentication methods, etc., if applicable.
Let me know if you need any further customization!
