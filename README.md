
### **Node.js Backend Developer Test: Weather Retrieval API**

#### **Objective**

Create a Node.js application that fetches current weather data for a given location using the OpenWeatherMap API. The application should be designed following Domain-Driven Design (DDD) and Clean Architecture principles.

#### **Requirements**

1.  **Language**: Node.js with Express.js.
2.  **Architecture**: Follow DDD and Clean Architecture principles.
3.  **External API**: Use the OpenWeatherMap API to retrieve weather data.
4.  **Deployment**: Provide instructions to run the application locally.

#### **User Story**

As a user, I want to input a user location and receive the current weather information for that location via an API.

#### **Technical Specifications**

-   **API Endpoint**:
    
    -   **GET /api/weather?lat={latitude}&lng={longitude}**
    -   **Response**: JSON object containing the current weather data.
-   **Input Parameters**:
    
    -   `lat`: Latitude of the query city (ex. 41.4)
    -   `lng`: Longitude of the query city (ex. 2.17)
-   **Output**:
    
    -   Status code `200` for successful requests.
    -   Status code `500` for server errors.

#### **Steps to Follow**

1.  **Domain Layer**
    
    -   Define the core domain model for your application. For example, create a `Weather` entity that contains the necessary attributes like temperature, humidity, weather description, etc.
    -   Implement the necessary domain services that encapsulate the business logic for fetching and processing weather data.
2.  **Application Layer**
    
    -   Develop application services or use cases that handle the application's workflow logic. For example, create a `GetWeatherByCityUseCase` that orchestrates the process of fetching weather data from the OpenWeatherMap API.
    -   Use interfaces to define contracts between the domain and infrastructure layers.
3.  **Infrastructure Layer**
    
    -   Implement the OpenWeatherMap API client within this layer. The API client should interact with the external API and return data in a format that your application can use.
    -   Ensure proper error handling and mapping of external data to your domain model.
4.  **Interface Adapter Layer**
    
    -   Develop the Express.js controllers to handle incoming HTTP requests and route them to the appropriate use cases.
    -   Implement data transfer objects (DTOs) if necessary to map between the incoming request data and the domain model.
5.  **Testing**
    
    -   Write unit tests for domain services and use cases.
    -   Implement integration tests for the API endpoint.

#### **Evaluation Criteria**

1.  **Code Structure and Organization**:
    
    -   Clear separation of concerns and adherence to DDD and Clean Architecture principles.
    -   Proper use of interfaces and dependency injection.
2.  **API Functionality**:
    
    -   Correct and efficient retrieval of weather data.
    -   Appropriate error handling and response codes.
3.  **Code Quality**:
    
    -   Readability, maintainability, and adherence to coding standards.
    -   Unit and integration tests coverage.
4.  **Documentation**:
    
    -   Clear instructions for setting up and running the application.
    -   Well-documented code and API endpoints.

#### **Submission**

-   The candidate should submit their solution in a public GitHub repository.
-   Include a `README.md` file with instructions on how to set up, run, and test the application.