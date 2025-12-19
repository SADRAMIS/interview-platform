# 🎤 Interview-Platform

> AI-Powered Technical Interview Platform | Real-Time Coding Sessions | Automated Problem Generation

[![Java](https://img.shields.io/badge/Java-17-ED8B00?style=flat&logo=openjdk)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F?style=flat&logo=spring-boot)](https://spring.io/projects/spring-boot)
[![WebSocket](https://img.shields.io/badge/WebSocket-Real--Time-blue?style=flat)](https://en.wikipedia.org/wiki/WebSocket)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 🎯 Overview

Interview-Platform is an AI-powered platform for conducting technical interviews with real-time code execution, automated problem grading, and performance analytics. Designed for companies and educators to assess candidate skills efficiently.

### Key Features
- ✅ **Virtual Interview Sessions** with real-time collaboration
- ✅ **Problem Repository** with auto-generated coding challenges
- ✅ **Live Code Execution** with multiple language support
- ✅ **Automated Grading** with test case validation
- ✅ **Real-Time Collaboration** via WebSocket
- ✅ **Performance Analytics** & detailed feedback
- ✅ **Role-Based Access** (Interviewer, Candidate, Admin)

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-------------|
| **Backend** | Spring Boot 3, Spring WebSocket |
| **Language** | Java 17 |
| **Database** | PostgreSQL |
| **Real-Time** | WebSocket, STOMP |
| **Execution** | Docker (sandboxed) |
| **Build** | Maven |

---

## ✨ Core Features

### Interview Sessions
- 📧 **Session Management**
  - Create interview sessions
  - Invite candidates
  - Schedule interviews
  - Session recording (optional)
- 👤 **Role Management**
  - Interviewer privileges
  - Candidate permissions
  - Admin controls

### Coding Problems
- 👍 **Problem Generation**
  - Algorithm challenges
  - Data structure problems
  - System design questions
  - Difficulty levels (Easy, Medium, Hard)
- 📄 **Problem Details**
  - Problem description
  - Example test cases
  - Time/space constraints
  - Solution templates

### Real-Time Code Editor
- 🟰️ **Live Coding**
  - Multi-language support (Java, Python, C++, etc.)
  - Syntax highlighting
  - Real-time synchronization
  - Undo/redo functionality
- ⚡ **Code Execution**
  - Run code against test cases
  - Real-time output
  - Error reporting
  - Performance metrics (runtime, memory)

### Automated Grading
- ✅ **Test Validation**
  - Run hidden test cases
  - Check correctness
  - Memory/time limits
  - Edge case handling
- 📈 **Score Calculation**
  - Test pass rate
  - Code quality metrics
  - Time efficiency
  - Overall score

### Performance Analytics
- 💡 **Candidate Feedback**
  - Strengths & weaknesses
  - Code quality assessment
  - Problem-solving approach
  - Recommendations
- 📉 **Interview Analytics**
  - Completion rate
  - Average scores
  - Difficulty distribution
  - Candidate rankings

---

## 🚀 Getting Started

### Prerequisites
- Java 17+
- PostgreSQL 13+
- Docker (for code execution sandbox)
- Maven 3.8+

### Installation

```bash
# Clone repository
git clone https://github.com/SADRAMIS/interview-platform.git
cd interview-platform

# Configure application
cp src/main/resources/application.properties.example src/main/resources/application.properties

# Build
mvn clean package

# Run
mvn spring-boot:run
```

### Docker Setup
```bash
docker-compose up
```

---

## 📖 API Endpoints

### Sessions
- `POST /api/sessions` - Create interview session
- `GET /api/sessions` - Get user's sessions
- `GET /api/sessions/{id}` - Get session details
- `PUT /api/sessions/{id}` - Update session
- `DELETE /api/sessions/{id}` - End session

### Problems
- `GET /api/problems` - Get problem list (paginated)
- `GET /api/problems/{id}` - Get problem details
- `POST /api/problems` - Create problem (admin)
- `GET /api/problems/random` - Get random problem

### Code Submission
- `POST /api/submissions/run` - Run code (test cases)
- `POST /api/submissions/submit` - Final submission
- `GET /api/submissions/{id}` - Get submission details

### WebSocket (Real-Time)
- `/ws/interview/{sessionId}` - Join interview session
- `/ws/code/{sessionId}` - Code synchronization
- `/topic/interview/{sessionId}` - Broadcast updates

---

## 📊 Database Schema

### Key Tables
- **users** - User accounts (interviewer, candidate, admin)
- **interview_sessions** - Interview sessions
- **problems** - Problem repository
- **submissions** - Code submissions & results
- **test_cases** - Problem test cases
- **feedback** - Interview feedback & scores

---

## 🔐 Security

- ✅ JWT authentication
- ✅ Role-based access control
- ✅ Sandboxed code execution (Docker)
- ✅ Input validation
- ✅ Rate limiting
- ✅ Session management

---

## 🧪 Testing

```bash
# Run tests
mvn test

# With coverage
mvn clean test jacoco:report
```

---

## 🚧 Future Enhancements

- [ ] AI-powered problem recommendations
- [ ] Video recording & playback
- [ ] Live screen sharing
- [ ] Whiteboard collaboration
- [ ] Interview scheduling
- [ ] Email notifications
- [ ] Mobile app
- [ ] Multi-language support

---

## 🤝 Contributing

1. Fork the repository
2. Create feature branch: `git checkout -b feature/new-feature`
3. Commit changes: `git commit -m 'Add feature'`
4. Push: `git push origin feature/new-feature`
5. Open Pull Request

---

## 📄 License

MIT License - see [LICENSE](LICENSE) file

---

## 👨‍💼 Author

**SADRAMIS**
- [GitHub](https://github.com/SADRAMIS)
- [Email](mailto:ramis.sadykov.99@mail.ru)
- [Telegram](https://t.me/Ramzes196)

<div align="center">

### ⭐ Star this project if you find it useful!

*Made with ❤️ by SADRAMIS*

**Last Updated: December 2025**

</div>
