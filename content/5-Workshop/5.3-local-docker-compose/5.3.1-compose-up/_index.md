---
title : "Start Docker Compose"
date : 2024-01-01 
weight : 1
chapter : false
pre : " <b> 5.3.1 </b> "
---

#### Objective

This step starts the full application stack on your local machine. When complete, containers must be in a running or healthy state, and the frontend must be accessible at the local address.

#### Create the environment file

At the repository root, create the local configuration file if it does not already exist:

~~~powershell
cp .env.example .env
~~~

The <code>.env</code> file contains variables for Docker Compose, especially PostgreSQL configuration. This file is for local use only and should not be committed to Git.

#### Build and run the stack

~~~powershell
docker compose up --build -d
~~~

Expected output on success:

~~~text
[+] Building 4/4 ... DONE
[+] Running 11/11
 ✔ Container mini-ecommerce-devops-postgres-1   Healthy
 ✔ Container mini-ecommerce-devops-redis-1      Healthy
 ✔ Container mini-ecommerce-devops-frontend-1   Started
 ✔ Container mini-ecommerce-devops-cartservice-1         Started
 ✔ Container mini-ecommerce-devops-checkoutservice-1     Started
 ✔ Container mini-ecommerce-devops-productcatalogservice-1 Started
~~~

The <code>--build</code> flag ensures images are built from the current source code. The <code>-d</code> flag runs containers in the background so you can continue checking status and logs.

![docker compose up -d results (live capture)](/images/5-Workshop/5.3-local-docker-compose/compose-up-live.png)

{{% notice info %}}
The first build may take 10 to 20 minutes because the project includes multiple runtimes such as Go, .NET, Node.js, and Python. Subsequent runs are usually faster thanks to Docker layer cache.
{{% /notice %}}

#### Check containers

~~~powershell
docker compose ps
~~~

The expected result is that core services are in a running state. For Redis or PostgreSQL, a healthy status (when health checks are configured) is the preferred outcome.

![docker compose ps results on a live machine](/images/5-Workshop/5.3-local-docker-compose/compose-ps-screenshot.png)

#### Follow logs when needed

~~~powershell
docker compose logs -f frontend
docker compose logs -f cartservice
~~~

Logs help isolate errors by service. For example, if the frontend cannot load the product catalog, check the product catalog service; if the cart fails, check cartservice and Redis.

#### Services in Docker Compose

| Service | Role |
|---------|------|
| <code>frontend</code> | Web UI |
| <code>productcatalogservice</code> | Product catalog |
| <code>cartservice</code> | Cart handling and Redis connection |
| <code>checkoutservice</code> | Checkout orchestration |
| <code>currencyservice</code> | Currency conversion |
| <code>paymentservice</code> | Payment simulation |
| <code>emailservice</code> | Order confirmation email simulation |
| <code>shippingservice</code> | Shipping cost calculation |
| <code>redis</code> | Cart state storage |
| <code>postgres</code> | Platform database |

#### Access the UI

Open a browser at:

~~~text
http://127.0.0.1:8080
~~~

![Online Boutique home page (live capture)](/images/5-Workshop/5.3-local-docker-compose/local-home-real.png)

If the home page displays normally, proceed to functional verification in section 5.3.2.
