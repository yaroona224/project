# Project
# Working with KSA entertainment
## 🧠 Let`s learn how to load a csv file in MySQL
<img width="349" alt="Screenshot 2025-02-11 at 11 23 48 AM" src="https://github.com/user-attachments/assets/d8afcdab-a007-4416-b51c-27fe89ed390e" />

<img width="841" alt="Screenshot 2025-02-11 at 11 24 12 AM" src="https://github.com/user-attachments/assets/fcd6e0a7-7a48-4021-952f-cdde46b92880" />

## Let`s learn how we can play with this dataset using some questions:
### 1. Retrieve all theaters with a rating of 4 or higher
```sql
SELECT * FROM project.cleaned_file WHERE rating >= 4:
```
<img width="1016" alt="Screenshot 2025-02-11 at 11 40 59 AM" src="https://github.com/user-attachments/assets/023c3bf2-972c-45f3-a393-98f100088942" />

###  2. Count the number of venues by genre
```sql
SELECT genre, COUNT(*) AS venue_count FROM project.cleaned_file GROUP BY genre;
```
<img width="213" alt="Screenshot 2025-02-11 at 11 40 03 AM" src="https://github.com/user-attachments/assets/905d0ff3-389d-49e5-a87d-606cfc6a02a5" />

### 3. Find the highest-rated venue
```sql
SELECT * FROM project.cleaned_file ORDER BY rating DESC LIMIT 1;
```
<img width="665" alt="Screenshot 2025-02-11 at 11 42 30 AM" src="https://github.com/user-attachments/assets/c92253fc-5796-4fdf-bd6c-6b04c9b3ba82" />

### 4. List venues with more than 10,000 reviews
```sql
SELECT * FROM project.cleaned_file WHERE CAST(review_count AS SIGNED) > 10000;
```
<img width="983" alt="Screenshot 2025-02-11 at 11 43 36 AM" src="https://github.com/user-attachments/assets/887f5628-ea63-4ec5-8636-3622bd9e07e6" />

### 5. Retrieve venues located in Saudi Arabia
```sql
SELECT * FROM project.cleaned_file WHERE location LIKE '%Saudi Arabia%';
```
<img width="989" alt="Screenshot 2025-02-11 at 11 44 55 AM" src="https://github.com/user-attachments/assets/6ef82049-87ec-4b68-9dff-7d506bdd352c" />

### 6. Find the average rating for each genre
```sql
SELECT genre, AVG(rating) AS average_rating FROM project.cleaned_file GROUP BY genre;
```
<img width="249" alt="Screenshot 2025-02-11 at 11 53 51 AM" src="https://github.com/user-attachments/assets/d06aaaf2-a45e-4857-863c-775000ff5bc5" />

### 7. Get the top 5 most reviewed venues
```sql
SELECT * FROM project.cleaned_file ORDER BY CAST(review_count AS SIGNED) DESC LIMIT 5;
```
<img width="818" alt="Screenshot 2025-02-11 at 11 54 53 AM" src="https://github.com/user-attachments/assets/ab24d78e-c218-4d03-8e13-87e37b3c6408" />

### 8. Find venues that have a "cinema" in their name
```sql
SELECT * FROM project.cleaned_file WHERE name LIKE '%Cinema%';
```
<img width="936" alt="Screenshot 2025-02-11 at 11 55 44 AM" src="https://github.com/user-attachments/assets/38fda1c3-5a9c-4b2a-acc0-e2c6e738a6cc" />

### 9. Retrieve venues that have a comment mentioning "comfortable"
```sql
SELECT * FROM project.cleaned_file WHERE best_comment LIKE '%comfortable%';
```
<img width="895" alt="Screenshot 2025-02-11 at 11 57 10 AM" src="https://github.com/user-attachments/assets/f3ac8b85-2aaf-4209-b9cf-bd69a8cdb3a5" />

### 10. Count how many venues have a rating of 0
```sql
SELECT COUNT(*) AS zero_rated_venues FROM project.cleaned_file WHERE rating = 0;
```
<img width="146" alt="Screenshot 2025-02-11 at 11 58 01 AM" src="https://github.com/user-attachments/assets/2c9ed016-e169-496c-a93b-367776b84845" />









