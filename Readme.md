# Medi Core: Hospital Management System
**Course:** Object-Oriented Programming (OOP) Assignment  
**Section:** BCS-2G

---

## 🚀 How to Compile and Run
1. Open your terminal or command prompt in the project folder.
2. Compile all source files using the g++ compiler:  
   `g++ *.cpp -o Medi Core`
3. Run the application:  
   `./Medi Core` (on Linux/Mac) or `Medi Core.exe` (on Windows).

---

## 🔗 GitHub Repository
https://github.com/l250678

---

## 🛠 Technical Highlights & Project Constraints
* **Manual Memory Management (No std::vector):** In strict compliance with project rule VI, `std::vector` is not used. Instead, a custom **Storage<T>** template class manages dynamic arrays, ensuring full control over memory.
* **Zero Memory Leakage:** Every object created (Patients, Appointments, etc.) is tracked and cleaned up through custom destructors to ensure no memory leaks (Rule VII).
* **Strict Modularity:** Following requirement IV, every class is isolated into its own **.h** and **.cpp** file. The `main()` function is kept clean as a sequence of function calls.
* **Manual Time Calculation:** To avoid "unsafe" `localtime` errors, the **Helper** class uses manual math to generate timestamps (DD-MM-YYYY) from Unix time.
* **Data Persistence:** All system information is handled via the **FileHandler** class, which syncs data with **.txt** files in real-time.

---

## 📋 System Functionality & Logic

### 1. Realistic Patient Portal
* **Dynamic Registration:** The system scans the database at runtime to auto-assign the next unique Patient ID.
* **Appointment Flow:** Patients can search for doctors by specialization. The system manages states like Scheduled, Completed, or No-Show.
* **Financial Management:** Includes a virtual wallet. Patients can top up balances, and the billing module calculates costs for services and medicine.

### 2. Doctor Portal
* **Daily Schedule:** Filters global data to show doctors only their specific appointments for the current date.
* **Clinical Records:** Doctors can write prescriptions and observations that are permanently linked to the Patient's medical history.

### 3. Admin Portal
* **Staff Oversight:** Admins can add/remove doctors and view a comprehensive log of all registered users in the hospital.

---

## File Structure
* **main.cpp**: Orchestrates the program flow.
* **Storage.h**: Custom template container (the alternative to `std::vector`).
* **FileHandler.cpp/h**: Manages the text-file "database."
* **Helper.cpp/h**: Mathematical logic for time and string utilities.
* **Validator.cpp/h**: Ensures all user inputs are valid before processing.

---
