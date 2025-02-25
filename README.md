# LLM RAG Chatbot  

The **Academic Advisor Chatbot** project is an AI-driven chatbot designed to help students navigate academic queries related to the Computer Science and Engineering (CSE) department. The chatbot can answer questions about course prerequisites, academic schedules, department policies, and more.

---
## Prerequisites

Make sure the following are installed on your local machine before proceeding:

- [Docker](https://www.docker.com/products/docker-desktop/)

---
## Installation

#### Step 1: Clone the Repository

First, clone the GitHub repository to your local machine using the command below:

```
git clone https://github.com/DrAlzahraniProjects/csusb_fall2024_cse6550_team2.git
```


#### Step 2: Navigate to the Project Directory

Once the repository is cloned, navigate to the project directory location:

```
cd csusb_fall2024_cse6550_team2
```

#### Step 3: Update the Local Repository

Ensure your local repository is up-to-date by running the below command:

```
git pull origin main
```
#### Step 4 : Run the Setup Script:

Make sure Docker is installed and running on your local machine. Use below command to run the Setup Script which builds docker image.

```
python setup.py
```
Get "MISTRAL_API_KEY" from [Team2 Discussions Board](https://csusb.instructure.com/courses/43192/discussion_topics/419700) and paste it on terminal when asked.


If **Step 4** does not work for you use **Step 5** as an alternative to build docker image.

#### Step 5: Build and Run the Docker Image

Make sure Docker is installed and running on your local machine. Build the Docker image by using the following command:

```
docker build -t team2_app .
```

Run the Docker image by using the following command. Make sure you replace the "MISTRAL_API_KEY" with actual key from [Team2 Discussions Board](https://csusb.instructure.com/courses/43192/discussion_topics/419700) 
```
docker run -d -p 5002:5002 -p 6002:6002 -e API_KEY=MISTRAL_API_KEY  team2_app
```
---
## Accessing the Application

Once the docker container starts running, you can access the Academic Advising Chatbot at:

**Accessing Locally Through Docker** 

*App* - http://localhost:5002/team2/

*Jupyter* -  http://localhost:6002/team2/jupyter




