# Candy Store

Welcome to Candy Store, a Node.js web application designed for an e-commerce platform. Created and deployed on an EC2 instance by Kashi, this project brings the sweetest shopping experience to the digital world.

### Prerequisites
Ensure you have the following installed:
- Node.js
- npm (Node Package Manager)
- Docker (optional for containerization)
- Amazon Linux EC2 instance (for Git as SCM and target server).
- Install Git and Docker on both the server and the target instance.
- Git as Source Code Management (SCM) tool.
- Docker Hub to store Docker images.




##Steps to Deploy the Candy-Store Application on ec2 server ##

1.📦 Set Up the Application:
Check the application is running on the local machine (EC2 instance).

2.📝 Create Dockerfile:
Write a simple Dockerfile using RUN npm install.

3.🔨 Build Docker Image:
Build the Docker image using this Dockerfile: docker build -t kashi779/candy-store:01 .

4.🚀 Create Docker Container:
Run the application inside a container on port 3000 (node app.js): docker run --rm -t -p 3000:3000 kashi779/candy-store:01

5.📤 Push Docker Image to DockerHub:
After logging in, push the Docker image to DockerHub: docker push kashi779/candy-store:tagname

6.⬇️ Pull Docker Image on Target Server:
Pull the latest Docker image on the target server to create a container to run the application.

7.📦 Create Container from Latest Docker Image:
On the target EC2 instance, run the following command: docker run -d --rm -p 3000:3000 candy-store:latest

8.🌐 Expose Necessary Port:
Ensure the application is listening on port 3000.

9.🔗 Access the Running Application:
Open your web browser and navigate to http://localhost:3000 or your public IP address with port 3000.

10.✅ Successful Deployment:
Hence we have successfully deployed the Node.jsapplication on the server!





###Contributing
Contributions are welcome! Please create a pull request or open an issue to discuss your ideas.


###License
This project is licensed under the MIT License. See the LICENSE file for details.


###Contact
If you have any questions or need further assistance, feel free to ask!. For any inquiries or support, 
please reach out to Kashi at gsagre99@gmail.com


###Acknowledgements
- Express.js for providing the server framework.
- Docker for containerization.
- GitHub for version control and repository hosting.







