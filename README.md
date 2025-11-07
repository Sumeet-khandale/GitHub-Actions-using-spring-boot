# GitHub-Actions-using-spring-boot

---

```markdown
#  Hotel Service - Spring Boot + GitHub Actions

This is a simple Spring Boot microservice called Hotel Service.  
It is built using Java 17, Maven, and GitHub Actions for CI (Continuous Integration).  


---

## ⚙️ Tech Stack
- Java 17
- Spring Boot
- Maven
- GitHub Actions

---

## 📁 Project Structure
```

HotelService/
├── pom.xml
├── src/
└── .github/
└── workflows/
└── first-actions.yml

````

---

##  Run Locally
````
1. **Clone the repository**
   ```bash
   git clone https://github.com/Sumeet-khandale/GitHub-Actions-using-spring-boot.git
   cd GitHub-Actions-using-spring-boot/HotelService
```
````

2. **Build the project**

   ```bash
   mvn clean package -DskipTests
   ```

3. **Run the project**

   ```bash
   mvn spring-boot:run
   ```

4. **Open in browser**

   ```
   http://localhost:8081
   ```

---

## 🤖 GitHub Actions Workflow

File: `.github/workflows/first-actions.yml`

```yaml
name: Build Spring Boot Project

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Set up JDK 17
        uses: actions/setup-java@v4
        with:
          java-version: '17'
          distribution: 'temurin'

      - name: Build with Maven
        working-directory: ./HotelService
        run: mvn clean package -DskipTests
```

---

## 🧠 How It Works

* Every time you **push code** or **create a pull request** to the `main` branch,
  GitHub Actions automatically runs:

  1. Checkout your code
  2. Set up Java 17
  3. Build using Maven

You can see the progress in the **“Actions” tab** of your GitHub repo.

---

## 👨‍💻 Author

**Sumeet Khandale**
🔗 [GitHub Profile](https://github.com/Sumeet-khandale)

---

✅ **That’s it!**
Your project will automatically build on every code push using GitHub Actions 🎉

```

---

```
