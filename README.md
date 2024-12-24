# Project Title

## Overview

This project consists of a .NET API and a React frontend application. The API provides backend services, while the React app serves as the frontend interface.

## Prerequisites

- [.NET 6 SDK](https://dotnet.microsoft.com/download/dotnet/6.0)
- [Node.js](https://nodejs.org/) (version 14 or higher)
- [MySQL](https://www.mysql.com/) (for the database)

## Getting Started

### .NET API

1. **Navigate to the API directory:**
   ```bash
   cd /path/to/dotnet_api_tutorial
   ```
2. **Restore dependancies:**
   ```bash
   dotnet restore
   ```
3. **Update the connection string and JWT in `appsettings.json`:**

   ```json
   {
     "ConnectionStrings": {
       "DefaultConnection": "Server=localhost;Port=3306;Database=<your_database>;User=<your_username>;Pwd=<your_password>;"
     },
     "Logging": {
       "LogLevel": {
         "Default": "Information",
         "Microsoft.AspNetCore": "Warning"
       }
     },
     "AllowedHosts": "*",
     "JWT": {
       "Issuer": "<your_issuer>",
       "Audience": "<your_audience>",
       "SigningKey": "<your_signing_key>" // e.g. "Iv1.1b2d3e4f5g6h7i8j9k0l"
     }
   }
   ```

4. **Run the migrations to set up the database:**
   ```bash
   dotnet ef migrations add init
   dotnet ef database update
   ```
5. **Run the API:**
   ```bash
   dotnet run
   ```

## React Frontend

1. **Navigate to the frontend directory:**
   ```bash
   cd /path/to/react_frontend_tutorial
   ```
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Start the development server:**
   ```bash
    npm start
   ```

## Project Structure

### .NET API

- `Program.cs`: Entry point of the application.
- `Startup.cs`: Configures services and the app's request pipeline.
- `Controllers/`: Contains API controllers.
- `Models/`: Contains data models.
- `Data/`: Contains database context and migrations.

### React App

- `src/`: Contains the source code for the React app.
- `public/`: Contains static assets.
- `package.json`: Manages project dependencies and scripts.

## Scripts

### .NET API

- `dotnet run`: Runs the application.
- `dotnet build`: Builds the application.
- `dotnet test`: Runs tests.

### React App

- `npm start`: Starts the development server.
- `npm run build`: Builds the app for production.
- `npm test`: Runs tests.
- `npm run eject`: Ejects the app from create-react-app.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Credits

- **Teddy Smith**: [Github](https://github.com/teddysmithdev) | [Youtube](https://www.youtube.com/@TeddySmithDev)
