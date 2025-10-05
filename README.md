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

## 🛠️ Built With

### Core Tech
- [Node.js](https://nodejs.org/)  
- [Express.js](https://expressjs.com/)  
- [EJS](https://ejs.co/)  
- HTML5 / CSS3  

### Additional Libraries
- [Body-parser](https://www.npmjs.com/package/body-parser) – to parse form submissions  
- [pg](https://www.npmjs.com/package/pg) – PostgreSQL client for Node.js  
- [JSON](https://www.json.org/json-en.html) – data format used for database queries  

---

## 📸 Demo

![Capital Quiz Demo](./capitalQuiz.jpg)  


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
3. Set up your PostgreSQL database.
