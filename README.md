# Movie Store

This project is aimed at developing the services of a Movie Store application.

## Project Structure

1. **Movie:**
   
   ![image](https://github.com/muhammet-enes-aksoy/Movie-Store/assets/97848966/9d8d6f79-ebd6-49ab-8155-368f70fb3ada)

    - Movie Name
    - Release Year
    - Genre
    - Director
    - Actors
    - Price
        - **Directors and actors should be kept separately. An actor can also be a director, but these are two separate entities.**

3. **Actors:**

   ![image](https://github.com/muhammet-enes-aksoy/Movie-Store/assets/97848966/6a9656b9-e774-469e-875a-e760110ecfd0)

    - First Name
    - Last Name
    - Movies they played in
        - **Multiple actors can play in a single movie, and an actor can have multiple movies.**

5. **Directors:**

   ![image](https://github.com/muhammet-enes-aksoy/Movie-Store/assets/97848966/90bad133-0021-4b40-8894-4eb71935b742)

    - First Name
    - Last Name
    - Movies they directed

7. **Customer:**

   ![image](https://github.com/muhammet-enes-aksoy/Movie-Store/assets/97848966/b76d01ed-5836-4576-a858-70f1b27f8542)

    - First Name
    - Last Name
    - Purchased movies
    - Favorite genres
        - **A customer can have multiple favorite movie genres, and they can purchase a genre multiple times. No need to impose a restriction here.**

9. **Authentication:**

    ![image](https://github.com/muhammet-enes-aksoy/Movie-Store/assets/97848966/328e0fb0-eed4-4d7b-8f9d-68f7a3d2f4af)

    - Login endpoint for customers. Unauthorized users should not be able to make purchases from the application.

11. **Orders:**

    ![image](https://github.com/muhammet-enes-aksoy/Movie-Store/assets/97848966/2cfe9d67-a99c-4a26-8921-bbccda6d3057)

    - The movies purchased by customers should be stored in a structure like "My Orders" with the following properties:
        - Purchasing customer
        - Purchased movie
        - Price
        - Purchase date

## Application Requirements

1. **Movies:**
    - Add/Remove/Update/List Movies

2. **Customers:**
    - Add/Remove Customers

3. **Actors:**
    - Add/Remove/Update/List Actors

4. **Directors:**
    - Add/Remove/Update/List Directors

5. **Movie Purchase:**
    - Customers should be able to purchase a movie through the application.

6. **Purchase History:**
    - Listing purchase data based on customers. Purchased movies can be deleted from the system later. This should not affect the order data.

7. **Film Genres:**
    - Film genres can be created as default when the application is run. There is no need to manage them with services.

## Technical Requirements

1. **Entities:**
    - Entity objects should not be used as input/output.

2. **Models and DTOs:**
    - Models and DTOs should be used where necessary. Objects should be transformable to each other with the help of the AutoMapper library.

3. **Controller:**
    - Service tasks should not be performed in the controller.

4. **Validation:**
    - Each service should have a validation class. The application should be well protected with strict rules, and all possible validations should be implemented.

5. **Exception Handling and Logging:**
    - Exception handling and logging infrastructure should be implemented using middleware.
    - Logging system should be as follows:
        - Every request and response made in the application should be logged to the console.
        - When the application encounters an error or a validation error is thrown, these errors should be logged to the console in a meaningful way.
        - The logging method should not spread throughout the application.
        - When needed, the logging format can be changed by making changes only at one point.

6. **Dependency Injection:**
    - Dependency creation should be avoided in the project. Dependency injection using a DI container should manage dependencies from a single point.

7. **Authentication and Authorization:**
    - The project should implement a basic Authentication and Authorization structure. The purchase endpoint should be an endpoint used only by customers.

8. **Unit Tests:**
    - The project should have unit tests written comprehensively. All tests should run without errors.

9. **Data Consistency:**
    - Data consistency should be considered in deletion services. Records with related data in other tables cannot be deleted.
