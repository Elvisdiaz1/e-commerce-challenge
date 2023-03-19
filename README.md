# <E_Commerce_Challenge>

![badmath] https://img.shields.io/badge/MIT-blue

## Description

This application was built for the purposes of creating a application that allows you to create a mysql database and interact with it using a server. This e-commerce database server can allow you to view the database, add, update, and delete products, categories, and tags. The application was created by using node.js, express, mysql, sequelize, and mysql2 to connect mysql to node.js. The reason why I did this application was so I can have a application to view the database made with mysql and interact with the database using server routes. I learned how to use sequelize to build database tables and use server routes to perform updates, addition, and deletions to those tables.

## Table of Contents

If your README is long, add a table of contents to make it easy for users to find what they need.

- [Installation](#installation)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)

## Installation

To install this application, you need clone the repository. To clone the repository, you go to the green button on the repository that says "< > Code". Then you can choose to copy either the https url or the ssh url if you have a ssh key. After you copy the link, then you go to your terminal on your computer and in the terminal, you change the current directory to the directory you want to place the cloned repository in and then you type "git clone" and paste the url. Finally, you hit enter and the repository will be on your machine.

## Usage

This is a server based application. You need to activate the mysql datatbase so you have to go to the schema.sql file in the terminal and type "mysql -u root -p" to enter your password. From there, type "source schema.sql". Then you need to go to server.js in your code editor, enter your mysql password and user in the ".env" file, save the file, and enter in the terminal with the server.js file. Then type "npm run seed" to enter the data in the sql database and type "node server" or "npm start" to start the server. Once you started the server, you can use Insomnia to use the URL paths and requests to interact with the database.

To view the database, you can enter "http://localhost:3001/api/products" with a GET request and press the "send" button to view the products database page or change "/products" for "/categories" or "/tags" for their respective pages. To add a product, enter "http://localhost:3001/api/products" with a POST request, enter an object with "product_name" key, a price with the "price" key, and a stock count with the "stock" key, and press the "send" button to create your new product, like this {"product_name":"new item" , "price": 14.99, "stock": 14}. It should be noted that the prices in the products databases are rounded up when you view them. The same can be done with categories and tags, so to do that, you must change the url correct naming and the categories and tags can only create a new name, ex: {"category_name":"new item"} for categories and {"tag_name":"new item"} for tags. To update the products/tags/categories, enter "http://localhost:3001/api/(products or tags or categories)/(id of item goes here)" with a PUT request and at the end of the URL, enter the id of the item you want to update the info for. Make a object and enter the key you want to change, enter the value you want it to change into, and press the "send" button to do the update. So if you want to change the price and stock count for the product you made, then put the item's id in the url and make a object with the price key and change the value, like this { "price": 25.99, "stock": 30}. When you do the GET request, the item will now appear like this: {"product_name":"new item" , "price": 26, "stock": 30}. To delete an item, enter http://localhost:3001/api/(products or tags or categories)/(id of item goes here)" with a DELETE request and at the end of the URL, enter the id of the item you want to delete and press the "send" button to do the deletion. To view any change you made to the database, just do the GET request.

![Tutorial Video](/e-commerce.mp4)

## Credits

Node.js- https://nodejs.org/en

Express.js- https://www.npmjs.com/package/express

Mysql- https://www.mysql.com/downloads/

Mysql2- https://www.npmjs.com/package/mysql2

Sequelize- https://www.npmjs.com/package/sequelize

## License

This application license is: MIT
