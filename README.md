#  eBay-like e-commerce auction site

Project 2 for CS50’s Web Programming with Python and JavaScript.

## Project Overview
The Commerce Auction Site is a Django project that includes a single app called "auctions." The application facilitates online auctions with features like creating and managing listings, bidding on items, and adding comments. Below is an overview of the project.

## Getting Started

Follow these steps to get the "Commerce" project up and running on your local machine.

### Download the Code

You can obtain the project code by either cloning the repository or downloading the ZIP archive. To clone the repository, open your terminal and run the following command:

```bash
git clone https://github.com/moinuding587/commerce.git
```


### Project Structure

### URLs
- URL configuration for the "auctions" app is defined in `auctions/urls.py`.
- Existing URL routes include:
- Default index route
- Login route
- Logout route
- Register route

### Views
- View functions associated with each URL route are defined in `auctions/views.py`.
- Key views:
- `index_view`: Displays the homepage with auction listings.
- `login_view`: Handles user login and registration.
- `logout_view`: Logs out the user.
- `create_listing_view`: Allows users to create new auction listings.

### Templates
- HTML templates are located in the `auctions/templates/auctions/` directory.
- The main layout is defined in `layout.html`, and it includes conditional rendering based on user authentication.

### Models
- Database models are defined in `auctions/models.py`.
- The existing model is `User`, which inherits from `AbstractUser`.
- To meet the project requirements, you will need to add models for auction listings, bids, comments, and auction categories. You should define the fields for each model as per your application's needs.

## Requirements

### Models
- This application must have at least three additional models: one for auction listings, one for bids, and one for comments.

### Create Listing
- Users can create new auction listings with a title, description, and a starting bid.
- Optionally, users can provide an image URL and specify a category for the listing.

### Active Listings Page
- The default route displays all currently active auction listings.
- For each listing, it should show the title, description, current price, and a photo (if available).

### Listing Page
- Clicking on a listing takes users to a specific page for that listing.
- Users can view all details about the listing, including the current price.
- If a user is signed in, they can add the item to their watchlist.
- Users can bid on the item, provided the bid meets certain criteria.
- Users who created the listing can "close" the auction.

### Watchlist
- Signed-in users can access their Watchlist page, displaying listings they've added to their watchlist.

### Categories
- Users can view a list of all listing categories.
- Clicking on a category name takes the user to a page displaying all active listings in that category.

### Django Admin Interface
- Site administrators can use the Django admin interface to manage listings, comments, and bids.

## Usage

## Prerequisites

Before you get started, make sure you have the following software installed on your machine:

- Python 3
- Python package installer (pip)

## Installation

1. Install the required dependencies, including Django 4, by running the following command in your terminal:

    ```bash
    pip install -r requirements.txt
    ```

2. After cloning the repository, navigate to the project folder.

3. Create new database migrations based on the changes in models:

    ```bash
    python3 manage.py makemigrations
    ```

4. Apply the migrations to the database:

    ```bash
    python3 manage.py migrate
    ```

5. To access the Django Admin Interface, create a superuser with the following command and follow the prompts:

    ```bash
    python3 manage.py createsuperuser
    ```

6. Finally, run the application locally by executing:

    ```bash
    python3 manage.py runserver
    ```

## Usage

Once the server is running, visit the site in your web browser at [http://localhost:8000](http://localhost:8000).

That's it! You've successfully set up and launched the "Commerce" application on your local machine.






 
