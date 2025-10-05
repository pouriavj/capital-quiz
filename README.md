# Capital Quiz

An interactive Node.js and PostgreSQL quiz app that challenges users to name the capital city of any country in the world.  
The app dynamically fetches country names and capitals from a **PostgreSQL database** and renders questions using **EJS templates**.

---

## 🚀 Features

- Randomly selects countries for quiz questions from a PostgreSQL database  
- Tracks total correct answers per session  
- Uses **server-side rendering** with EJS  
- Simple and responsive design with CSS  

---
## 📸 Demo

![Capital Quiz Demo](./capitalQuiz.jpg)  


---

## 🗄️ Database Setup (Using pgAdmin)

Follow these steps to set up the PostgreSQL database for the **Capital Quiz** project using **pgAdmin**.

---

### 🧩 Step 1: Create a New Database
1. Open **pgAdmin** and connect to your PostgreSQL server.  
2. Right-click on **Databases** → click **Create** → **Database**.  
3. Enter a name, for example: `capitalquiz`.  
4. Set a **password** that you’ll also use in your project’s connection settings.  
5. Click **Save**.

---

### 🧱 Step 2: Create the `capitals` Table
1. Right-click on your new database → choose **Query Tool**.  
2. Paste and run this SQL command:
 ```sql
   CREATE TABLE capitals (
       id SERIAL PRIMARY KEY,
       country TEXT,
       capital TEXT
   );
 ```
3. Click Execute (▶️) to create the table.
---
### 📥 Step 3: Import the `capitals.csv` File

1. In **pgAdmin**, expand your database → right-click on the **capitals** table → choose **Import/Export Data**.  
2. Under **Filename**, browse and select the `capitals.csv` file from your project folder.  
3. Set **Format** to `CSV`.  
4. Check ✅ **Header** (to include the first line of the CSV as column names).  
5. Leave **Delimiter** as a comma `,`.  
6. Click **OK** to import the data.


> ⚠️ **Notes:**
> - The `capitals.csv` file already includes an `id` column.  
> - PostgreSQL will use the existing IDs from the CSV during import.  
> - Because the `id` column is defined as `SERIAL PRIMARY KEY`, PostgreSQL will **automatically continue numbering** for any **new rows** you insert later — picking up from the **highest existing ID** in the table.

---
## 🔑 Database Authentication

The app connects to PostgreSQL using a username and password.  
Open `index.js` and Replace the placeholders with your credentials:

```js

const db = new pg.Client({
  user: "your-username-here",      // <-- Enter your PostgreSQL username here
  host: "localhost",               // <-- Usually localhost unless using a remote DB
  database: "capitalquiz",         // <-- Your database name
  password: "your-password-here",  // <-- Enter your PostgreSQL password here
  port: 5432,                      // <-- Default PostgreSQL port
});


```
---

## ⚙️ How to Run

1. Clone the repository:
```bash
git clone https://github.com/pouriavj/capital-quiz.git
cd capital-quiz
```
2. Install dependencies:
```bash
npm install
```
3. **Start the server**
```bash
node index.js
```
The app will be available at 👉 http://localhost:3000<br/>
4. **(Optional) Change the port**<br/>
Open `index.js` and modify:
```javascript
const port = 3000; // change this to your preferred port
```
---
## 🛠️ Built With

### Core Tech
- [Node.js](https://nodejs.org/)  
- [Express.js](https://expressjs.com/)  
- [EJS](https://ejs.co/)  
- HTML5 / CSS3  

### Additional Libraries
- [body-parser](https://www.npmjs.com/package/body-parser) – to parse form submissions  
- [pg](https://www.npmjs.com/package/pg) – PostgreSQL client for Node.js  
- [JSON](https://www.json.org/json-en.html) – data format used for database queries  




