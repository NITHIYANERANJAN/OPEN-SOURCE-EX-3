# OPEN-SOURCE-EX-3
## NAME : NITHIYANERANJAN S
## REG NO : 212223040136
## DEPT : CSE
## AIM:
To create a user group, add users with specific permissions, assign passwords, and verify their group membership and login restrictions in RHEL.

## PROCEDURE:

### **STEP 1:**  
Create a new group  
```bash
sudo groupadd admin
```

### **STEP 2:**  
Add user **harry** to admin group  
```bash
sudo useradd -m -G admin harry
```

### **STEP 3:**  
Add user **natasha** to admin group  
```bash
sudo useradd -m -G admin natasha
```

### **STEP 4:**  
Create user **sarah** with no-login shell  
```bash
sudo useradd -m -s /sbin/nologin sarah
```

### **STEP 5:**  
Set passwords for all users  
```bash
echo "harry:redhat" | sudo chpasswd
echo "natasha:redhat" | sudo chpasswd
echo "sarah:redhat" | sudo chpasswd
```

### **STEP 6:**  
Check group membership  
```bash
groups harry
groups natasha
groups sarah
```

### **STEP 7:**  
Verify sarah’s login shell  
```bash
grep sarah /etc/passwd
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/ac81ae6e-730d-4cb4-8c22-5ca6fcc2b514)

## RESULT:
The users were created, assigned groups, provided passwords, and verified successfully in the Red Hat Lab Terminal.
