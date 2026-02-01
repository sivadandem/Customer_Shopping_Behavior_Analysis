# Screen Recording Presentation Script

## Restaurant Admin Dashboard - Video Presentation Guide

### Pre-Recording Checklist

**Before Recording:**

- [ ] Close unnecessary browser tabs
- [ ] Clear browser history/bookmarks bar (optional)
- [ ] Open VS Code with project
- [ ] Open Postman with API collection
- [ ] Open MongoDB Atlas dashboard
- [ ] Open Live Frontend URL in browser
- [ ] Open Live Backend URL in browser
- [ ] Test microphone audio
- [ ] Set screen resolution to 1920x1080
- [ ] Turn off notifications

---

## Video Structure (8-10 minutes)

| Section | Duration | What to Show |
|---------|----------|--------------|
| Introduction | 1 min | Title slide / README |
| Tech Stack | 1 min | README / Architecture |
| Live Demo - Frontend | 3 min | Netlify deployed app |
| API Testing | 2 min | Postman |
| Code Walkthrough | 2-3 min | VS Code |
| Challenges & Conclusion | 1 min | README / Summary |

---

## Complete Script

### SECTION 1: Introduction (1 minute)

**Screen:** Show your GitHub README or a title slide

**Say:**
```
"Hello, my name is [Your Name] and today I'll be presenting my 
Restaurant Admin Dashboard project.

This is a full-stack web application that allows restaurant owners 
to manage their menu items and track customer orders.

The project was built as part of the Eatoes Technical Assessment, 
and it demonstrates my skills in building RESTful APIs, working 
with MongoDB, and creating responsive React applications.

Let me walk you through the project."
```

---

### SECTION 2: Tech Stack (1 minute)

**Screen:** Show README tech stack section or create a simple slide

**Say:**
```
"For this project, I used the MERN stack:

- Frontend: React 18 with hooks for state management
- Backend: Node.js with Express.js for the REST API
- Database: MongoDB with Mongoose ODM
- Deployment: 
  - Frontend is deployed on Netlify
  - Backend is deployed on Render
  - Database is hosted on MongoDB Atlas

Let me show you the live application."
```

---

### SECTION 3: Live Demo - Frontend (3 minutes)

#### 3.1 Menu Management Page

**Screen:** Open your Netlify deployed frontend URL

**Say:**
```
"This is the Menu Management page. As you can see, all menu items 
are displayed in a responsive grid layout.

Each card shows the item name, category, price, and availability status."
```

**Action:** Scroll through the menu items

---

#### 3.2 Search with Debouncing

**Screen:** Click on search bar and type slowly

**Say:**
```
"Let me demonstrate the search functionality. I'll type 'pizza'...

Notice that the search doesn't trigger on every keystroke. 
I've implemented debouncing with a 300 millisecond delay.

This means the API is only called after I stop typing, which 
prevents unnecessary API calls and improves performance."
```

**Action:** Type "pizza" slowly, pause, show results

---

#### 3.3 Category Filter

**Screen:** Click on category dropdown

**Say:**
```
"Users can also filter menu items by category. 
Let me select 'Appetizer'...

Now only appetizer items are displayed. 
I can also filter by 'Main Course', 'Dessert', or 'Beverage'."
```

**Action:** Select different categories

---

#### 3.4 Toggle Availability (Optimistic UI)

**Screen:** Find a menu item and click toggle button

**Say:**
```
"One of the key features is the availability toggle with optimistic UI updates.

Watch when I click this toggle... the UI updates immediately, 
without waiting for the API response.

This provides instant feedback to the user. If the API call fails, 
the change is reverted and an error message is shown."
```

**Action:** Toggle availability on/off

---

#### 3.5 Add New Menu Item

**Screen:** Click "Add Menu Item" button

**Say:**
```
"Let me add a new menu item. I'll click 'Add Menu Item'...

This opens a modal form with validation. Let me fill in the details:
- Name: 'Veggie Burger'
- Category: 'Main Course'
- Price: 12.99
- Description: 'Delicious vegetable patty burger'

When I submit, the item is added and appears in the list."
```

**Action:** Fill form and submit

---

#### 3.6 Orders Dashboard

**Screen:** Navigate to Orders page

**Say:**
```
"Now let's look at the Orders Dashboard.

This page displays all customer orders with status badges. 
Each order shows the order number, customer name, table number, 
items ordered, and total amount.

I can filter orders by status - Pending, Preparing, Ready, 
Delivered, or Cancelled."
```

**Action:** Show orders, click on filters

---

#### 3.7 Update Order Status

**Screen:** Click on an order's status dropdown

**Say:**
```
"Restaurant staff can update the order status using this dropdown.

Let me change this order from 'Pending' to 'Preparing'...

The status badge updates immediately."
```

**Action:** Change order status

---

### SECTION 4: API Testing with Postman (2 minutes)

**Screen:** Open Postman

**Say:**
```
"Now let me show you the backend API testing using Postman.

I've created a collection with all the API endpoints."
```

---

#### 4.1 Health Check

**Screen:** Click on Server Status request

**Say:**
```
"First, the health check endpoint at GET /api/health.

This confirms our server is running. As you can see, 
we get a 200 OK response with status 'OK'."
```

**Action:** Send request, show response

---

#### 4.2 Get All Menu Items

**Screen:** Click on GET menu request

**Say:**
```
"GET /api/menu returns all menu items from the database.

The response includes the auto-generated _id from MongoDB, 
along with all the menu item details like name, category, 
price, ingredients, and timestamps."
```

**Action:** Send request, scroll through response

---

#### 4.3 Create Menu Item

**Screen:** Click on POST menu request

