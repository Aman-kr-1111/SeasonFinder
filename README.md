# 🌱 IOCProj02-DependencyInjection

---

## 📌 Project Description

Welcome to **IOCProj02-DependencyInjection**! 🚀 This project is a hands-on implementation of **Spring's Inversion of Control (IoC) Container** using **Dependency Injection (DI)**. It demonstrates how Spring can manage object dependencies efficiently, reducing boilerplate code and improving modularity. 

In this example, we create a **SeasonFinder** service that determines the season based on the current date. The project follows Spring's **Annotation-based Configuration** approach along with XML-based bean definitions.

---

## 🚀 Tech Stack & Tools

- ![Java](https://img.shields.io/badge/Java-17-007396?logo=java&logoColor=white) **Java 17**
- ![Spring](https://img.shields.io/badge/Spring_Framework-6.2.2-6DB33F?logo=spring&logoColor=white) **Spring Core (IOC, DI)**
- ![Maven](https://img.shields.io/badge/Maven-3.8.6-C71A36?logo=apache-maven&logoColor=white) **Maven**
- ![JUnit](https://img.shields.io/badge/JUnit-5.11-25A162?logo=junit5&logoColor=white) **JUnit 5** (for testing)
- ![Git](https://img.shields.io/badge/Git-Version_Control-F05032?logo=git&logoColor=white) **Git & GitHub**
- ![Eclipse](https://img.shields.io/badge/Eclipse-IDE-2C2255?logo=eclipse-ide&logoColor=white) **Eclipse IDE**

---

## 📦 Dependencies

The project uses the following dependencies:

```xml
<dependencies>
    <dependency>
        <groupId>org.springframework</groupId>
        <artifactId>spring-context-support</artifactId>
        <version>6.2.2</version>
    </dependency>
    <dependency>
        <groupId>org.junit.jupiter</groupId>
        <artifactId>junit-jupiter-api</artifactId>
        <scope>test</scope>
    </dependency>
</dependencies>
```

---

## 📁 Project Structure

```
IOCProj02-DependencyInjection
│── src/main/java/com/nt/sbeans/
│   ├── SeasonFinder.java
│── src/main/java/com/nt/client/
│   ├── DependencyInjectionTest.java
│── src/main/java/com/nt/cfgs/
│   ├── applicationContext.xml
│── pom.xml
│── README.md
```

---

## ⚙️ Setup & Run

### 1️⃣ Clone the Repository
```sh
git clone https://github.com/your-repo-link.git
cd IOCProj02-DependencyInjection
```

### 2️⃣ Build the Project
```sh
mvn clean install
```

### 3️⃣ Run the Application
```sh
mvn exec:java -Dexec.mainClass="com.nt.client.DependencyInjectionTest"
```

## 🎯 How It Works

This project demonstrates how **Spring’s IoC container** and **Dependency Injection** work together to manage object dependencies efficiently.

1️⃣ **Spring Container Initialization:**
   - The **applicationContext.xml** file defines the bean configuration.
   - The `LocalDate` bean is registered using XML configuration with a factory method `now()`.
   - The `SeasonFinder` class is marked as a **Spring component** using `@Component("sf")`, enabling Spring to manage it as a bean.

2️⃣ **Dependency Injection in Action:**
   - The `SeasonFinder` class has a dependency on `LocalDate`.
   - Spring injects the `LocalDate` bean automatically using `@Autowired`.
   - When the `findOutSeasonName(String user)` method is called, it fetches the **current month** using `date.getMonthValue()` and determines the **season** accordingly.

3️⃣ **Executing the Test Class:**
   - The `DependencyInjectionTest` class initializes the Spring container using `FileSystemXmlApplicationContext`.
   - The `SeasonFinder` bean is retrieved using `ctx.getBean("sf")`.
   - The `findOutSeasonName()` method is invoked to display the seasonal message.

---

## 📌 Expected Output

```
SeasonFinder::0-param constructor
SeasonFinder.findOutSeasonName()
Hot Summer wishes to: raja
```

---

## 📌 Key Takeaways

✅ Understanding **Spring Dependency Injection** (DI) 🔄  
✅ Configuring **Spring Beans** using XML and `@Component` 🏗️  
✅ Managing **predefined classes as Spring Beans** ⚙️  
✅ Implementing **IoC Container** for better dependency management 🎛️  
✅ Hands-on experience with **Maven and JUnit Testing** 🛠️  

---

## 🏆 Why This Project is Important?

✨ This project is perfect for beginners trying to understand **Spring Framework’s IoC & DI concepts**. By implementing DI, developers can write clean, maintainable, and loosely coupled code. The **SeasonFinder** use case is a fun yet practical example to get started!

---

## ✨ Created By

👨‍💻 **Aman Kumar**  
🚀 Passionate Java Full Stack Developer 💡  
📧 Reach me at: [LinkedIn](https://www.linkedin.com/in/your-profile) | [GitHub](https://github.com/your-profile)  

---

🔗 **Happy Coding! 🚀**

