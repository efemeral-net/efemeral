---
{"publish":true,"title":"Survivor Data Visualization App (2020)","PassFrontmatter":true}
---

During the lockdown in 2020, like many others, I had extra time on my hands. I was spending a lot of my time taking computer science courses and learning Python. After a while, I felt I was ready to try to build a web app to practice processing and visualizing data. I had the idea to pull the data from the other way I was spending a lot of time: binging Survivor. 

![Screenshot 2025-03-02 at 4.59.40 PM.png](../media/Screenshot%202025-03-02%20at%204.59.40%20PM.png)

---
## **The Idea: Merging "Survivor" with Data Science**

I've always been fascinated by the strategies, alliances, and voting patterns in "Survivor." The idea of **quantifying** these elements and presenting them visually intrigued me. So, I started collecting data—manually compiling a **database of winners, ages, votes, and regions** spanning 40 seasons.

The goal was simple:

1. **Create a database** of contestant statistics
2. **Write SQL queries** to extract insights
3. **Use Flask & Jinja** to display the data dynamically
4. **Visualize key trends** using **Matplotlib**

---

## **Tech Stack & Implementation**

### **Flask & Jinja: The Web Framework**

Flask’s lightweight nature made it seem more approachable as I was learning, but I was glad I did. This project had a lot to render and building with Flask and rendering them dynamically with Jinja templates helped the code stay clean and run fast. It allowed me to create clean, template-driven pages without unnecessary complexity.

### **SQLite & SQL Queries: The Data Engine**

Continuing on the goal of simplicity, I used an **SQLite database** to store all the contestant data, including:

- **Winner stats** (name, age, season)
- **Votes received**
- **Regional representation**

With SQL queries, I could efficiently retrieve and filter data for visualization.

### **Matplotlib: Bringing the Data to Life**

I opted for Matplotlib to generate static charts. Using Python scripts, I created **pie charts** to illustrate key trends.

![Screenshot 2025-03-02 at 5.00.06 PM.png](../media/Screenshot%202025-03-02%20at%205.00.06%20PM.png)

---
### **Front-End Design: A Clean, Dynamic Look**

The front-end keeps things simple yet bold, with a **high-contrast gradient background** and a **clean, structured layout**. A fixed side nav ensures easy access, while **monospace fonts, subtle transparency, and hover effects** give the data a sharp, modern feel. Tables and pie charts are styled for clarity, and **media queries** keep everything responsive.

---

## **Challenges & Lessons Learned**

**Data Collection Was a Grind**  
The hardest part was manually compiling and verifying the data. Pulling from the [**Survivor Wiki**](https://survivor.fandom.com/wiki/Main_Page) and cross-checking stats was time-consuming, but having a dataset I felt was unique and fun helped keep me pushing forward.

**Matplotlib's Image Cropping & Transparency**  
Generating **cropped, transparent images** was an unexpected challenge. I had to tweak the `bbox` parameters and use **PIL** for post-processing to get the charts looking just right.

```python
img = Image.open(imgPath)
croppedImage = img.crop(box)
croppedImage.save('static/' + file_name + '_cropped.png')
```

**SQL Query Optimization**  
As the database grew, some queries became inefficient. Learning how to **index** and optimize SQL queries made a noticeable difference in page load times.

---

The final product lives at **[survivor40.netlify.app](https://survivor40.netlify.app/)**, and the code is on my **[GitHub](https://github.com/k-hurl-e/survivor)**.