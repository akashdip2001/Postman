# Postman

# **Chapter 1: Your First API Request – *Getting Books from the Library API***  

In this step of my Postman journey, I learned how to make my **first API request** to retrieve all books in a library catalog. Here's how it unfolded:  

---

### 🌟 **What I Learned**:
1. **HTTP Methods**:  
   - The API documentation taught me that HTTP methods (GET, POST, PUT, DELETE) are like verbs that define the type of action I want to perform.  
   - In this case, I used **GET** because I was retrieving data.  

2. **Request URL**:  
   - A URL includes:
     - **Protocol**: `https://`
     - **Host**: `library-api.postmanlabs.com`
     - **Path**: `/books`  

3. **Response Status Codes**:  
   - I encountered a **200 OK** status code, meaning my request was successful.  
   - I also learned about other status codes like 4xx (client errors) and 5xx (server errors).  

---

### 🛠 **Task Completed**:  
- I created a new request in Postman:  
  - **Method**: GET  
  - **URL**: `https://library-api.postmanlabs.com/books`  
- I sent the request and received a response containing a **JSON array of book objects**.  

---

### 📝 **Takeaways**:  
- APIs are built around conventions, but **reading the documentation** is key to understanding how to use them.  
- Postman makes it easy to interact with APIs and view responses in real-time.  

This chapter felt like opening a treasure chest of information—my first API request! 🚀

