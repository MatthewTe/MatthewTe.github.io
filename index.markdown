---
layout: default
title: Matthew Teelucksingh's Software Portfoilio
description: "Welcome to my software portfolio. I started as an student at the University of Waterloo where I studied environmental economics. My exposure to field data collection techniques early on fueled an interest in programming, specifically the processes of collecting and transforming raw data. Since then I have continued to develop these skills by building various projects that ingest, serve and display data in my primary programming language: python. If you think that my skillset can benefit you, I encourage you to have a look at my projects and contact me if you find them interesting!"
---
## Why is my portfolio a generic Cayman styled Github Pages site?
When looking at other people's portfolios I am often surprised by how impressive their front-end styling is, as well as how complicated their tech stack appears to be. Given this trend I feel as if I should justify why my portfolio is built and hosted using GitHub Pages (with the Cayman theme no less). One of the core values I’ve learned during my personal and professional experience with software development is efficiency. **There is no need to re-invent the wheel and add unnecessary complexity to something that already works.** The quicker I can get my portfolio up and running, the more time I have to focus on building and maintaining the actual projects that demonstrate my value to employers. No need to add complexity for complexity’s sake. 


# Projects
Most of my projects revolve around building data ingestion and transformation projects and APIs.

## Online Data Portal
![There is no image for some reason](assets/images/data_portal_screenshot.png)
This Online Data Portal is the project that I have spent most of my time on. Conceptually this data portal is designed to ingest and serve data for my other projects and dashboards. The tech stack is as follows: 
- All services in the project are containerized via Docker containers and orchestrated via docker-compose.
- All load balancing and internal proxy routing is done by an Nginx server. This is the primary entry-point to the application for external traffic.
- The main content that is served to users is done via the Django Web Framework and the Web API’s are built using the Django REST Framework toolkit.
- On the back-end, pipelines that extract, transforms and ingest external data are scheduled and executed by a Celery task queue which uses Redis as a messages broker. 
- All of the data is stored on a PostgreSQL database.
- The entire service is hosted on Digital Ocean.

This project is at the heart of all of my personal projects and is available externally to anyone who wants to make use of the data. You can read more about the project [here](#) or if you want to make use of the APIs you can [check out the docs](#).  

## Personal Research Site
![There is no image for some reason](assets/images/research_site_thunbnail.png)
Another personal project, the research site was built to help me organize my thoughts and research on topics that I am interested in. It is another django web project that performs CRUD operations, allowing me to add items relevant to research such as personal blog posts, citations, books I have read, etc. 
- All services in the project are containerized via Docker containers and orchestrated via docker-compose.
- The project renders content via the Django Web Framework. Said content is styled by bootstrap css and JavaScript on the front-end. Static files are hosted using Digital Ocean Spaces and served by django’s S3 Digital Ocean plugin.
- The project is hosted on Digital Ocean.
- All of the data is stored on a PostgreSQL database. 

You can view the [source code](https://github.com/MatthewTe/research_site) or you can [visit the site](http://159.223.180.214/) and see what topics I am interested in researching/writing about!