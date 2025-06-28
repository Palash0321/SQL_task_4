# SQL_task_4
**SELECT 
    *
FROM
    ecommerce.orders;**
    
![Screenshot 2025-06-27 135805](https://github.com/user-attachments/assets/ebf72669-ff12-46c0-a008-259cb9231425)


### SELECT, WHERE, ORDER BY, GROUP BY

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
    State, COUNT(`Order ID`) AS OrderpereachState
FROM
    ecommerce.orders
GROUP BY State;**

![Screenshot 2025-06-28 171127](https://github.com/user-attachments/assets/48b073d8-572b-4314-b0aa-0369ebd00315)

** 






    
