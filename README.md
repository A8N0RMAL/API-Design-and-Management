# API-Design-and-Management
A comprehensive guide to building, documenting, securing, and scaling production-ready APIs that developers love to use.

---

## Understanding API(Application Programming Interface):
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

### Basic API Request-Response Flow:
* Client sends a request to the server.
* Server processes the request and sends back a response with status codes.
* Understanding response codes and JSON payloads is part of API basics.

---

## API Types

* APIs enable communication between software components by providing specific services.

### 📊Types of APIs
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

**🔧 Development Approaches**
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
