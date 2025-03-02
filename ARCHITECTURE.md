```plaintext
C4Model
    Person(student, "Student")
    Person(counselor, "Counselor")
    System_Boundary(bookingSystem, "Counseling Booking System") {
        Container(webApp, "Web Application", "React", "User interface for students to view and book sessions")
        Container(api, "Backend API", "Node.js", "Handles business logic and manages sessions")
        ContainerDb(db, "Database", "PostgreSQL", "Stores user data, appointments, and available slots")
    }
    Rel(student, webApp, "Uses")
    Rel(counselor, webApp, "Uses")
    Rel(webApp, api, "API Calls")
    Rel(api, db, "Reads/Writes to Store Appointments")
