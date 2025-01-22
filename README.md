# JokesWebApp

![Front App Img](JokesWebApp/wwwroot/images/FrontAppPage.jpg)

## Overview

JokesWebApp is a web application built using ASP.NET Core that allows users to view, create, and manage jokes. This project serves as a demonstration of modern web application development with Entity Framework Core, MVC architecture, and SQL Server for data storage.

## Features

- **Browse Jokes**: View a list of jokes stored in the database.
- **Create Jokes**: Add new jokes with a title and content.
- **Edit/Delete Jokes**: Modify or remove existing jokes.
- **Responsive Design**: Works across devices with modern styling.

## Prerequisites

To run this project, ensure you have the following installed:

- [.NET SDK](https://dotnet.microsoft.com/download) (version 6.0 or higher)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) or LocalDB (bundled with Visual Studio)
- [Visual Studio Code](https://code.visualstudio.com/) or any preferred IDE for .NET development
- Entity Framework Core CLI tools

## Setup Instructions

### Clone the Repository

```bash
git clone https://github.com/your-username/JokesWebApp.git
cd JokesWebApp
```

### Configure the Database

1. Open the `appsettings.json` file and ensure the connection string matches your local environment:
   ```json
   "ConnectionStrings": {
       "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=aspnet-JokesWebApp;Trusted_Connection=True;MultipleActiveResultSets=true"
   }
   ```
2. Apply migrations to create the database schema:
   ```bash
   dotnet ef database update
   ```

### Run the Application

1. Launch the application:
   ```bash
   dotnet run
   ```
2. Open a browser and navigate to [https://localhost:5001](https://localhost:5001).

## Project Structure

- **Controllers**: Handle HTTP requests and map them to views or APIs.
- **Models**: Represent the data structure and handle business logic.
- **Views**: Define the HTML templates for the UI.
- **Data**: Includes the `DbContext` and migration configurations for Entity Framework Core.
- **wwwroot**: Contains static files like CSS, JavaScript, and images.

## Technologies Used

- **Framework**: ASP.NET Core MVC
- **Database**: SQL Server with Entity Framework Core
- **Frontend**: Razor Views with Bootstrap
- **IDE**: Visual Studio Code

## Deployment

To deploy the application:

1. Publish the application:
   ```bash
   dotnet publish -c Release
   ```
2. Deploy the published files to a web server like IIS or Azure App Service.

## Contributing

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push the branch:
   ```bash
   git push origin feature/YourFeature
   ```
5. Create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
