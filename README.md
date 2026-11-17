# Marine Guard

Marine Guard is a team project for monitoring coral reef health. Its planned workflows include coral bleaching detection, field observations, alerts, reporting, and task management. The backend in this snapshot contains implemented endpoints for a marine resource library.

## What’s in this repository

| Folder | Contents |
| --- | --- |
| [`AIML-Project/`](AIML-Project/) | Java 21 backend built with Spring Boot, Spring Data MongoDB, and Maven. Contains public and admin library controllers and library category management. |
| [`marineguard-frontend/`](marineguard-frontend/) | Frontend scaffold with placeholders for accounts, observations, alerts, the resource library, reports, and tasks. |

The frontend source files in this snapshot are empty, and its `package.json` has no development or start script. A working frontend and coral bleaching model are needed to run the full platform.

## Run the backend on Windows

1. Install **JDK 21** and make a MongoDB database available.
2. In `AIML-Project/src/main/resources/application.properties`, configure MongoDB using an environment variable before committing the file.

   ```properties
   spring.data.mongodb.uri=${MONGODB_URI}
   ```

3. From the repository root, open PowerShell and run:

   ```powershell
   cd AIML-Project
   $env:MONGODB_URI = "mongodb://localhost:27017/marineguard"
   .\mvnw.cmd spring-boot:run
   ```

   The example assumes local MongoDB. For a hosted database, set the actual connection string in your local environment. Once Spring Boot starts, it uses port **8080** by default.

## License

The backend includes an [MIT License](AIML-Project/LICENSE).
