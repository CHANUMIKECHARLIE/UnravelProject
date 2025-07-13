# System Optimizer Project

This project demonstrates a multi-module Java application to handle:
- Thread-safe session management
- Memory leak detection and caching strategy
- Concurrent log processing with prioritization
- Deadlock resolution in multithreaded environments
- Optimized HikariCP-based database connection pooling with custom monitoring


## 🛠️ Technologies Used
- Java 11+
- Spring Boot (for database connection management)
- HikariCP (Connection Pooling)
- Maven (for dependency management)


## Modules & Features

🔐 **SessionManager**
- Thread-safe session tracking
- Prevents memory leaks
- Includes session cleanup logic

🧠 **MemoryManager**
- Simulates large session data usage
- Uses LRU cache to prevent memory leaks
- Logs memory usage for analysis

⚙️ **LogProcessor**
- Priority-based producer-consumer model
- Uses thread pools and PriorityBlockingQueue
- Ensures critical tasks are processed first

💥 **DeadlockSimulator**
- Demonstrates common deadlock
- Fixed using ordered locking strategy
- Thread-safe and deadlock-free

🗄️ **DatabaseManager**
- Uses HikariCP with Spring Boot
- Logs slow connections and pool underutilization
- Includes monitoring with TimerTask


## 🧩 Dependencies
Add these to your pom.xml:

    <dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>com.zaxxer</groupId>
			<artifactId>HikariCP</artifactId>
		</dependency>
		<dependency>
	        <groupId>com.mysql</groupId>
	        <artifactId>mysql-connector-j</artifactId>
	        <version>8.0.31</version>
	    </dependency>


## 📝 Author
Chanu Bala Devi
(Java Backend Developer)
