1)Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
 ANS :In the Diagram, the "Product" and "Product_Category" entities have a one-to-many relationship.
- In the "Product" table (`dbo.Product`), there is a foreign key column named `category_id`, which references the primary key column `id` in the "Product_Category" table (`dbo.product_category`). This foreign key column represents the category of each product.
- This foreign key constraint ensures that each product in the "Product" table must have a valid reference to a category in the "Product_Category" table.
- Since the foreign key column `category_id` in the "Product" table can hold only one value at a time, it implies a one-to-many relationship from the "Product_Category" table to the "Product" table. This means that one category can have multiple products associated with it, but each product belongs to only one category.

2)How could you ensure that each product in the "Product" table has a valid category assigned to it?
ANS:To ensure that each product in the "Product" table has a valid category assigned to it, you can enforce referential integrity through the use of foreign key constraints. 
In the provided database script, there's already a foreign key constraint (FK_Product_product_category) defined between the "Product" and "Product_Category" tables. 
This constraint ensures that each value in the category_id column of the "Product" table must correspond to a valid id in the "Product_Category" table."
