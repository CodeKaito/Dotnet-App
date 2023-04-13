# Installing .NET and Creating Your First App with Visual Studio Code

## Introduction

This repository is a step-by-step guide to creating a .NET application from scratch. With the help of this guide, you will learn how to use the .NET framework to develop powerful and efficient applications in the C# programming language. From setting up your development environment to publishing and deploying your app, this repository covers everything you need to know to create a polished and professional application in .NET. Whether you are a beginner or an experienced developer, this guide will help you master the fundamentals of .NET and build applications that meet your business needs. So, dive in and start creating your own .NET applications today!

This guide will walk you through the process of installing .NET on your machine and creating and deploying your first .NET application using Visual Studio Code.

## Prerequisites

Before you get started, you will need the following:

- A computer running Windows, macOS, or Linux
- Visual Studio Code (download it [here](https://code.visualstudio.com/download))
- .NET SDK (download it [here](https://dotnet.microsoft.com/download))

## Installing .NET

1. Download the .NET SDK from the official [.NET website](https://dotnet.microsoft.com/download) for your operating system.
2. Run the installation package and follow the prompts to complete the installation.

## Creating Your First .NET Application

1. Open Visual Studio Code, and select `View` > `Terminal`.
2. In the terminal, navigate to the directory where you want to create your new .NET application.
3. Type the following command to create a new console application:
   
   ```bash
   dotnet new console -n MyFirstApp
   ```
   
   This will create a new directory called "MyFirstApp" with a basic .NET console application inside.
   
4. To open the new project in Visual Studio Code, type the following command:
   
   ```bash
   code MyFirstApp
   ```
   
   This will open the "MyFirstApp" directory in Visual Studio Code.

## Running Your Application

1. In Visual Studio Code, select `View` > `Terminal` to open the terminal.
2. In the terminal, navigate to the directory where your .NET application is located.
3. Type the following command to run the application:
   
   ```bash
   dotnet run
   ```
   
   This will compile and run your application.

## Deploying Your Application

1. In Visual Studio Code, select `View` > `Explorer` to open the file explorer.
2. Navigate to your .NET application directory, and open the `.csproj` file.
3. Select `Debug` > `Start Without Debugging` to build and run your application.
4. Once the application is running, open your web browser and navigate to `http://localhost:5000` to view your deployed application.

## Deploying the Application on the Web

Now that we have created our first .NET application, let’s deploy it on the web.

1. Open a terminal or command prompt.
2. Navigate to the myapp directory.

```bash
cd /path/to/myapp
```

3. Run the following command to create a new .NET web application.

```bash
dotnet new web -o mywebapp
```

4. Change the directory to mywebapp.

```bash
cd mywebapp
```

5. Open the Startup.cs file in your favorite code editor.

```bash
code Startup.cs
```

6. Replace the contents of the file with the following code that configures the web application to serve a "Hello, World!" message.

```csharp
using Microsoft.AspNetCore.Builder;
using Microsoft.AspNetCore.Hosting;
using Microsoft.AspNetCore.Http;
using Microsoft.Extensions.DependencyInjection;
using Microsoft.Extensions.Hosting;

namespace mywebapp
{
    public class Startup
    {
        public void ConfigureServices(IServiceCollection services)
        {
        }

        public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            if (env.IsDevelopment())
            {
                app.UseDeveloperExceptionPage();
            }

            app.UseRouting();

            app.UseEndpoints(endpoints =>
            {
                endpoints.MapGet("/", async context =>
                {
                    await context.Response.WriteAsync("Hello, World!");
                });
            });
        }
    }
}
```

7. Save the file, and close the code editor.
8. Navigate back to the mywebapp directory and run the following command to build the web application.

```bash
dotnet build
```

9. Run the following command to start the web application.

```bash
dotnet run
```

Testing the Application

1. Open your web browser and navigate to [http://localhost:5000](http://localhost:5000).
2. You should see a "Hello, World!" message displayed on the page.

## Deploying a .NET Application on Azure with GitHub

This document outlines the process of deploying a .NET application on Azure using GitHub. It is assumed that you have a basic understanding of the Azure platform and have a GitHub repository that contains your .NET application.

### Prerequisites

- An Azure account
- A resource group created in Azure
- A GitHub repository containing your .NET application
- Visual Studio (optional)

### Step 1: Create a Deployment Center

1. Navigate to your Azure portal.
2. Select your resource group from the left-hand side menu.
3. Click on the "Add" button at the top of the page.
4. Search for "Deployment Center" in the search bar and select it.
5. Click on the "Create" button.
6. Select "GitHub" as the source control.
7. Authenticate with your GitHub account and select the repository containing your .NET application.
8. Click "Save".

### Step 2: Configure Build Options

1. After creating the Deployment Center, click on the "Configure" tab.
2. Select the build provider that matches your application's version of .NET.
3. Configure the build options as needed.
4. Click "Save".

### Step 3: Configure Deployment Options

1. After configuring the build options, click on the "Deployment options" tab.
2. Select the deployment method that matches your application's architecture.
3. Configure the deployment options as needed.
4. Click "Save".

### Step 4: Deploy Your Application

1. After configuring the deployment options, click on the "Overview" tab.
2. Click "Sync" to begin the deployment process.
3. Wait for the deployment to complete.
4. Navigate to your application's URL to verify that it is working correctly.

Congratulations! You have successfully installed .NET, created your first .NET application, and deployed it on the web! This is just the beginning of what you can do with .NET. Start exploring the many features and possibilities of .NET to build powerful and modern applications.
