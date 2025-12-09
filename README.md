# API-Design-and-Management
A comprehensive guide to building, documenting, securing, and scaling production-ready APIs that developers love to use.

---

### Understanding API(Application Programming Interface):
* **API** is defined as a communication method between two devices, not limited to computers.
* The term “API” originated in the 1960s, initially referring to any action within an application.
* Around 2000, the concept evolved with RESTful APIs and network interfaces becoming prominent.
* APIs facilitate a client-server model where the client sends requests and the server responds.

### OSI Model and Layer 7 (Application Layer):
* **OSI** Model is a Conceptual model that have **7** distinct layer to send data over network.
* APIs operate at the **application layer** (Layer 7), which manages protocols like HTTP.
* Understanding the OSI model is crucial for grasping how APIs function within network communication.
<img width="1150" height="757" alt="image" src="https://github.com/user-attachments/assets/4630523f-992b-4939-ba3c-bef929cf57e9" />

---
### HTTP Methods Overview:
* Mention of HTTP request methods such as GET, POST, PUT, DELETE.
* These methods are essential for RESTful API interactions.
<img width="1146" height="620" alt="image" src="https://github.com/user-attachments/assets/713ac493-725f-4363-82ee-e68833e47210" />

---
### Practical API Server Setup Using Flask (Python):
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

---

### Basic API Request-Response Flow:
* Client sends a request to the server.
* Server processes the request and sends back a response with status codes.
* Understanding response codes and JSON payloads is part of API basics.
---

