<img width="1235" height="576" alt="image (18)" src="https://github.com/user-attachments/assets/93cbd48d-4636-4ae1-a43a-719ab033558f" />
<img width="959" height="490" alt="image (19)" src="https://github.com/user-attachments/assets/8b41b0f5-2ddd-41ba-91fa-899b24925c5d" />
![image (1)](https://github.com/user-attachments/assets/70d122a8-f3ea-4e46-ab0a-24e69a5fd6ea)
![image (2)](https://github.com/user-attachments/assets/0b8b09ee-d7a3-411e-a126-2657826aa3aa)
![Create a single page diagram for the following workflow  - visual selection](https://github.com/user-attachments/assets/74cf251c-f506-42d8-bac4-5d8f16287256)
![image (3)](https://github.com/user-attachments/assets/63905fd2-3191-4d71-bf3b-1e2011850abc)
![image (4)](https://github.com/user-attachments/assets/a6228bd3-6f39-4d3f-9869-c2864ea51615)
<img width="1854" height="921" alt="image (21)" src="https://github.com/user-attachments/assets/9060389c-0265-41ee-8f28-17019fe8a2b4" />
<img width="1916" height="877" alt="image (22)" src="https://github.com/user-attachments/assets/7b71d12a-bede-484e-a0f3-915f937e2e26" />
<img width="1800" height="141" alt="image (23)" src="https://github.com/user-attachments/assets/047ecd34-730f-47e7-b6b1-09a44d570037" />
![image (5)](https://github.com/user-attachments/assets/4d09dbed-3c1c-48c8-86f6-0f563a8fc9b9)
![image (6)](https://github.com/user-attachments/assets/c7791d7b-8491-4f54-b4a4-45beb5f90909)
![image7](https://github.com/user-attachments/assets/ef7542ba-66ec-4251-bdad-2e2308a519ac)


Log Processing
A folder contains application logs.
Each log line may have levels: ERROR, INFO, WARNING, DEBUG.
A Python/Java program continuously reads logs line by line.
Based on the log type:
If ERROR, send to Error Logging REST API.
If WARNING, send to Warning Logging REST API.
If INFO, send to Info Logging REST API.
If DEBUG, send to Debug Logging REST API.
REST API & Storage
REST APIs are hosted on AWS.
Logs are stored in a database, which maintains counts of each log type (error, warning, info, debug).
UI Dashboard
A UI application queries the database.
It displays the counts of each log type in real-time.
Distributed Setup
Multiple servers will send logs simultaneously.
The Java program will continuously push logs to REST APIs.
All components run inside Docker containers.
Test Automation (Unit Testing Scope)
Write unit tests for:
Log file reader (verifying correct classification of log levels).
API caller (ensuring the correct REST endpoint is hit based on log type).
Database writer (verifying counts are updated properly).
UI data fetcher (checking counts match DB values).
Automation scripts should simulate multiple servers sending logs.
Tests must validate:
Correct log segregation.
Accurate API calls.
Proper DB updates.
UI correctly reflects counts.

