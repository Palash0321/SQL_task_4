# SQL_task_4
### ORDERS TABLE:

**SELECT 
    *
FROM
    ecommerce.orders;**
    
![Screenshot 2025-06-27 135805](https://github.com/user-attachments/assets/ebf72669-ff12-46c0-a008-259cb9231425)

**SELECT 
    CustomerName
FROM
    ecommerce.orders;**

![Screenshot 2025-06-28 173828](https://github.com/user-attachments/assets/b2761a26-ba69-4905-a765-b269aeb9059a)

**SELECT 
    State
FROM
    ecommerce.orders;**

![Screenshot 2025-06-28 173921](https://github.com/user-attachments/assets/62d35e19-1b67-4dd5-b7da-c22db9e035df)

**SELECT 
    city
FROM
    ecommerce.orders;**

![Screenshot 2025-06-28 174021](https://github.com/user-attachments/assets/23c39ed6-6454-469d-9c12-c569e30b5eb0)


### SELECT, WHERE, ORDER BY, GROUP BY
### **AGGREGATION FUNCTIONS (COUNT)**

**SELECT 
    CustomerName, State, city
FROM
    ecommerce.orders
    WHERE
    city = 'Bhopal';**

![Screenshot 2025-06-28 171054](https://github.com/user-attachments/assets/e3f1998e-267d-423a-b691-2230ecbae4a9)

**SELECT 
    *
FROM
    ecommerce.orders
WHERE
    State = 'Uttar Pradesh'
    ORDER BY CustomerName ASC;**

![Screenshot 2025-06-28 172841](https://github.com/user-attachments/assets/ca477800-8932-4dc0-9653-98098cc84eb6)

**SELECT 
    `Order ID`, CustomerName
FROM
    ecommerce.orders
WHERE
    `Order Date` = '10-03-2018';**

![Screenshot 2025-06-28 171107](https://github.com/user-attachments/assets/4170ff07-179a-41a1-9148-2f777c2f695a)

**SELECT 
    COUNT(`Order ID`) AS Total_Orders
FROM
    ecommerce.orders;**

![Screenshot 2025-06-28 174158](https://github.com/user-attachments/assets/7e9d6461-402c-4691-9164-d15a95fc7d19)

**SELECT 
    COUNT(DISTINCT CustomerName) AS UniqueCustomers
FROM
    ecommerce.orders;**

![image](https://github.com/user-attachments/assets/50713d51-e1be-4db8-849f-23644caca5dc)



**SELECT 
    State, COUNT(`Order ID`) AS OrderpereachState
FROM
    ecommerce.orders
GROUP BY State;**

![Screenshot 2025-06-28 171127](https://github.com/user-attachments/assets/48b073d8-572b-4314-b0aa-0369ebd00315)

**SELECT 
    city, COUNT(`Order ID`) AS OrderPerCity
FROM
    ecommerce.orders
GROUP BY city
HAVING COUNT(`Order ID`) > 20;**

![Screenshot 2025-06-28 171411](https://github.com/user-attachments/assets/6e0e32f1-7327-45dc-b1e8-27ccdf693efc)

**SELECT 
    State, COUNT(DISTINCT city) AS UniqueCity
FROM
    ecommerce.orders
    GROUP BY State;**

![image](https://github.com/user-attachments/assets/e7695937-2aa5-48bc-aa35-2a5610ff6bf0)



### VIEW

**CREATE VIEW CityOrderCount AS
    SELECT 
        city, COUNT(`Order ID`) AS Numoforders
    FROM
        ecommerce.orders
    GROUP BY city;
SELECT 
    *
FROM
    CityOrderCount;**

![Screenshot 2025-06-28 171426](https://github.com/user-attachments/assets/1166586a-be0f-4484-9562-bf1cd96bae7b)

**CREATE VIEW UniqueCustomerLocations AS
    SELECT DISTINCT
        CustomerName, State
    FROM
        ecommerce.orders;
SELECT 
    *
FROM
    UniqueCustomerLocations;**

![Screenshot 2025-06-28 171443](https://github.com/user-attachments/assets/44d96860-2cd7-478c-96b4-75f478686056)

### DETAILS TABLE:
**SELECT 
    *
FROM
    ecommerce.details;**

![Screenshot 2025-06-27 135747](https://github.com/user-attachments/assets/a0503295-8a87-4f47-a288-c1a152fad5fe)

**SELECT 
    `Order ID`
FROM
    ecommerce.details;**

![image](https://github.com/user-attachments/assets/1bd9f470-4bc8-435a-abba-055507a51681)

**SELECT 
    `Sub-category`
FROM
    ecommerce.details;**

![image](https://github.com/user-attachments/assets/12f3be3b-0a63-49b7-a825-81129640a6c0)

**SELECT 
    Amount
FROM
    ecommerce.details;**

![image](https://github.com/user-attachments/assets/abaaa058-1b7e-4eae-8742-8612613ca93e)

**SELECT 
    Profit
FROM
    ecommerce.details;**

![image](https://github.com/user-attachments/assets/058f4bd2-0b4b-45fd-b37e-f283219e6390)

**SELECT 
    Quantity
FROM
    ecommerce.details;**

![image](https://github.com/user-attachments/assets/3d13ff86-4a38-40aa-b692-70acdb9eb491)

**SELECT 
    Category
FROM
    ecommerce.details;**

![image](https://github.com/user-attachments/assets/56b65a82-cdce-4a1c-8e17-84dc54529e48)

**SELECT 
    PaymentMode
FROM
    ecommerce.details;**

![image](https://github.com/user-attachments/assets/64f93e40-c509-417b-b11d-094158d80494)

**SELECT DISTINCT
    PaymentMode
FROM
    ecommerce.details;**

![image](https://github.com/user-attachments/assets/a0f9e856-52b0-478c-ab63-4cbcbc22745c)

**SELECT DISTINCT
    Category
FROM
    ecommerce.details;**

![image](https://github.com/user-attachments/assets/ba481804-bdbf-4d8a-aad1-b7db443c9a97)

### SELECT, WHERE, ORDER BY, GROUP BY
### **AGGREGATE FUNCTIONS (SUM, COUNT, AVERAGE, MAX)**

**SELECT 
    Category, SUM(Amount) AS Total_Amount
FROM
    ecommerce.details
GROUP BY Category;**

![image](https://github.com/user-attachments/assets/9f21df60-27cf-4df3-a0db-ba47f57f1c54)

**SELECT 
    *
FROM
    ecommerce.details
WHERE
    Amount >= 1000
ORDER BY Amount DESC;**

![image](https://github.com/user-attachments/assets/756c8bdc-6f72-474c-8ee0-072492c6b229)

**SELECT 
    *
FROM
    ecommerce.details
WHERE
    `Order ID` = 'B-25681';**

![image](https://github.com/user-attachments/assets/190e891d-b239-428b-97a1-e566077fc721)

**I used AND OPERATOR IN THIS QUERY**
**SELECT 
    *
FROM
    ecommerce.details
WHERE
    Category = 'Electronics'
        AND Profit > 500;**

![image](https://github.com/user-attachments/assets/c511b3d5-7b84-4e17-92c6-1aae61dba8e4)
























    
