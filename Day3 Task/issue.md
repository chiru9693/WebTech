<img width="425" height="330" alt="image" src="https://github.com/user-attachments/assets/6f6cebde-ded6-4039-aaf6-e21dad71020b" />
Application Not Running Error
Problem: Spring Boot application not started.
Error Example
Connection refused: localhost:8080

Reason
Spring Boot server not running.

Solution
Run PmsApplication.java
Check console logs.

## 2 .Wrong URL Error

Problem: Incorrect API URL in Postman.
Correct URL from your project:
```
http://localhost:8080/Product/addProduct
```
Error Example   : 404 Not Found

Reason
Wrong endpoint
Wrong mapping

Check   :  @RequestMapping("/Product")     ,   @PostMapping("/addProduct")

3️⃣ JSON Format Error

Problem: Wrong JSON format in Postman Body.

Correct format (from your document): 

day 3

[
 {
   "Category":"hello",
   "Description":"123",
   "inStock":true,
   "name":"Laptop",
   "price":55000,
   "stockQuantity":10
 }
]

Error Example

400 Bad Request

Reason

Missing brackets

Wrong key names

4️⃣ Field Name Mismatch Error

Problem: JSON field names not matching Product.java fields

Example mismatch:

JSON → Category
Java → category

Error

HttpMessageNotReadableException

Solution
Make sure names match.

5️⃣ Database Connection Error

Error Example

Cannot connect to database

Reason

MySQL not running

Wrong username/password

Check

spring.datasource.url
spring.datasource.username
spring.datasource.password
6️⃣ Table Not Found Error

Error Example

Table 'Product' doesn't exist

Reason

Table not created

Wrong database selected

From your document you must run: 

day 3

use ProductManagementSystem;
select * from Product;
7️⃣ Repository Bean Error

Error Example

No qualifying bean of type ProductRepository

Reason

Repository not extending JpaRepository

Example correct:

public interface ProductRepository 
       extends JpaRepository<Product, Integer>
8️⃣ Dependency Injection Error

If @Autowired not working.

Example

NullPointerException

Reason

ProductService service = null

Check annotations:

@RestController
@Service
@Repository
@Autowired
9️⃣ HTTP Method Error

If using wrong method.

Example

405 Method Not Allowed

Reason

You used GET instead of POST

Correct:

POST /Product/addProduct
🔟 Data Not Inserting in Database

Possible reasons

Entity mapping wrong

Database not connected

Transaction error
