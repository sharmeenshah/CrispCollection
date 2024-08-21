Clone the Repository:
git clone https://github.com/sharmeenshah/CrispCollection/    //This is the repository url
cd CRISP Collection                                           // This is repository name
Install Dependencies:
npm install
Run Newman Tests:
newman run CrispAssignment.postman_collection.json \
  -e QA.postman_environment.json \
  -d testdata.csv \
  -r htmlextra \
  --reporter-htmlextra-export newman-report.html
CI/CD Workflow
The GitHub Actions workflow automates testing and archiving reports
Key Steps:
Install dependencies
Run tests
Archive report: Named newman-html-report-success on success or newman-html-report-failure on failure.
