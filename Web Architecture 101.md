# Web Architecture 101

![Modern web application architecture overview](https://cdn-images-1.medium.com/max/1600/1*K6M-x-6e39jMq_c-2xqZIQ.png)

## 1. DNS

## 2. Load Balancer

### Horizontal application scaling vs vertical application scaling

### horizontal scaling means that you scale by adding more machines into your pool of resources whereas

### vertical scaling means that you scale by adding more power to an existing machine

### In web development, you (almost) always want to scale horizontally because to keep it simple, stuff breaks. Load balancers are the magic sauce that makes scaling horizontally possible

## 3. Web Application Servers

### They typically communicate with a variety of backend infrastructure such as databases, caching layers, job queues, search services, other microservices, data/logging queues, and more

## 4. Database Servers

### The industry is aligning on SQL as an interface even for NoSQL databases

## 5. Caching Service

### A caching service provides a simple key/value data store that makes it possible to save and  look up information in close to 0(1) time

## 6. Job Queue & Servers

### Job queues store a list of jobs that need to be run asynchronously. The simplest are first-in-first-out (FIFO) queues though most applications end up needing some sort of priority queuing system

## 7. Full-text Search Service

### The most popular full-text search platform today is Elasticsearch though there are other options such as Sphinx or Apache Solr

## 8. Services

## 9. Data

### A typical pipeline has three main stages:

### 1. The app sends data, typically events about user interactions, to the data "firehose" which provides a streaming interface to ingest and process the data

### 2. The raw data as well as the final transformed/augmented data are saved to cloud storage

### 3. The transformed/augmented data is often loaded into a data warehouse for analysis

## 10. Cloud storage

## 11. CDN

### CDN stands for “Content Delivery Network” and the technology provides a way of serving assets such as static HTML, CSS, Javascript, and images over the web much faster than serving them from a single origin server