**Say:**
```
"To create a new menu item, I send a POST request to /api/menu 
with the item details in the request body.

Notice the _id is automatically generated by MongoDB - I don't 
need to create it manually. MongoDB uses ObjectId which is a 
12-byte unique identifier."
```

**Action:** Show request body, send request, show response with new _id

---

#### 4.4 Get Orders with Population

**Screen:** Click on GET orders request

**Say:**
```
"GET /api/orders returns all orders with populated menu item details.

Notice how each order's items array contains the full menu item 
information, not just the ID. This is done using Mongoose's 
populate method."
```

**Action:** Send request, show populated data

---

#### 4.5 Delete Menu Item

**Screen:** Click on DELETE request

**Say:**
```
"Finally, DELETE /api/menu/:id removes a menu item.

We get a success response confirming the deletion."
```

**Action:** Send request, show response

---

### SECTION 5: Code Walkthrough (2-3 minutes)

**Screen:** Open VS Code

---

#### 5.1 Project Structure

**Say:**
```
"Let me show you the code structure.

The project is organized into two main folders:
- 'client' for the React application
- 'server' for the Node.js API

This separation makes the code maintainable and easy to deploy."
```

**Action:** Show the folder structure in VS Code's file explorer. Point to the server folder (containing controllers, models, routes) and the client folder (containing src/components, src/pages, src/hooks).

---

#### 5.2 Backend - Schema

**Screen:** Open the MenuItem.js model file (e.g., in `server/models/MenuItem.js`)

**Say:**
```
"Here's the MenuItem schema, located in my models folder. I've defined fields like name, 
description, category with enum validation, price, and ingredients array.

The timestamps option automatically adds createdAt and updatedAt fields.

Notice I've also added a text index on name and ingredients 
for efficient search queries."
```

**Action:** Scroll through the schema code in MenuItem.js

---

#### 5.3 Backend - Controller

**Screen:** Open the menu controller file (e.g., `server/controllers/menuController.js`)

**Say:**
```
"In the menu controller, I have functions for each CRUD operation.

Here's the getAllMenuItems function - it supports filtering 
by category, availability, and price range using query parameters.

Error handling is done with try-catch blocks, returning 
appropriate status codes."
```

**Action:** Show the getAllMenuItems function in menuController.js

---

#### 5.4 Frontend - useDebounce Hook

**Screen:** Open your custom useDebounce.js hook file (e.g., in `client/src/hooks/useDebounce.js`)

**Say:**
```
"Here's my custom useDebounce hook, which lives in my hooks folder.

It takes a value and delay as parameters. Using useEffect, 
it sets a timeout to update the debounced value.

The cleanup function clears the timeout if the value changes 
before the delay completes. This is the key to preventing 
unnecessary API calls."
```

**Action:** Show the code for the useDebounce hook.

---

#### 5.5 Frontend - Optimistic Update

**Screen:** Open the component with the toggle functionality (e.g., `client/src/components/MenuItemCard.jsx` or `client/src/pages/MenuManagement.jsx`)

**Say:**
```
"For optimistic updates, I store the previous state before 
making changes inside my Menu Item Card component.

When the user clicks the toggle, I update the local state immediately, 
then make the API call. If the API call fails, I catch the error, 
revert to the previous state, and show an error toast."
```

**Action:** Show the handler function for the toggle action, highlighting the immediate state update and the catch block.

---

### SECTION 6: Challenges & Conclusion (1 minute)

**Screen:** Show README challenges section or summary slide

**Say:**
```
"During this project, I faced a few challenges:

1. CORS Issues - Solved by configuring proper CORS middleware 
   with allowed origins.

2. Debouncing - Understanding useEffect cleanup functions took 
   some research, but it's now working perfectly.

3. Deployment - Managing environment variables across different 
   environments required careful configuration.

In conclusion, this project demonstrates:
- RESTful API design with proper validation
- MongoDB with indexing and aggregation
- React best practices with custom hooks
- Performance optimization with debouncing and optimistic updates
- Full deployment pipeline

Thank you for watching. The project is live and all links are 
available in the GitHub README.

Feel free to reach out if you have any questions."
```

---

## Quick Reference - Key Points to Mention

| Feature | What to Say |
|---------|-------------|
| Debouncing | "300ms delay, prevents unnecessary API calls" |
| Optimistic UI | "Updates instantly, reverts on failure" |
| ObjectId | "Auto-generated by MongoDB, 12-byte unique identifier" |
| Population | "Mongoose populate joins related documents" |
| Text Index | "Enables efficient text search on name and ingredients" |
| Timestamps | "Automatically tracks createdAt and updatedAt" |
| MERN Stack | "MongoDB, Express, React, Node.js" |

---

## Recording Tips

1. Speak clearly and at a moderate pace
2. Pause briefly between sections
3. Move mouse slowly when demonstrating
4. Zoom in on code when showing details (Ctrl + Mouse Scroll in VS Code)
5. If you make a mistake, pause and continue - you can edit later
6. Keep energy positive and professional
7. Practice once before final recording

---

## Recommended Recording Tools

| Tool | Platform | Free? |
|------|----------|-------|
| OBS Studio | Windows/Mac/Linux | Yes |
| Loom | Web/Desktop | Yes (5 min limit) |
| Screencast-O-Matic | Web/Desktop | Yes |
| QuickTime | Mac | Yes |
| Xbox Game Bar | Windows 10/11 | Yes (Win + G) |

---

## Final Checklist Before Submitting

- [ ] Video is 8-10 minutes long
- [ ] Audio is clear and audible
- [ ] All features are demonstrated
- [ ] Code is visible and readable
- [ ] Live URLs are shown working
- [ ] No sensitive data visible (API keys, passwords)
- [ ] Video exported in good quality (1080p)
- [ ] File size is reasonable for upload
