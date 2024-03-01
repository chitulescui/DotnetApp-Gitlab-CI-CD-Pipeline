# PizzaPlace-DevOps-Nexus

TODO: YAML files for CI/CD pipelines specially developed for GitLab services. 

# Getting Started
TODO: Execute the following steps in order to import or duplicate this repository. 
1. Clone this repository locally.
   ```
        git clone https://github.com/chitulescui/DotnetApp-Gitlab-CI-CD-Pipeline.git
   ```
2. Clone this repository to your Azure DevOps own repository.
   ```
        git clone --bare https://github.com/EXAMPLE-USER/OLD-REPOSITORY.git
   ```
    Mirror Push to Another repository:
   ```
        cd OLD-REPOSITORY.git
        git push --mirror https://github.com/EXAMPLE-USER/NEW-REPOSITORY.git
   ```
    Remove the temporary local repository you created earlier
   ```  cd ..
        rm -rf OLD-REPOSITORY.git
   ```

# Clone repository
1. Clone the repository 
# Build, Restore and Publish
TODO: Create your CI pipeline to build and pack your .csproj file 
1. Build & Pack 
   Create your pipeline based on .gitlab-ci.yml file. 
# Download artifact and deploy to Github Artifacts 
TODO: Create your CD pipeline to publish your artifact to Github Artifacts (User has to change the subscription details and working folders specified in YML file)
1. Download & Push to Github Artifacts - **WebAppSwk**


Run the following commands:
1. Add Github source to your project:
```
dotnet nuget add source --username username --password "password" --store-password-in-clear-text --name "name" "https://nuget.pkg.github.com/chitulescui/index.json"
```
2. Push nuget package to Github
```
dotnet nuget push "bin/Release/WebAppSwk.1.0.0.nupkg" --api-key "api-key" --source "name"
```
# Run Docker containers for each application
Docker image file was configured with port exposed to : 8080. 


Run docker container with the following comand:
```
docker compose up --build
```
