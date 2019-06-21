# nessus_docker

Software source : [https://www.tenable.com/downloads/nessus](https://www.tenable.com/downloads/nessus)

#### version 8.4.0

# download

```bash
docker pull onthewayzh/nessus
```

# run

```bash
docker run -d --name nessus -p 8834:8834 onthewayzh/nessus
```

# use

Please visit this link : `https://localhost:8834`

Initialize Nessus : 
1. Input username and password
2. Visit the Nessus website for the serial number,url:[https://www.tenable.com/products/nessus/nessus-essentials](https://www.tenable.com/products/nessus/nessus-essentials)
3. Nessus automatic configuration 

If you get an error in step 3, execute the following command:

```bash
docker exec -ti nessus bash    # Entering the container
/opt/nessus/sbin/nessuscli update    # Update Nessus in the container
exit    # Exit the container
```