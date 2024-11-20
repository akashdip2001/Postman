[<img align="right" alt="python_logo" width="300" src="https://github.com/user-attachments/assets/3d0e35e2-bcca-4042-a6c7-11380c5729bb">](https://postmanstudent.notion.site/GGSOC-Postman-API-Fundamentals-Student-Expert-821795dd2e3f493586f713d2168d1c33)

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

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

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

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# **Chapter 3: Sending Data with POST – *Adding a Book to the Library***  

This chapter introduced me to the **POST** method, which allows us to send data to an API. My task was to add a new book to the library by sending structured data in the request body. Here's what I learned and did:  

---

### 🌟 **What I Learned**:  
1. **What is the Body?**  
   - The **Body** is used to send structured data (e.g., JSON) with requests to create or update resources.  
   - It is commonly used with **POST**, **PUT**, and **PATCH** methods.  

![Screenshot (234)](https://github.com/user-attachments/assets/bc66a6e8-0ccb-4486-9f9d-67dbf9414970)
![Screenshot (235)](https://github.com/user-attachments/assets/72638642-2c8b-4426-80a7-166d15019d0f)

2. **JSON Format for Body Data**:  
   - The data must be structured in **key-value pairs** like this:  
     ```json
     {
     "title": "What is Time ??",
     "author": "Akashdip Mahapatra",
     "genre": "Physics",
     "yearPublished": 2024
      }
     ```
     
![Screenshot (236)](https://github.com/user-attachments/assets/254af363-f430-4f87-8bda-94f6bf8d05a2)

3. **Using Postman's Body Tab**:  
   - Select the **Body** tab in Postman.  
   - Choose **raw** as the data format and set the type to **JSON** for syntax highlighting.  

4. **API Key Authorization**:  
   - Learned about the importance of including an **api-key** in the headers for authorization to avoid a `401 Unauthorized` error.  

---

### 🛠 **Task Completed**:  
1. **Created the "add book" Request**:  
   - **Method**: POST  
   - **URL**: `{{baseUrl}}/books`  
   - **Body**: Added the book data in JSON format.  

2. **Sent the Request**:  
   - Initially received a **401 Unauthorized** response.  
   - This error taught me that APIs often require authentication to ensure secure access.  

---

### 📝 **Takeaways**:  
- POST requests allow us to **create new resources** by sending data in the request body.  
- Structured data like JSON is essential for adding information in a format that APIs can understand.  
- Errors like **401 Unauthorized** highlight the need for proper **authentication**, which I'll address in the next lesson.  

This chapter felt like adding a personal favorite book to the shelves of an ever-growing library—what an exciting moment! 📖✨

### Give Auth on a Request

![Screenshot (238)](https://github.com/user-attachments/assets/e82661d2-1076-48c9-85dd-18777e7b6e74)

### Give Auto on full Folder - **collection level Authorization**

![Screenshot (239)](https://github.com/user-attachments/assets/fdb7f4ca-d3f6-4555-95f1-7af9a1191ef1)
![Screenshot (240)](https://github.com/user-attachments/assets/6802e9e8-f12c-4f5e-aee6-a88e6e2ec311)
![Screenshot (241)](https://github.com/user-attachments/assets/cb726d8b-6bb3-44aa-8f4c-8d6edc73fbbd)

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# **Chapter 4: Introduction to Variables and Scripting – *Logging Data from the API***  

In this chapter, I learned how to use **JavaScript scripting** within Postman to interact with API responses. Here's what I did and learned:  

---

### 🌟 **What I Learned**:  

1. **JavaScript Basics in Postman**:  
   - **Logging data**:  
     - Used `console.log()` to print data to the console:  
       ```javascript
       console.log("Hello world!")
       ```  
   - **Comments**: Added explanations in the script to make it readable:  
     ```javascript
     // This is a single-line comment  
     /* This is a  
        multi-line comment */
     ```  

2. **Postman Scripting Environment**:  
   - Postman allows us to write scripts in the **Pre-request** and **Post-response (Tests)** tabs for automation and response handling.  

3. **Using `pm` Object**:  
   - `pm` is a global Postman object that provides functions to interact with requests and responses.  
   - For example:  
     ```javascript
     console.log(pm.response.json())
     ```  
     This extracts and logs the response JSON from the API.  

4. **Postman Console**:  
   - Located in the lower-left corner, it allows viewing logs, errors, and raw request-response cycles.  

---

### 🛠 **Task Completed**:  

1. **Updated the "add a book" Request**:  
   - Changed the body data to add a new book:  
     ```json
     {
       "title": "The Great Gatsby",
       "author": "F. Scott Fitzgerald",
       "genre": "fiction",
       "yearPublished": 1925
     }
     ```  

2. **Added a Script**:  
   - Opened the **Tests tab** and wrote a script to log the API response:  
     ```javascript
     console.log(pm.response.json())
     ```  

3. **Sent the Request**:  
   - Observed the new book being added successfully.  
   - Opened the **Postman Console** to view the JSON response logged by the script.  

---

### 📝 **Takeaways**:  
- **Scripts in Postman** enhance automation by processing data dynamically.  
- Logging with `console.log()` is a powerful way to debug and inspect API responses.  
- Postman Console is a great tool for tracking request and script execution.  

It was rewarding to see how we could capture data programmatically—like being the librarian who documents each new arrival in the library! 📚✨

![Screenshot (244)](https://github.com/user-attachments/assets/82ab7577-ed59-4caf-a0a2-d3ad17ee1440)

---

### **Response Details**  
- **ID**: `04cd01e2-29ee-42f2-93b3-c41c0e71bb90`  
- **Title**: `"What is Time ??"`  
- **Author**: `"Akashdip Mahapatra"`  
- **Genre**: `"Physics"`  
- **Year Published**: `2024`  
- **Checked Out**: `false` (The book is not checked out yet.)  
- **Permanent Collection**: `false` (It's not part of a permanent collection.)  
- **Created At**: `"2024-11-19T22:34:49.814Z"` (Date and time when the book was added.)  

---

### 🎯 **Achievement**  
- **HTTP Status Code**: `201 Created`  
  - Indicates that the book was successfully added to the library database.  
- The server returned all the details of the newly created book entry, including a unique `id` to reference this book in future requests.

---

### 📘 **Next Steps**  
- Use this `id` in future operations, like retrieving, updating, or deleting this specific book.  
- Continue exploring how Postman handles variables and scripting for automating these tasks! 😊

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

Here’s a summary of how you can **grab the new book ID** and save it as a variable:

---

### **Steps to Save the Book ID as a Collection Variable**
1. **Change the Book Details in the Body Tab**  
   - Go to the **Body tab** of the "add a book" request.  
   - Replace the book details with information about a new book you'd like to add.

   Example JSON:
   ```json
   {
     "title": "The Mysteries of Space",
     "author": "Akashdip Mahapatra",
     "genre": "Astronomy",
     "yearPublished": 2024
   }
   ```

2. **Add the Script to Save the Book ID**  
   - Open the **Post-response tab** in the **Scripts section** of the "add a book" request.  
   - Replace the `console.log()` statement with the following code:
     ```javascript
     // Save the "id" value from the response to a local variable named "id"
     const id = pm.response.json().id;

     // Save the "id" as a collection variable named "id"
     pm.collectionVariables.set("id", id);
     ```
![Screenshot (245)](https://github.com/user-attachments/assets/34af0bfa-306c-4db0-9c9a-1ded9c872fe2)

3. **Save and Send the Request**  
   - Save your changes.  
   - Click **Send** to execute the request.

![Screenshot (246)](https://github.com/user-attachments/assets/b4dcb739-0b08-42ff-bc80-80c7e289b370)

4. **Verify the Variable is Set**  
   - After the request completes successfully (with a `201 Created` status), the script will run, saving the book’s `id` into a collection variable.  
   - To confirm:
     - Click your **Postman Library API v2 collection**.
     - Go to the **Variables tab**.
     - Look for a variable named `id` under **Current Value**. Its value should match the `id` from the response.

---

### **Example of How the ID Variable Works**
You can now use `{{id}}` in subsequent requests within the same collection. For example:
- To retrieve the book by ID:  
  **GET** `https://library-api.postmanlabs.com/books/{{id}}`

![Screenshot (248)](https://github.com/user-attachments/assets/cf1cfca0-6e10-4d29-bfcb-422b28e566e5)
![Screenshot (249)](https://github.com/user-attachments/assets/4f428542-90a6-4fd7-97a4-c0cedae76d83)

---

### **Next Steps**
With this automation in place, you’re ready to use the stored `id` variable in future tasks like updating, deleting, or checking out the book. Keep going—you’re doing great! 😊

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

## Halfway Test
### Steps to Complete the Halfway Test for Your Collection

1. **Fork the "Collection Test" into Your Workspace**  
   - Open the provided link for the "Collection Test" collection.  
   - Hover over the "Collection Test" collection name, click the **three dots**, and select **Create a Fork**.  
   - Choose your workspace, e.g., "Postman API Fundamentals Student Expert," as the destination.  
   - Click **Fork Collection**.

![Screenshot (252)](https://github.com/user-attachments/assets/80be23c1-68b1-4440-80c4-53d37e520b79)
![Screenshot (253)](https://github.com/user-attachments/assets/dcb70c9d-2f52-4076-9a6e-234242827562)

2. **Generate an API Key for Your "Postman Library API v2" Collection**  
   - Navigate to your **Postman Library API v2** collection.  
   - Click **View more actions** (three dots) > **Share** > **Via API**.  
   - Click **Generate New Key**, then **Copy** the generated link.

![Screenshot (254)](https://github.com/user-attachments/assets/ccd8c0a8-30f9-4de9-8eb2-87b7f413a154)
![Screenshot (255)](https://github.com/user-attachments/assets/79ef837e-a84b-4278-bf94-1c54e331119e)

3. **Set the Submission Variable in the Forked "Collection Test"**  
   - Go to the forked **"Collection Test"** collection.  
   - Open the **Variables** tab.  
   - Locate the variable named `submission`. Paste the API key link you copied earlier into both the **Initial Value** and **Current Value** columns.  
   - Click **Save** to persist the changes.

![Screenshot (256)](https://github.com/user-attachments/assets/233d9e44-2060-4001-bac1-b6a6a50db63b)
![Screenshot (257)](https://github.com/user-attachments/assets/39b39cd8-6b93-4c1b-ad62-bde27be7c026)

4. **Send the Halfway Test Request**  
   - In the **"Collection Test"** collection, find the request titled **Halfway Test**.  
   - Send the request by clicking the **Send** button.

5. **Check the Test Results Tab**  
   - If everything is correct, you will see:  
     **Test Results: 16/16**  
   - If some tests fail (e.g., **Test Results: 14/16**), refer to the **Test Messages** in the response. They provide hints about what needs fixing.

![Screenshot (259)](https://github.com/user-attachments/assets/56e53e52-8c28-4c68-b6f3-57b9be8df9a3)

6. **Resolve Any Errors**  
   - **Test Messages** will specify what’s wrong with your collection. Use these messages as a guide to fix the errors.  
   - Go back to your **Postman Library API v2** collection and:  
     - Ensure all requests are correctly configured as per the earlier lessons.  
     - Verify your scripts, query parameters, and headers are properly set.  
   - Save any updates to your collection, then re-send the **Halfway Test** request.

<img width="870" alt="6n2s7wufz2wz5S" src="https://github.com/user-attachments/assets/3c2f92df-5752-46f1-b115-541bd8f9c0f9">

7. **Additional Help**  
   - If you're stuck, revisit previous lessons to double-check your implementation.  
   - Join the [Discord Community](https://discord.com/channels/831210428314157076/1268565927599800423) for support or FAQs.

8. **Celebrate Your Success**  
   - Once you achieve **Test Results: 16/16**, you've successfully completed the halfway milestone! 🎉  

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# **Chapter 5: PATCH and DELETE – *Task: Checkout your book***  

### Steps to Checkout a Book Using the PATCH Method

1. **Create the "checkout a book" Request**  
   - In your **Postman Library API v2** collection:  
     - Hover over the collection name, click the **three dots**, and select **Add Request**.  
     - Name this new request **"checkout a book"**.

![Screenshot (260)](https://github.com/user-attachments/assets/f4a9d5b9-a2bd-4d85-99e2-119519669342)

2. **Configure the Request**  
   - **Request Method**: Set it to **PATCH**.  
   - **Request URL**: Enter the following:  
     ```text
     {{baseUrl}}/books/:id
     ```  
   - Replace `:id` with `{{id}}`. This dynamically uses the value of the `id` collection variable set during the "add a book" request.

![Screenshot (261)](https://github.com/user-attachments/assets/b5926066-84c8-4535-8a18-5b385865b6f9)

3. **Update the Body with JSON**  
   - Go to the **Body** tab and select:  
     - **raw** as the input type.  
     - **JSON** from the format dropdown.  
   - Add the following JSON data:  
     ```json
     { 
       "checkedOut": true 
     }
     ```

![Screenshot (262)](https://github.com/user-attachments/assets/8b1fc267-a11a-4594-a079-9ce01ff40053)

4. **Ensure Authorization is Properly Set**  
   - The **Authorization** tab should be set to **Inherit from parent**.  
   - This will automatically use the API Key added at the collection level.

5. **Save and Send the Request**  
   - Click **Save** to save the request.  
   - Hit **Send** to make the PATCH request.  

6. **Verify the Response**  
   - If successful, you will receive a **200 OK** status code.  
   - The response body will include the updated details of your book, with the `checkedOut` property set to `true`.  

![Screenshot (263)](https://github.com/user-attachments/assets/7a258a65-23c1-4a1a-891f-d96d993801ad)

7. **Check the Updated Book Data Using the "get book by id" Request**  
   - Open your **"get book by id"** request.  
   - Ensure the `id` path variable is set to `{{id}}`.  
   - Save and Send the request.  
   - You should now see the updated book data, confirming that the `checkedOut` property is `true`.  

### Outcome
You’ve successfully updated the book's `checkedOut` status to true. The library's database now reflects that the book is checked out! 😊 

---

### Steps to Delete a Book Using the DELETE Method

1. **Create the "delete a book" Request**  
   - In your **Postman Library API v2** collection:  
     - Hover over the collection name, click the **three dots**, and select **Add Request**.  
     - Name the new request **"delete a book"**.

2. **Configure the DELETE Request**  
   - **Request Method**: Set to **DELETE**.  
   - **Request URL**: Enter:  
     ```text
     {{baseUrl}}/books/:id
     ```  
   - Replace `:id` with `{{id}}`. This uses the `id` collection variable dynamically set during the "add a book" request.

3. **Check Path Variable**  
   - In the **Params** tab, ensure the `id` path variable is set to `{{id}}`.

4. **Save and Send the Request**  
   - Click **Save** to save the request.  
   - Hit **Send** to delete the book.  

5. **Verify the Response**  
   - A **204 No Content** status code indicates the server successfully deleted the book.  
   - No response body is expected.

![Screenshot (265)](https://github.com/user-attachments/assets/64b3ef25-81f2-4bb1-b95d-965905f2f1f9)
![Screenshot (266)](https://github.com/user-attachments/assets/ba42028c-2096-4721-9c3d-4001e1745f89)

6. **Test If the Book Is Really Deleted**  
   - Without making any changes, **Send the DELETE request again**.  
   - You will get a **404 Not Found** status code.  
   - This confirms that the book no longer exists in the database.

![Screenshot (267)](https://github.com/user-attachments/assets/e7e1d9ac-7fea-4b9b-a69a-d068d0eea308)

---

### Outcome
The book has been successfully deleted from the library database. Trying to delete it again confirms its absence. Another step mastered in managing a library database through APIs! 😊 

---

# **Skillcheck**

Here’s a step-by-step guide to help you successfully complete all tasks in this skill check and pass the test.

---

### **[Task 1] Make the Request**
1. **Create a Request**: 
   - Name your request **"skill check"**.
   - Place it under the **delete a book** request in your collection.

2. **Set Endpoint**:  
   Use the POST method with the endpoint:  
   ```
   https://postman-echo.com/post
   ```
![Screenshot (268)](https://github.com/user-attachments/assets/ddc35ad1-d80e-4d23-98e5-eeba3ff754ba)
![Screenshot (269)](https://github.com/user-attachments/assets/4d9ba5dd-9ca4-4232-a9aa-32d923299091)

---

### **[Task 2] Add a Query Parameter**
1. **Add a Query Parameter**:
   - Go to the **Params** tab.
   - Add the query parameter:
     - **Key**: `movieName`
     - **Value**: Your favorite movie (e.g., `Interstellar`).

![Screenshot (270)](https://github.com/user-attachments/assets/5767546d-a3d2-4cfe-97c4-134a37d0800f)
![Screenshot (271)](https://github.com/user-attachments/assets/874697b1-15f7-4702-9aa9-811088d33433)

---

### **[Task 3] Use a Base URL Variable**
1. **Create a Collection Variable**:
   - Go to the **Variables** tab of your collection.
   - Add a variable:
     - **Key**: `skillcheckBaseUrl`
     - **Initial Value**: `https://postman-echo.com`
     - **Current Value**: `https://postman-echo.com`

2. **Replace the Base URL**:
   - Change the request URL to:  
     ```
     {{skillcheckBaseUrl}}/post
     ```

![Screenshot (272)](https://github.com/user-attachments/assets/17c3515e-3cc3-442b-8430-48f0e331a00d)
![Screenshot (273)](https://github.com/user-attachments/assets/89778b4a-4a05-4615-965b-ba073a5524cc)

---

### **[Task 4] Use API Key Authorization**
1. **Set Authorization**:
   - Go to the **Authorization** tab of the "skill check" request.
   - Choose **API Key** as the authorization type.
   - Configure the API key:
     - **Key**: `student-expert`
     - **Value**: `skillcheck`
     - **Add To**: `Header`

![Screenshot (274)](https://github.com/user-attachments/assets/e9c3ee49-0914-4c19-990c-7f7b17f5d410)
![Screenshot (275)](https://github.com/user-attachments/assets/d30b2733-69b5-4761-935d-3ffe5ed3eb08)

---

### **[Task 5] Add a JSON Body with `actorName`**
1. **Add a Body**:
   - Go to the **Body** tab.
   - Select **raw** and choose **JSON** from the dropdown.
   - Add the following JSON:
     ```json
     {
        "actorName": "<actor_name>"
      }
     ```

2. **Send the Request**:
   - Hit **Send** and ensure you get a successful response (e.g., status `200 OK`).

![Screenshot (276)](https://github.com/user-attachments/assets/27129e7b-2495-4932-b058-f519e4ae4347)
![Screenshot (277)](https://github.com/user-attachments/assets/844b1ef3-a4a4-4aef-80f8-c225a3e2f338)

---

### **[Task 6] Set a Collection Variable Using Post-Response Script**
1. **Write the Post-Response Script**:
   - Go to the **Tests** tab of the "skill check" request.
   - Add the following script:
     ```javascript
     // Parse the JSON response
     var responseJson = pm.response.json();

     // Extract the actorName from the response
     var actorName = responseJson.data.actorName || responseJson.actorName;

     // Set the actorName as a collection variable
     pm.collectionVariables.set("favoriteActor", actorName);

     // Log to confirm
     console.log("favoriteActor set to: " + actorName);
     ```

![Screenshot (278)](https://github.com/user-attachments/assets/6c07f2be-41cd-48de-961d-3c42e43ff99e)

2. **Test the Script**:
   - Send the request again.
   - Go to the **Collection Variables** tab in Postman to confirm that the variable `favoriteActor` is set correctly (e.g., `Matthew McConaughey`).

![Screenshot (279)](https://github.com/user-attachments/assets/8b71e9be-213a-4265-b5af-05a9f9a77e51)

---

### **Test Your Collection Locally**
1. **Check the Collection Order**:
   - Ensure the requests in your **Postman Library API v2 collection** are in the correct order:
     1. Get all books
     2. Get a single book
     3. Add a book
     4. Update a book
     5. Delete a book
     6. Skill check

2. **Run the Collection Test**:
   - Go to the **Final Check** request in the "Collection Test" collection.
   - Send the request.

3. **Check Test Results**:
   - Go to the **Test Results** tab in the response.
   - Confirm that all tests pass (e.g., `Test Results (28/28)`).

---

### **Troubleshooting Tips**
- If some tests fail:
  - Read the test messages carefully to understand what needs fixing.
  - Verify query parameters, variables, body content, and script logic.
  - Ensure your requests are in the correct order.

- If everything is correct, save the collection and retry.

---

### **Final Step: Submission**
After passing all tests, submit your collection following the course instructions to claim your badge!

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# ✅ successfully submit your Postman collection:

---

### **Step 1: Verify Your Collection**
Ensure your collection has **exactly 7 requests in this order**:
1. **Get books**
2. **Get fiction books**
3. **Get book by ID**
4. **Add a book**
5. **Checkout a book**
6. **Delete a book**
7. **Skillcheck**

If the requests are out of order, you can reorder them by dragging and dropping them in the collection tab.

![Screenshot (280)](https://github.com/user-attachments/assets/034026a0-202c-465b-ba3b-ac3932f64d1f)
![Screenshot (281)](https://github.com/user-attachments/assets/d10c4343-c066-4a9b-b5b1-deae8f6dc4ad)
![Screenshot (282)](https://github.com/user-attachments/assets/46c5a76b-d8c4-4910-9d59-6ed49af855b0)
![Screenshot (283)](https://github.com/user-attachments/assets/adf14ae9-4f74-401b-9db3-e6746310b06c)

---

### **Step 2: Check the Submission Variable**
The variable `{{submission}}` must already contain a **public JSON link** to your Postman Library API v2 collection. To confirm:
1. Go to your collection.
2. Click the **three dots (⋮)** next to the collection name.
3. Select **Share Collection**.
4. Ensure **Enable Sharing** is turned ON, and copy the link.
5. Check that this link is set as the value of the `{{submission}}` variable in your environment.

---

### **Step 3: Update the "Submit" Request**
1. **Navigate to the "Submit" Request**:
   - Go to the **"Collection Test"** collection and locate the `submit` request.
2. **Set the Request Method and URL**:
   - Method: `POST`
   - URL: `https://lesson-completion.postmanlabs.com/submit`
3. **Add the Raw JSON Body**:
   - Go to the **Body** tab.
   - Select **raw** and choose **JSON** format from the dropdown.
   - Paste the following JSON:
     ```json
     {
       "email": "akashdip...@aot.edu.in",
       "postmanCollectionJsonUrl": "{{submission}}",
       "publishedCourseId": "2q2jokzsn62y8",
       "lessonId": "go6mgkytvk8u"
     }
     ```
4. **Save the Request**:
   - Click the **Save** button (💾).

---

### **Step 4: Submit the Request**
1. Send the request by clicking the **Send** button.
2. Check the response:
   - If successful, you’ll see a success message, and this lesson will automatically be marked as complete. 🎉
   - If you see a `424` error, follow the troubleshooting steps below.

![Screenshot (285)](https://github.com/user-attachments/assets/94ab22d4-463e-4063-8ae8-a16283677c63)
![Screenshot (286)](https://github.com/user-attachments/assets/f56ee10f-4041-4b85-b671-4388a26e8625)

---

### **Step 5: Troubleshooting Common Errors**
#### **If You Get a 424 Error**
1. Read the error message in the response. It will give hints about what went wrong.
2. Common fixes:
   - Ensure the requests in your collection are in the correct order.
   - Verify the request body for the "Skillcheck" request and ensure:
     - The query parameter `movieName` is correctly added.
     - The `actorName` is correctly sent in the JSON body.
   - Double-check the `post-response script` in the Skillcheck request.
   - Make sure all requests in the collection return the expected responses.

3. Save your changes and re-submit.

#### **If You Get a 500-Level Error**
- Wait for 5 minutes and try submitting again.
- If the issue persists, re-check your submission link or regenerate it by re-sharing your collection.

---

### **Step 6: Completion**
- After passing all tests, refresh the course page.
- If marked complete, proceed to claim your **Postman Student Expert badge**!

Let me know if you encounter any specific issues or errors. I'll guide you through!

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

![Screenshot (287)](https://github.com/user-attachments/assets/520ff4c0-1895-4109-9d11-8eee14782e06)
![Screenshot (288)](https://github.com/user-attachments/assets/335679c0-e884-411a-9cd5-aec4c29b19db)
![Screenshot (289)](https://github.com/user-attachments/assets/64142f08-204c-42d7-a354-0b54b0b056d1)
![Screenshot (290)](https://github.com/user-attachments/assets/be137aa2-0ea7-4e58-9415-0be1f773d5e7)
![Screenshot (291)](https://github.com/user-attachments/assets/dd81d75f-f22f-41a4-9f09-2cd87858a52c)
![Screenshot (292)](https://github.com/user-attachments/assets/24336c46-8668-4faa-b401-2e2924ecede9)

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

[<img src="https://github.com/user-attachments/assets/2d142e94-8ef1-4205-ae56-5873a50ed9ae" width="100%" />](https://www.linkedin.com/posts/akashdip2001_postman-api-certification-activity-7264947968200368128-MHWG?utm_source=share&utm_medium=member_desktop)