![Screenshot (219)](https://github.com/user-attachments/assets/39386e02-7cc5-41e4-9971-bb740a48fcb0)

## Explane

### Steps to Make Your First API Request: **Get Books**

#### **1. Add a New Request**
1. Open Postman.
2. Inside your Collection:
   - Click **"Add a request"**.
   - Alternatively, hover over the Collection name, click the three dots (**⋮**), and select **"Add request"**.
3. **Name the Request**:
   - Enter the name **"get books"**.

#### **2. Configure the Request**
1. Set the **Request Method**:
   - Use the dropdown near the request name to select **GET**.
2. Enter the **Request URL**:
   - Paste the URL:  
     **`https://library-api.postmanlabs.com/books`**.

#### **3. Save Your Work**
1. Use the shortcut:
   - Windows: **Ctrl + S**.
   - Mac: **Command + S**.

#### **4. Send the Request**
1. Click the **Send** button (usually in blue).
2. Observe the Response Section:
   - Check the bottom half of Postman for the response.

---

### **Interpreting the Response**
- The response will be in **JSON format** and include an **array of book objects**.  
   Example:
   ```json
   [
       { "id": 1, "title": "Book Title 1", "author": "Author Name" },
       { "id": 2, "title": "Book Title 2", "author": "Author Name" }
   ]
   ```
- Note: The content might differ due to real-time updates by other users.

---

### **Key Concepts: HTTP Request Components**
#### **1. Request Method**
- **GET**: Retrieve data.
- Other Methods:
  - **POST**: Create data.
  - **PUT/PATCH**: Update data.
  - **DELETE**: Remove data.

#### **2. Request URL**
- Structure: **`<protocol>://<host>/<path>`**
  - Protocol: **https://**
  - Host: **library-api.postmanlabs.com**
  - Path: **/books**
- This forms the endpoint: **`https://library-api.postmanlabs.com/books`**

#### **3. Response Status Codes**
- **200 OK**: Successful response.
- Other Common Status Codes:
  - **201 Created**: New resource created.
  - **400 Bad Request**: Invalid request format.
  - **401 Unauthorized**: Missing or incorrect credentials.
  - **404 Not Found**: Resource doesn’t exist.
  - **500 Internal Server Error**: Server issue.

---

### **Summary Table: Request Configuration**
| Field            | Value                                              |
|-------------------|----------------------------------------------------|
| **Method**        | GET                                                |
| **URL**           | https://library-api.postmanlabs.com/books          |
| **Expected Status** | 200 OK                                           |
| **Response Format** | JSON                                             | 

**Congratulations!** You’ve successfully retrieved a list of books using an API request. 🎉

```json
[
    {
        "id": "613fc957-d07b-42b3-b9d7-553eccb47f40",
        "title": "The Prince",
        "author": "Mchiavelli",
        "genre": "fiction",
        "yearPublished": 1513,
        "checkedOut": true,
        "isPermanentCollection": false,
        "createdAt": "2024-11-19T20:30:01.863Z"
   }
]
```
| [View All GET Requests](get%20books.json) |
| --- |

---

# **Chapter 2: Request Parameters – *Using Query Parameters to Filter Results***  
## Variables in Postman

In this step, I learned about **query parameters** and how they allow us to refine API requests by adding filters or extra data. Here's what I did:  

---

### 🌟 **What I Learned**:
1. **What are Query Parameters?**  
   - Query parameters are **key-value pairs** added to the end of the request URL.  
   - Syntax:  
     ```
     <base_url>?<key1>=<value1>&<key2>=<value2>
     ```
   - They allow for dynamic filtering, as seen in:  
     ```
     GET https://some-api.com/photos?orientation=landscape&size=500x400
     ```

2. **Practical Example**:  
   - A Google search query like `q=postman` in the URL:  
     ```
     https://www.google.com/search?q=postman
     ```
     uses a query parameter (`q`) to return results for "Postman."

3. **When to Use Query Parameters**:
   - To filter, sort, or add optional data to responses.
   - Reading the **API documentation** is key to understanding which parameters are available.

---

### 🛠 **Task Completed**:
1. **Filtered Fiction Books**:  
   - I duplicated the `get books` request in Postman, renamed it `get fiction books`, and added a query parameter:  
     - **Key**: `genre`  
     - **Value**: `fiction`  
   - Postman updated the request URL automatically:  
     ```
     https://library-api.postmanlabs.com/books?genre=fiction
     ```

2. **Sent the Request**:
   - I clicked **Send** and received a **200 OK** response with an array of books, but this time, only those in the "fiction" genre.  

---

### 📝 **Takeaways**:
- **Query Parameters** are a powerful way to customize API requests.  
- Postman’s **Params tab** makes it easy to add and manage query parameters visually.
- This exercise emphasized the importance of **API documentation** in discovering parameter options.  

Filtering data by genre was like flipping through the pages of a library catalog to find the exact shelf I needed. Onward to the next chapter! 📚✨

![Screenshot (220)](https://github.com/user-attachments/assets/5a3cd88e-41f0-4653-8bcb-8eca280ea708)
![Screenshot (222)](https://github.com/user-attachments/assets/41a5fa19-8f76-41fe-803b-1da4c8ba5e40)
![Screenshot (225)](https://github.com/user-attachments/assets/d5fcdd10-0721-49e5-bfcd-cb4e06741066)

### I don't want all books ---> [Postman Library API v2 documentation](https://documenter.getpostman.com/view/15567703/UVyxRtng)

![Screenshot (226)](https://github.com/user-attachments/assets/9252fd04-1ee7-49df-bca3-dc31deffe805)
![Screenshot (227)](https://github.com/user-attachments/assets/e45245f1-6447-49ef-8fe3-beef61501c74)
![Screenshot (229)](https://github.com/user-attachments/assets/b458f5c7-167f-41e3-86d0-d7ce33b3739e)

### Now I want a particular book --> by ID

![Screenshot (230)](https://github.com/user-attachments/assets/2dede524-af3b-4d77-a693-e0ed5e522d86)
![Screenshot (231)](https://github.com/user-attachments/assets/df09069a-b81f-4bad-aea2-f6a047abf34a)
![Screenshot (232)](https://github.com/user-attachments/assets/e4fa7536-535b-4860-917d-2618e86efc98)
![Screenshot (233)](https://github.com/user-attachments/assets/f58804b8-e201-41a4-b6a0-d0f31500057e)

