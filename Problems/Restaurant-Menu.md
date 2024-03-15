# Restaurant Menu Recommender - Vegetarian, Vegan, Gluten-Free
## Problem Description
You are tasked with creating a restaurant menu recommender system that suggests suitable menu items for customers with dietary restrictions such as vegetarian, vegan, and gluten-free. Given a set of menu items and the dietary preferences of the customer, the system should recommend menu items that align with their dietary restrictions.

## Input
The input will contain:
- A list of menu items with details such as name, description, ingredients, and dietary information (vegetarian, vegan, gluten-free).
- Customer's dietary preferences, indicating whether they are vegetarian, vegan, or have a gluten-free diet.

## Output
The output will contain:
- A list of recommended menu items that match the customer's dietary preferences.

## Constraints
- Each menu item may have multiple dietary tags (e.g., vegetarian, vegan, gluten-free).
- The customer's dietary preferences may include any combination of vegetarian, vegan, and gluten-free.
- The number of menu items and the length of dietary preferences will not exceed practical limits.

## Examples
|Input|Output|
|-|-|
|Menu: <br> - Grilled Vegetable Salad (Vegetarian, Gluten-Free)<br> - Vegan Pad Thai (Vegan)<br> - Quinoa Stuffed Bell Peppers (Vegetarian, Gluten-Free)<br> Customer Preferences: Vegetarian|Recommended Menu: <br> - Grilled Vegetable Salad<br> - Quinoa Stuffed Bell Peppers|
|Menu: <br> - Margherita Pizza (Vegetarian)<br> - Vegan Lasagna (Vegan)<br> - Gluten-Free Pasta Primavera (Gluten-Free)<br> Customer Preferences: Gluten-Free|Recommended Menu: <br> - Gluten-Free Pasta Primavera|