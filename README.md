# Subedi Thapa Wardrobe Rental Web Application

## Project Owners

- **Names:** Ashish Subedi & Bijay Thapa
- **Phone:** 0470 345 ***
- **Emails:** ashishsubedi313@gmail.com, bijaythapa@gmail.com
- **Location:** 110 Castlereagh St, NSW 2170
- **Facebook:** https://www.facebook.com/hashish.highkage
- **Instagram:** https://www.instagram.com/hashish_highkage

## Project Overview

This repository contains a clothing rental website hosted as a Node.js Express application and prepared for deployment to Microsoft Azure App Service using Terraform and GitHub Actions.

The website has been customised as **Subedi Thapa Wardrobe Rental**, a simple rental platform for traditional and modern outfits. The sample product names, website branding, contact details and cloud resource names have been updated for Ashish Subedi and Bijay Thapa.

## Main Features

- Static clothing rental website with Home, Categories, Mens, Womens, Wishlist, Cart, Login, Register, About Us and Contact Us pages.
- Custom product catalogue using renamed sample items such as Castlereagh Velvet Shirt, Sydney Printed Kurta and Harbour Tiered Dress.
- Node.js Express server for hosting the static website.
- `/health` endpoint for deployment testing.
- Terraform Infrastructure as Code for Azure Resource Group, App Service Plan and Linux Web App.
- GitHub Actions workflow for Terraform provisioning and Azure Web App deployment.

## Project Structure

- `app/public/` contains the HTML, CSS and image files for the website.
- `app/server.js` serves the static website and provides the `/health` endpoint.
- `terraform/` contains the Infrastructure as Code files for Azure.
- `.github/workflows/deploy.yml` contains the CI/CD pipeline.

## Deployment Summary

Terraform provisions:

- Azure Resource Group
- Azure App Service Plan
- Azure Linux Web App

GitHub Actions runs Terraform and deploys the Node.js web app to Azure App Service.

## Health Check

After deployment, test:

`https://<your-web-app-name>.azurewebsites.net/health`
