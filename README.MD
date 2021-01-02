# BoxBilling

### How to run

Build image for landing page.

```sh
$ docker build -t landing:1.0.0 -f landingpage/Dockerfile .
```

Build image for boxbilling.

```sh
$ docker build -t tbb:1.0.0 -f boxbilling/Dockerfile .
```

run docker compose

```sh
$ docker-compose up
```

open phpmyAdmin http://localhost:8005/ and import databases :

- import structure.sql to boxbilling database
- import content.sql to boxbilling database

Verify the deployment by navigating to your server address in your preferred browser.

boxbilling http://localhost:8004/

landing page http://localhost:3000/

#### NOTES

- Credential applied for all

```sh
username : boxbilling
password : boxbilling
```

sometimes you can't login to phpMyAdmin but it's ok wait for around 30s, because mysql need time to execute add user script, but if after 30s you still can't login re-run the bb-mysql image.
