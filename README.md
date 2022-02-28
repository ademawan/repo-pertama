<div id="top"></div>

# AIRBNB BE-6

<!-- PROJECT LOGO -->
<div align="center">

  <h3 align="center">AIRBNB</h3>
Find vacation rentals, cabins, beach houses, unique homes and experiences around the world - all made possible by hosts on Airbnb

  <p align="center">
    AIRBNB DEVELOPMENT
    <br />
    <div id = "other-software-design"></div>
    ·
    <a href="https://github.com/AIRBNB-App-Project2/backend-airbnb/tree/main/repository/altaProject.drawio?raw=true">ERD</a>
    ·
    <a href="https://app.swaggerhub.com/apis/faliqadlan/airbnb/1.0.0">Open API</a>
  </p>
</div>
<br />

<!-- TABLE OF CONTENTS -->
## Table of Contents
1. [About the Project](#about-the-project)
2. [High Level Architecture](#high-level-architecture)
3. [Tech Stack](#tech-stack)
4. [Code Structure](#code-structure)
    - [Structuring](#structuring)
    - [Unit Test](#unit-test)
5. [How to Contrib](contribute.md)
6. [Contact](#contact)

<!-- ABOUT THE PROJECT -->
## About The Project
- An app that allow user to be a pet shop owner to sell their services and products or to be a customer to buy them. 
- Pet shop owners will be helped to market the products and services so that they can be easily reached by customers and they will be helped to get the products and services that are needed by their pets easily.
- Build with Golang, Echo Framework, MySQL adn GORM for manage repository, Xuri Excelize for Export List Product Selling to Excel, FTP to store Image Product to server, Xendit API for Payment Gateway, Deploy the project on [Okteto](https://ellashella24.cloud.okteto.net).

<p align="right">(<a href="#top">back to top</a>)</p>

## High Level Architecture

HLA design for this project shown in the picture below

<img src="images/HLA-rev-3.jpeg" alt="hla" width="800" height="462" >

<br />

<p align="right">(<a href="#top">back to top</a>)</p>

## Tech Stack
### RESTful-API
- [Go](https://go.dev/)
- [Echo Framework](https://echo.labstack.com/) - Go Framework
- [MySQL](https://www.mysql.com/) - SQL Database
- [GORM](https://gorm.io/index.html) - ORM Library
- [aws-s3](https://s3.console.amazon.com/s3) - Upload File
- [midtrans](https://www.midtrans.com/ - Payment Gateway

### Deployment
- [Docker](https://www.docker.com/) - Container Images
### Collaboration 
- [Trello](https://trello.com/) - Manage Project
- [Github](https://github.com/) - Versioning Project

<p align="right">(<a href="#top">back to top</a>)</p>

## Code Structure
This project use Layered Architure to organized each components into spesific function  

### Structuring
  ```sh
    AIRBNB-App-Project2
    ├── configs                        
    │     └──config.go                # Contains list of configuration of the project
    ├── constants                     
    │     └──constants.go             # Contains list constant variable
    ├── delivery                      
    │     ├──templates                # Contains list of http request format based on the result from controller 
    │     │   └── httpRes.go          # Contains list of http request format
    │     ├──controllers              # Contains list of component that receive the request and return a response
    │     │   └── user
    │     │     │   ├── formatter.go  # Contains list of request format for each function on the controller
    │     │     │   ├── user_test.go  # Contains list of function for test each function on the controller
    │     │     │   └── users.go      # Contains list of controller for each entity
    │     ├──middlewares              # Contains list of all middleware 
    │     │   ├── JwtAuth.go          # Contains list of function to config middleware basic auth
    │     │   ├── JwtMiddleware.go    # Contains list of function to config middleware token
    │     │   └── formatter_res.go    # Contains list of response format for each function on the controller
    │     └──routes  
    │         └── routes.go           # Contains list of route to access each function on controller  
    ├── entities                      # Contains model all entity
    │     └── user.go                 # Contains model for spesific entity
    ├── node-output                   # Contains list of documentation
    │     └── open-api-swagger.yaml  
    ├── repository                    # Contains list of functions that process the request and stores it in database
    │     ├── database   
    │           ├── user_test.go            # Contains list of function for test each function on the repository
    │           └── user.go                 # Contains list of repository for each entity
    │    └── erd   
    │         └── altaProject.drawio                 # Contains list of relations database
    ├── utils                         
    │     ├── mysqldriver.go          # Contains list of function to config MySQL type database
    │     ├── aws.go                  # Contains list of function to config aws s3
    │     ├── midtrans.go             # Contains list of function to config payment getaway
    │     └── hashPassword.go         # Contains list of function to generate password
    ├── .env                          # Contains list of environment variable to run the project 
    ├── .gitignore                    # Contains list of directory/file name that will igonored when push project
    ├── go.mod                  
    ├── go.sum 
    ├── docker-compose.yaml 
    ├── dockerfile 
    ├── main.go                       # Contains list of component that need to be executed first to run the app
    └── README.md    
  ```

### Unit Test
Coverage result on all functions is 99.2% which the most functions have reached 100% coverage. Coverage result for each function shown in the picture below

<img src="images/coverage-result-ver-2.jpg" alt="coverage-result">

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->
## Contact
* Ade Mawan - [Github](https://github.com/ademawan) 
* Faliq Adlan - [Github](https://github.com/faliqadlan) 

<p align="right">(<a href="#top">back to top</a>)</p>
