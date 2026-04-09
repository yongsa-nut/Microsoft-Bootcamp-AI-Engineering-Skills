# Code Interpreter Q&A — Groundtruth for Testing

---

## Dataset 1: thai_street_food.csv

### Q1: What is the cheapest dish and how much does it cost?
**Answer:** หมูปิ้ง (Moo Ping) at 10 THB.

### Q2: What is the average price of dishes in the "noodles" category?
**Answer:** There are 6 noodle dishes (50, 60, 45, 35, 15, 45). Average = 250 / 6 = **41.67 THB**.

### Q3: Which dish has the highest monthly sales?
**Answer:** หมูปิ้ง (Moo Ping) with 25,000 monthly sales.

### Q4: What is the average rating of dishes with spicy_level 0 (not spicy)?
**Answer:** Dishes with spicy_level 0: ข้าวมันไก่ (4.6), มะม่วงข้าวเหนียว (4.8), หมูปิ้ง (4.6), ไข่เจียว (4.1), กล้วยทอด (4.0), ผัดซีอิ๊ว (4.3), โรตี (4.4). Average = 30.8 / 7 = **4.40**.

### Q5: How many dishes come from each region? Which region has the most?
**Answer:** Central: 14, Isan: 3, North: 1, South: 2. **Central** has the most.

---

## Dataset 2: student_spotify.sql

### Q1: Which artist has the most songs in the database?
**Answer:** BTS, Taylor Swift, Blackpink, Ed Sheeran, Three Man Down, NewJeans, LISA, and Bodyslam each have 2 songs. It's a tie (8 artists with 2 songs each; Billkin, Tontrakul, Numcha, Milli have 1 each).

### Q2: What is the total number of streams (in millions) for all Thai artists?
**Answer:** Thai artists: LISA (820.5 + 950.0), Billkin (180.2), Three Man Down (250.0 + 200.1), Tontrakul (120.7), Numcha (95.3), Milli (85.0), Bodyslam (150.8 + 130.0) = **2,982.6 million**.

### Q3: What is the average song duration (in seconds) for each mood?
**Answer:**
- happy: (199 + 164 + 212) / 3 = **191.67 sec**  ← BTS Dynamite, BTS Butter, NewJeans OMG
- sad: (245 + 230 + 270 + 258 + 220 + 285) / 6 = **251.33 sec**
- chill: (200 + 210 + 195 + 185) / 4 = **197.50 sec**
- hype: (207 + 181 + 180 + 178 + 169 + 186) / 6 = **183.50 sec**

### Q4: Which country has the highest average streams per song?
**Answer:**
- Thailand: 2,982.6 / 8 = 372.83M
- South Korea: (1800 + 1200 + 1400 + 900.4 + 750.2 + 600.5) / 6 = 1,108.52M
- USA: (1500.3 + 1100.6) / 2 = 1,300.45M
- UK: (4000.1 + 2800.0) / 2 = 3,400.05M

**UK** (Ed Sheeran) has the highest average at **3,400.05 million**.

### Q5: List all songs with over 1 billion streams (streams_millions > 1000), sorted by streams descending.
**Answer:**
1. Shape of You — 4,000.1M
2. Photograph — 2,800.0M
3. Dynamite — 1,800.0M
4. Anti-Hero — 1,500.3M
5. Butter — 1,400.0M
6. How You Like That — 1,200.0M
7. Cruel Summer — 1,100.6M

---

## Dataset 3: contoso_sales.csv

### Q1: What is the total revenue across all orders?
**Answer:** Calculate each row's revenue (unit_price × quantity), then sum:
- 199.98 + 129.99 + 349.99 + 699.95 + 1199.97 + 359.96 + 179.98 + 149.99 + 399.98 + 199.99 + 569.97 + 349.99 + 139.98 + 499.99 + 499.90 + 299.98 + 279.99 + 359.94 + 299.97 + 299.98 + 479.92 + 459.98 + 299.97 + 519.96 + 179.99 + 179.98 + 399.95 + 359.98 + 239.97 + 249.99
= **$10,543.30**

### Q2: Which category generated the most total revenue?
**Answer:**
- Home Appliances: 199.98 + 349.99 + 149.99 + 199.99 + 569.97 + 279.99 + 299.98 + 299.97 + 519.96 + 179.98 = **3,049.80**
- Electronics: 129.99 + 699.95 + 399.98 + 349.99 + 299.97 + 479.92 + 179.99 + 249.99 = **2,789.78**
- Office & Productivity: 1199.97 + 499.90 + 359.94 + 459.98 + 359.98 = **2,879.77**
- Fitness & Wearables: 359.96 + 499.99 + 299.98 + 399.95 = **1,559.88**
- Personal Care: 179.98 + 139.98 + 239.97 = **559.93**

**Home Appliances** is highest at ~$3,049.80.

### Q3: How many orders were placed by Corporate vs Retail customers?
**Answer:** Corporate: 10 orders (1003, 1004, 1005, 1010, 1011, 1015, 1018, 1022, 1025, 1028). Retail: 20 orders. **Retail has more orders (20 vs 10).**

### Q4: Which region placed the most orders?
**Answer:** US: 14, UK: 5, Germany: 4, Canada: 5. *(Wait, let me recount)*
- US: 1001, 1003, 1005, 1008, 1011, 1013, 1016, 1018, 1020, 1022, 1024, 1026, 1029 = 13
- UK: 1002, 1007, 1012, 1017, 1025, 1030 = 6
- Germany: 1004, 1009, 1015, 1021, 1027 = 5
- Canada: 1006, 1010, 1014, 1019, 1023, 1028 = 6

**US** with **13 orders**.

### Q5: What is the single most expensive order by total value (unit_price × quantity)?
**Answer:** Order 1005 — PostureFlex Pro Ergonomic Chair, $399.99 × 3 = **$1,199.97**.
