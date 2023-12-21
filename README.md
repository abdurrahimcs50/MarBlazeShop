# MarBlazeShop Project Documentation

## Table of Contents
1. Introduction
2. Features
3. Installation Guide
4. Demo
5. Screenshots
6. Contributing
7. Acknowledgments
8. License

<a name="introduction"></a>
## Introduction
MarBlazeShop is an eCommerce application built with Python and Django Framework. It offers a wide range of features to provide a seamless shopping experience for customers.

<a name="features"></a>
## Features
1. **Accounts Management**: Design and implement a custom user model. Create user registration. Build user login and logout views. Implement password reset functionality. Implement My Account functionalities (profile editing, password change, order management).
2. **Store Management**: Design and implement models for products and categories. Create views for displaying a list of products, product details, and category-wise listings. Include search and filtering options for products.
3. **Product Image Gallery**: Implement a feature to upload and display unlimited images for each product.
4. **Shopping Carts Management**: Implement a shopping cart system. Allow users to increment, decrement, and remove items from the cart. Integrate with the checkout process.
5. **Order Management**: Develop an order management system for seamless order placement and tracking. Implement a checkout process. Generate and store orders with related information. Send order confirmation emails to users. Implement after-order functionalities (reduce quantity of sold products, clear the cart). Generate an invoice for the order. Create an Order completion page.
6. **Payment Gateway**: Incorporate a secure and reliable payment processing system.
7. **Post-Order Functionalities**: Code functionalities for post-order processes like reducing the quantity of sold products, sending order confirmation emails, clearing the cart, and generating an invoice upon order completion.
8. **Review and Rating System**: Implement an interactive star rating system, allowing even half-star ratings. Implement a review and rating system. Use interactive rating stars. Allow half-star ratings.
9. **Customer Account Management**: Develop functionalities for customers to edit their profile, change profile pictures, update passwords, and manage orders.

<a name="installation-guide"></a>
## Installation Guide

### Using Virtual Environment

1. **Clone the Repository**: First, clone the repository to your local machine. You can do this with the following command:
    ```bash
    git clone https://github.com/abdurrahimcs50/MarBlazeShop.git
    ```

2. **Navigate to the Project Directory**: Use the command `cd MarBlazeShop` to navigate into the project directory.

3. **Set Up the Virtual Environment**: Set up a virtual environment using `venv` (you might need to install it first). Here's how you can create a new virtual environment and activate it:
    ```bash
    python3 -m venv env
    source env/bin/activate

    #for windows
    env\Scripts\activate

    ```

4. **Install Dependencies**: Make sure Python installed on your machine. Then, install the necessary libraries. goto `requirements.txt` file directory `cd src`, you can use the following command:
    ```bash
    pip install -r requirements.txt
    ```

5. **Set Up the Environment Variables**: In the `src` folder, you'll find `.env.example`. Rename it to `.env` and replace the placeholder values with your actual data.

6. **Run Migrations**: Apply the migrations using the following command:
    ```bash
    python manage.py migrate
    ```

7. **Start the Server**: Finally, you can start the server using the following command:
    ```bash
    python manage.py runserver
    python Manage.py makemigrations
    python manage.py migrate
    ```

Now, you should be able to access the application at `localhost:8000` (or whatever port you've set) in your web browser.

### Using Docker Compose

1. **Clone the Repository**: First, clone the repository to your local machine. You can do this with the following command:
    ```bash
    git clone https://github.com/abdurrahimcs50/MarBlazeShop.git
    ```

2. **Navigate to the Project Directory**: Use the command `cd MarBlazeShop` to navigate into the project directory.

3. **Set Up the Environment Variables**: In the `src` folder, you'll find `.env.example` Rename it to `.env` and  `prod.env.example`. Rename it to `prod.env` and replace the placeholder values with your actual data.

4. **Build and Run the Docker Compose**: Use the following command to build and run your application:
    ```bash
    #for local testing
    docker-compose -f local.ym build
    docker-compose -f local.ym up

    #for production testing
    docker-compose -f production.yml build

    # For detached (background) mode, use:
    docker-compose -f production.yml up -d
    ```
    **Visit http://localhost:8000 in your web browser for local development or http://localhost or http://127.0.0.1 for production.**

    ##Execute Management Commands

   ```bash

    # Use the following commands to manage your Django application within the Docker container:

    # For local development:
    docker-compose -f local.yml run --rm web python manage.py makemigrations
    docker-compose -f local.yml run --rm web python manage.py migrate
    docker-compose -f loc.yml run --rm web python manage.py collectstatic
    docker-compose -f local.yml run --rm web python manage.py createsuperuser
    docker-compose -f local.yml run --rm web python manage.py startapp app_name
    docker-compose -f local.yml run --rm web python manage.py shell

    # For production:
    docker-compose -f production.yml run --rm web python manage.py makemigrations
    docker-compose -f production.yml run --rm web python manage.py migrate
    docker-compose -f production.yml run --rm web python manage.py collectstatic
    docker-compose -f production.yml run --rm web python manage.py createsuperuser
    docker-compose -f production.yml run --rm web python manage.py startapp app_name
    docker-compose -f production.yml run --rm web python manage.py shell
    
    ```

<a name="demo"></a>
## Demo
A demo of this application can be found at this link. [Check Live Demo](#)

<a name="screenshots"></a>
## Screenshots
Here are some screenshots of the application:

- Home Page:
- Product Page:

<a name="contributing"></a>

## Contributing

👏 Contributions are welcome! Whether you're reporting bugs, suggesting enhancements, or contributing code, your efforts are appreciated.

## Ways to Contribute

1. **Reporting Bugs**: If you encounter issues or unexpected behavior, please create a new issue. Be sure to provide detailed information about the problem and steps to reproduce it.

2. **Suggesting Enhancements**: Have an idea for improvement? Feel free to suggest it by creating an issue and describing your enhancement.

3. **Code Contributions**: Want to contribute code? Check the existing issues and pull requests to avoid duplication. Make your changes, test them locally, and submit a pull request.

4. **Writing Documentation**: If you find something that needs better documentation or want to contribute to our docs, that's fantastic! Clear documentation helps everyone understand and use the project effectively.

5. **Providing Feedback**: Share your experiences, suggestions, or concerns. Your feedback helps us make the project better.

6. **Sharing the Project**: If you find this project useful, consider sharing it with others. Spread the word on social media, tech communities, or among your colleagues. The more, the merrier.

<a name="acknowledgments"></a>
## Acknowledgments

Special thanks to the Python, Django, PostgreSQL, Docker, communities for their invaluable contributions.
<a name="license"></a>
## License

This project is licensed under the MIT License.

