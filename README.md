<img width="890" height="656" alt="download" src="https://github.com/user-attachments/assets/32330fd0-7ebc-48ce-9b1f-5b9f5fa6f7bb" /># API-Design-and-Management
A comprehensive guide to building, documenting, securing, and scaling production-ready APIs that developers love to use.

---

# Understanding API(Application Programming Interface):
* **API** is defined as a communication method between two devices, not limited to computers.
* The term “API” originated in the 1960s, initially referring to any action within an application.
* Around 2000, the concept evolved with RESTful APIs and network interfaces becoming prominent.
* APIs facilitate a client-server model where the client sends requests and the server responds.

## OSI Model and Layer 7 (Application Layer):
* **OSI** Model is a Conceptual model that have **7** distinct layer to send data over network.
* APIs operate at the **application layer** (Layer 7), which manages protocols like HTTP.
* Understanding the OSI model is crucial for grasping how APIs function within network communication.
<img width="1150" height="757" alt="image" src="https://github.com/user-attachments/assets/4630523f-992b-4939-ba3c-bef929cf57e9" />

---
## HTTP Methods Overview:
* Mention of HTTP request methods such as GET, POST, PUT, DELETE.
* These methods are essential for RESTful API interactions.
<img width="1146" height="620" alt="image" src="https://github.com/user-attachments/assets/713ac493-725f-4363-82ee-e68833e47210" />

---
## Practical API Server Setup Using Flask (Python):
* Demonstrates creating a simple API server using Flask, a popular Python web framework.
* Steps include:
  * Installing necessary packages.
  * Writing Python code to define a Flask app.
  * Creating endpoints (routes) that respond to HTTP requests.
  * Running the server locally on localhost at port 5000.
<img width="1625" height="879" alt="image" src="https://github.com/user-attachments/assets/8b783719-a234-42bb-96e1-50058e318b34" />

* Testing the server response via terminal or browser to confirm it handles requests properly.
* Example shows how to define a resource and return JSON responses.
<img width="1728" height="356" alt="image" src="https://github.com/user-attachments/assets/b04f98d0-951c-44ad-8954-3b32099fcf13" />

## Basic API Request-Response Flow:
* Client sends a request to the server.
* Server processes the request and sends back a response with status codes.
* Understanding response codes and JSON payloads is part of API basics.

---

# API Types

* APIs enable communication between software components by providing specific services.

## 📊Types of APIs
**Public APIs (Open APIs):**
* Available publicly for external developers to trade or interact with services.
* Security is critical to prevent abuse (e.g., DDoS attacks).
* Companies provide these APIs with usage policies and return mechanisms.

**Partner APIs (B2B):**
* Used between businesses under agreements or licenses.
* Integration is secured and controlled, allowing one company to provide services to another.

**Internal APIs:**
* Used within a company to enable communication between internal systems or components.
* Aims to clarify and streamline internal processes.

**Composite APIs:**
* Execute multiple API requests in a single call.

## 🔧 Development Approaches
- All API types can be designed using either:
* API Architectural Style (e.g., REST, GraphQL)
* API Standard Protocol (e.g., SOAP, gRPC)
<img width="1139" height="647" alt="image" src="https://github.com/user-attachments/assets/8a8b8e1c-d538-438b-89d1-9299332e816d" />

---
# API Architecture vs API Protocols

## 🏗️ **API Architecture Style**
**The high-level structural design** that governs how APIs are built, interact with systems, and expose functionality and data. It focuses on standards, patterns, and best practices rather than strict technical rules.

**Example:** REST (Representational State Transfer) - an architectural style for distributed systems

## 📡 **API Protocol**
**A set of strict rules and standards** that define exactly how software components communicate. It specifies the format of requests/responses, transmission methods, and communication restrictions.

**Example:** SOAP (Simple Object Access Protocol) - a messaging protocol for web services

---

## 🎯 **Quick Comparison**

| Aspect | API Architecture | API Protocol |
|--------|------------------|--------------|
| **Focus** | Structural design & patterns | Communication rules & formatting |
| **Flexibility** | High (guidelines, not strict rules) | Low (strict specifications) |
| **Example** | REST, GraphQL | SOAP, gRPC, JSON-RPC |
| **Purpose** | How to think about API design | How APIs actually communicate |
<img width="1135" height="661" alt="image" src="https://github.com/user-attachments/assets/bcc6c64c-8ebb-4d85-ad72-c24cb53063ea" />

---

**SOAP (Simple Object Access Protocol)**
* One of the earliest API protocols, developed by Microsoft.
* Uses XML for message formatting, making it language-agnostic but relatively slower due to XML parsing.
* Operates over application layer protocols like HTTP or SMTP.
* Requires WSDL (Web Services Description Language) files to describe the API interface.
* WSDL includes namespaces, headers (metadata), parameters, and error handling mechanisms.
* Tools exist (e.g., XC command) to generate source code from WSDL files for easier API consumption.
* SOAP is strict, standardized, supports multiple interfaces in one service, and includes built-in security features.
<img width="1140" height="658" alt="image" src="https://github.com/user-attachments/assets/4feef999-afe9-4dd1-8bc8-3280c1e3ee7b" />

