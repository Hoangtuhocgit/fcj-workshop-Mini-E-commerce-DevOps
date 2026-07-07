---
title : "Verify Local Stack"
date : 2024-01-01 
weight : 2
chapter : false
pre : " <b> 5.3.2 </b> "
---

#### Verification objective

After containers are running, verify that the application responds correctly and business flows can be completed. Verification includes automated smoke tests, database checks, and manual UI testing.

#### Frontend smoke test

~~~powershell
.\scripts\smoke-local.ps1
~~~

~~~bash
./scripts/smoke-local.sh
~~~

The expected result is HTTP 200 from the frontend on port 8080.

![smoke-local.ps1 results (live capture)](/images/5-Workshop/5.3-local-docker-compose/smoke-local-live.png)

#### PostgreSQL check

~~~powershell
.\scripts\verify-platform-db.ps1
~~~

This script verifies connectivity to PostgreSQL in Docker Compose. It confirms the platform database is working before comparing with RDS in the AWS environment.

![verify-platform-db.ps1 results (live capture)](/images/5-Workshop/5.3-local-docker-compose/verify-db-live.png)

#### UI verification

Manual verification steps:

1. Open <code>http://127.0.0.1:8080</code>.
2. Browse the product list and confirm data displays correctly.
3. Select a product and add it to the cart.
4. Open the cart and enter test payment details.
5. Confirm the order completion page displays correctly.

![Product detail page (live capture)](/images/5-Workshop/5.3-local-docker-compose/local-product-real.png)

![Cart and checkout form (live capture)](/images/5-Workshop/5.3-local-docker-compose/local-cart-real.png)

![Completed order (live capture)](/images/5-Workshop/5.3-local-docker-compose/local-checkout-real.png)

{{% notice note %}}
The full checkout flow is tested on Docker Compose. On AWS EKS, Phase 1 focuses on core services and does not deploy all supporting services.
{{% /notice %}}

#### Stop the local environment

~~~powershell
docker compose down
~~~

To also remove volumes:

~~~powershell
docker compose down -v
~~~

#### Result

After this step, you can conclude that the application runs stably in the local environment and is ready for AWS deployment.
