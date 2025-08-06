# Travel_Memory_project

This documentation outlines the step-by-step process to locally develop and deploy the Travel Memory MERN stack application (MongoDB, Express, React, Node.js) using a MacBook, followed by preparing for scalable deployment on AWS with domain integration through Cloudflare.

Begin by ensuring all necessary development tools are available on your MacBook. Use Homebrew to install Node.js, MongoDB (for local testing), nginx, Git, and any preferred code editors or utilities. After cloning the project from GitHub, separately set up both backend and frontend environments. For the backend, install dependencies, configure your .env file with the appropriate MongoDB connection string, and launch the server. For the frontend, install packages and adjust the API endpoint in urls.js to communicate with the locally proxied backend via nginx. Run both servers to verify seamless communication.

Configure nginx on your Mac to act as a reverse proxy. This ensures consistency with production deployment and allows your React app to make API requests to the backend under a unified base URL. Update nginx’s configuration file to set the correct ports and proxy rules, and always remember to reload nginx after changes.

For deployment, leverage your MacBook to push the fully tested application code to GitHub, from where it will be provisioned to AWS EC2 instances. Use the AWS CLI on your Mac to manage cloud infrastructure, including launching and configuring EC2 instances, setting up security groups, and creating load balancers for scalability and resilience. SSH from your MacBook into each EC2 instance for configuration, mirroring the successful local setup steps.

Integrate Cloudflare by pointing your custom domain’s DNS records to the AWS Load Balancer (via a CNAME) and directly to your EC2 instances (via an A record if required). This enables secure, performant, and scalable access to your application globally. Supplement your deployment with clear documentation, screenshots captured using Mac shortcuts, and a detailed architecture diagram (drawn in draw.io) to visualize infrastructure components and connections.

With this workflow, your MacBook serves as a complete development and DevOps environment, providing a smooth path from local coding to internet-ready, scalable deployment. All package management, scripting, configuration, and orchestration can be efficiently executed from macOS, ensuring a streamlined and reproducible deployment process suitable for modern professional development settings.