---

# RESTful APIs vs. GraphQL

## 📁 Core Concepts & Architecture

* **Resource**: An entity exposed by an API (e.g., User, Post, Comment).
* **REST API**: Uses multiple endpoints, each dedicated to a specific resource, utilizing HTTP verbs (GET, POST, PUT, DELETE) to manipulate data.
* **GraphQL**: A query language for APIs that operates via a single endpoint, allowing client-defined queries to return exactly the data requested.
* **Graph Structure**: Represents natural, interconnected relationships between data entities (User → Post → Comment).

---

## 🔷 RESTful API Concepts & Limitations

RESTful APIs use resources as fundamental building blocks. Each resource corresponds to a specific entity or data type, and standard HTTP verbs operate directly on these resources:
* **Creating a user**: `POST /user`
* **Retrieving a user**: `GET /user/{id}`

### 🚨 Challenges of REST in Complex Systems
When dealing with complex relationships (such as social networks where users interact by posting, commenting, and liking), REST can become cumbersome:
1.  **Multiple Endpoints**: Separate endpoints are required for each resource and action (`/user`, `/post`, `/comment`), exploding the API footprint.
2.  **Inconsistent Naming**: Endpoint design and naming conventions quickly become confusing and difficult to maintain.
3.  **Relational Complexity**: Handling deeply nested relational data is less straightforward, resulting in either:
    * **Over-fetching**: The server returns unnecessary fields (e.g., fetching a profile returns full histories, passwords hashes, metadata).
    * **Under-fetching**: The server returns too little data, forcing the client to fire multiple consecutive HTTP requests to get related info.

---

## 🚀 Introduction to GraphQL

GraphQL is a **query language for APIs** designed to overcome traditional REST constraints by shifting data control directly to the client.

### 📸 Architectural Overview: Client-Server Patterns

Below is a breakdown of how architectural patterns map visually between REST and GraphQL paradigms:

#### 1. The REST Communication Pattern
In a REST system, fetching a user and their complex relational metadata requires multiple distinct endpoints and structural iterations.

<img width="890" height="656" alt="download" src="https://github.com/user-attachments/assets/46f903ca-16ed-4530-9227-52f14cf3e901" />
*Figure 1: REST Multiple Endpoints vs Rigid Resource Structures.*

#### 2. The GraphQL Single Endpoint Shift
GraphQL simplifies data retrieval. Instead of querying multiple endpoints, the client pushes a custom declarative payload into a single gateway.

<img width="1656" height="733" alt="Screenshot 2026-05-19 174940" src="https://github.com/user-attachments/assets/69b7a166-d838-47af-858c-1933c45ebea6" />
*Figure 2: Client-Driven Declarative Data Fetching via a Single GraphQL Endpoint.*

---

## ⚙️ GraphQL Core Mechanisms

* **Single Endpoint Gateway**: All operations run through one interface (typically `POST /graphql`), drastically reducing API clutter.
* **Query Type**: The main entry point for all incoming read requests.
* **Types and Fields**: A strict schema definition that strictly maps the shape of the data and outlines exactly what fields are queryable.

### 📸 Query Implementation & Payload Matching
The key feature of GraphQL is that the response structure mirrors the query structure exactly. 

<img width="1323" height="657" alt="Screenshot 2026-05-19 175058" src="https://github.com/user-attachments/assets/707b58d3-5d52-40e2-92bc-0b46717b7ce7" />
*Figure 3: Executing a Precise Field Query and Receiving a Structured JSON Mirror Response.*

---

## 📊 Detailed Comparison: REST vs. GraphQL

| Aspect | REST | GraphQL |
| :--- | :--- | :--- |
| **Endpoints** | Multiple (one per resource/action) | Single endpoint (typically `POST /graphql`) |
| **Data Fetching** | Fixed JSON responses defined by the server | Client specifies exactly what fields to return |
| **Handling Relations** | Requires multiple network calls or nested endpoints | Natural graph representation traversed natively |
| **Flexibility** | Less flexible; server controls payload shape | Highly flexible; client controls payload shape |
| **Over/Under-fetching** | Common issues across scaled applications | Completely avoided by using precise element queries |

---

## 🛠️ Social Network Use Case Example

Consider a social application where users interact via posts, comments, likes, and emojis:
* **The REST Approach**: The client must invoke `/users/{id}` to find the author, then invoke `/users/{id}/posts` to pull text, and finally trigger multiple `/posts/{id}/comments` queries to construct the timeline UI.
* **The GraphQL Approach**: The client fetches the user, their posts, and nested comments sequentially using a single query string:

```graphql
query GetFeed {
  user(id: "3") {
    name
    posts {
      title
      comments {
        text
        author {
          name
        }
      }
    }
  }
}
```

## 📌Final Takeaways
- GraphQL is completely independent of the backend implementation, database layer, or programming language—it is strictly a query specification.
- GraphQL queries can take parameter inputs to generate dynamic, tailored server logic.
- GraphQL does not replace REST or gRPC entirely; it complements them, serving as an exceptional tool for aggregating complex, highly relational data structures efficiently.

---

