# OPAD - A Collaborative Text Editor
Distributed text editors are commonly used to support collaborative editing for software or document development. However, many existing solutions work with documents on the server; they do not support direct collaboration between two clients working with locally stored documents. 
Refer to this [document](https://github.com/O-Pad/.github/blob/main/DSCD%20Project%20Slides.pdf) for more details. 

**We propose a distributed text editor for real-time collaboration that stores the files locally.**

## Architecture

### O-Pad Client
O-Pad client is the application running on the user side that manages the text editor and sends and receives updates regarding changed files.

### Message Broker 
Maintains exchanges for each file being edited live and a queue for each user. 

![](https://github.com/O-Pad/.github/blob/main/profile/images/1.png)

### File Tracker
Maintains a map of files and the list of online O-Pad clients working on that file, i.e. the collaborators. Facilitates joining for the first time.

### RabbitMQ Server
It manages message exchanges, for client-client communication.

![](https://github.com/O-Pad/.github/blob/main/profile/images/2.png)

## Tech Stack
![](https://github.com/O-Pad/.github/blob/main/profile/images/3.png)

---
This project was done by [Paras Mehan](https://github.com/parasmehan123/), [Osheen Sachdev](https://github.com/oshhh), [Adwit Singh Kochar](https://github.com/adwitsingh) and [Dushyant Panchal](https://github.com/dushyant18033) as a course group project in Distributed Systems: Concepts and Design with [Dr. Pushpendra Singh](https://www.iiitd.ac.in/pushpendra) at IIIT Delhi during Monsoon 2021 Semester.



