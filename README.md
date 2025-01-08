### **Bank Management System Using Java and Swing**

---

#### **Project Overview**  
This project introduces a **Bank Management System** tailored for **UMURENGE SACCO**, integrating a secure **ATM Machine System** for seamless banking services. The system automates essential operations such as deposits, withdrawals, and balance inquiries using **Java Swing** for the user interface and MySQL for database management.  

---

#### **Key Features**  
1. **ATM System**:  
   - Secure PIN-based authentication.  
   - Transactions like withdrawals, deposits, and mini-statements.  
   - Intuitive and user-friendly interface.  

2. **Admin Dashboard**:  
   - Manage customer accounts and transactions.  
   - Generate detailed financial reports.  

3. **Security Enhancements**:  
   - Encrypted PIN storage.  
   - SQL injection prevention with prepared statements.  

---

#### **Technologies Used**  
- **Language**: Java (Swing for GUI).  
- **Database**: MySQL (JDBC for connectivity).  
- **Security**: Encrypted PIN storage and session management.  

---

#### **Setup Instructions**  
1. Install **JDK 8+** and **MySQL Server**.  
2. Import the provided database schema into MySQL.  
3. Run the project in your preferred Java IDE.  

---

#### **Sample Code**  

**Login Authentication Example**:  
```java
Connection conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/BankDB", "root", "password");
String query = "SELECT formno FROM Login WHERE card_no = ? AND pin = ?";
PreparedStatement pstmt = conn.prepareStatement(query);
pstmt.setString(1, cardNo);
pstmt.setString(2, pin);
ResultSet rs = pstmt.executeQuery();
if (rs.next()) {
    System.out.println("Login successful!");
}
```

---

#### **Benefits**  
- **For Clients**: Convenient and secure access to banking services anytime.  
- **For Bank**: Enhanced efficiency and reduced operational risks.  

--- 

This project demonstrates how **Java Swing** and **database integration** can streamline banking services for a cooperative institution.
