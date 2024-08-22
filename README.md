#ASSIGMENT SOLUTION#
Author Sharmeen Shah
## Clone the Repository

```bash
git clone https://github.com/sharmeenshah/CrispCollection/   # Repository URL
cd "CRISP Collection"                                         # Repository name
```
## Install the dependencies
```bash
npm install newman
npm install newman-html-extra
```

# Run the newman tests:
```bash

newman run CrispAssignment.postman_collection.json \
  -e QA.postman_environment.json \
  -d testdata.csv \
  -r htmlextra \
  --reporter-htmlextra-export newman-report.html
```

For the automation purpose I have integrated it with the github actions.

CI/CD Workflow
The GitHub Actions workflow automates testing and archiving of reports.

Named newman-html-report-success on success
Named newman-html-report-failure on failure
