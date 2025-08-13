Challenge 1 Wordpress
Description
The objective of this challenge is to have the participant search through the posts on the page and find the hidden flag within the comments

Solution
1. Open the web browser and visit the webpage on localhost:8081. Browse through the pages and note all the page URLs used in each post.
Use the terminal to make a GET request to find the hidden comment including the flag.
'Curl GET http://localhost:8081/?p=4 | grep FLAG'
<!-- FLAG{Wordpress-exploit-flag} -->



Recreating this challenge
Recreating this challenge is simple, however requires a few steps.

Use Docker to GET WordPress version 4.7.0 and deploy it.
Run through the administration page with default credentials.
Create multiple posts, in one of the posts hide the flag using the html or code section of the page and enter a comment of the flag
<!-- FLAG{Wordpress-exploit-flag} -->

Create a Docker image of the WordPress instance and MariaDB container, and host it on your Docker Hub by pushing it.
Create a Docker Compose file that pulls the same instance of the challenge.

This completes the recreation of this CTF Challenge.
