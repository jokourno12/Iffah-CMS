# Command
1. create SQL server developer
    - curl -fsSL https://packages.microsoft.com/keys/microsoft.asc | sudo gpg --dearmor -o /usr/share/keyrings/microsoft-prod.gpg
    - if receive warning: curl https://packages.microsoft.com/keys/microsoft.asc | sudo tee /etc/apt/trusted.gpg.d/microsoft.asc
    - curl -fsSL https://packages.microsoft.com/config/ubuntu/22.04/mssql-server-2022.list | sudo tee /etc/apt/sources.list.d/mssql-server-2022.list
    - sudo apt-get update
    - sudo apt-get install -y mssql-server
    - sudo /opt/mssql/bin/mssql-conf setup
    - choose developer and input password Qwerty123
    - systemctl status mssql-server --no-pager
    - sqlcmd -S localhost -U sa -P Qwerty123 -C
        - CREATE DATABASE iffah_cms;
2. install dotnet
3. piranha cms
    - dotnet new install Piranha.Templates
    - dotnet new piranha.mvc -n iffah_cms
    - dotnet restore
    - dotnet run
4. connect to database
    - dotnet add package Piranha.Data.EF.SQLServer
    - dotnet add package Piranha.AspNetCore.Identity.SQLServer
    - updating
        - appsettings.json
        - Program.cs
    - dotnet run


# Architecture
1. Operational Excellence
2. Security
3. Reliability
4. Performance Efficiency
5. Cost Optimization
6. Sustainability