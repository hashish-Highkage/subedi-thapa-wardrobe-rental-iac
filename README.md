# Subedi Thapa Wardrobe Rental Web Application

## Project Owners

- **Names:** Ashish Subedi & Bijay Thapa
- **Phone:** 0470 345 ***
- **Emails:** ashishsubedi313@gmail.com, bijaythapa@gmail.com
- **Location:** 110 Castlereagh St, NSW 2170
- **Facebook:** https://www.facebook.com/hashish.highkage
- **Instagram:** https://www.instagram.com/hashish_highkage
- **Live Website:** subedi-thapa-rental-app-ashish-bijay-313.azurewebsites.net

# Subedi & Thapa Wardrobe Rental – Cloud IaC Deployment

## Project Overview

This project is a simple cloud-based wardrobe rental web application developed for Assessment 3: Enterprise Cloud Infrastructure Design. The application allows users to view clothing rental categories, men’s and women’s clothing items, login/register pages, wishlist, cart, and contact information.

The purpose of this project is to demonstrate cloud deployment using DevOps practices, Infrastructure as Code, and CI/CD automation.

## Technologies Used

* HTML, CSS and JavaScript for the web application
* Node.js and Express.js to serve the static web application
* Microsoft Azure App Service for cloud hosting
* Terraform for Infrastructure as Code
* GitHub Actions for CI/CD automation
* GitHub for version control and team collaboration

## Cloud Architecture

The application is deployed to Microsoft Azure using Terraform. The infrastructure includes:

* Azure Resource Group
* Azure App Service Plan
* Azure Linux Web App

Terraform provisions the required cloud infrastructure automatically. GitHub Actions then builds and deploys the web application to Azure App Service.

## Repository Structure

```text
subedi-thapa-wardrobe-rental-iac/
├── app/
│   ├── package.json
│   ├── server.js
│   └── public/
│       ├── index.html
│       ├── about-us.html
│       ├── categories.html
│       ├── contact-us.html
│       ├── login.html
│       ├── register.html
│       ├── mens.html
│       ├── womens.html
│       ├── cart.html
│       ├── wishlist.html
│       ├── css/
│       └── assets/
│
├── terraform/
│   ├── providers.tf
│   ├── variables.tf
│   ├── main.tf
│   └── outputs.tf
│
├── .github/
│   └── workflows/
│       └── deploy.yml
│
└── README.md
```

## Infrastructure as Code

Terraform is used to create and manage the Azure infrastructure. The Terraform files are stored inside the `terraform` folder.

Main Terraform files:

* `providers.tf` configures the Azure provider.
* `variables.tf` stores reusable variable values.
* `main.tf` defines Azure infrastructure resources.
* `outputs.tf` displays the deployed web application URL.

## CI/CD Pipeline

GitHub Actions is used to automate the deployment process. The workflow file is located at:

```text
.github/workflows/deploy.yml
```

The pipeline performs the following steps:

1. Checks out the GitHub repository.
2. Sets up Terraform.
3. Runs Terraform init, validate, plan, and apply.
4. Sets up Node.js.
5. Installs application dependencies.
6. Tests the application.
7. Logs in to Azure.
8. Deploys the application to Azure App Service.

## Testing

The project was tested using the following methods:

* Terraform validation was completed successfully.
* Terraform plan and apply were completed successfully.
* GitHub Actions workflow completed successfully.
* Azure Resource Group and App Service were created successfully.
* The live wardrobe rental website opened successfully in the browser.
* The `/health` endpoint confirmed that the application was running.

## Live Application

Live website URL:

```text
subedi-thapa-rental-app-ashish-bijay-313.azurewebsites.net
```

Health check URL:

```text
subedi-thapa-rental-app-ashish-bijay-313.azurewebsites.net/health
```

## Team Members

* Ashish Subedi
* Bijay Thapa

## Individual Contributions

| Team Member   | Contribution                                                                                                         |
| ------------- | -------------------------------------------------------------------------------------------------------------------- |
| Ashish Subedi | GitHub repository setup, web app organisation, Terraform review, deployment testing, screenshots, report preparation |
| Bijay Thapa   | Web application customisation, Azure testing support, presentation preparation, documentation review                 |

## Conclusion

This project demonstrates how a simple web application can be deployed to the cloud using Infrastructure as Code and CI/CD automation. Terraform provides repeatable cloud infrastructure provisioning, while GitHub Actions automates the build and deployment process. The project also supports DevOps principles such as version control, automation, testing, collaboration, and continuous deployment.
