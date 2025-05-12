```plantuml
class UserInterface {
	+authenticator: Authenticator
	+accounting: Accounting
	+calendar: Calendar
	+user: User

	+showMenu(): void
	+exit(): void
	+register(): void
	+login(): void
	+showLoggedMenu(): void
	+addMoney(): void
	+getCarnets(): void
	+buyCarnet(): void
	+extendCarnet(): void
	+returnCarnet(): void
	+getClasses(): void
	+registerToClass(): void
	+addClass(): void
}

class Authenticator {
	-registeredUsers: ArrayList<User>
	-instance: Authenticator

	-Authenticator()
	+getInstance(): Authenticator
	+register(username: String, email: String, password: String, asTrainer: boolean): User
	+login(username: String, password: String): User
	+getCode(User user): String
}

class User {
	-username: String
	-email: String
	-password: String
	-isTrainer: boolean
	-balance: String
	-carnet: Carnet
	-calendar: Calendar

	+User(username: String, email: String, password: String, isTrainer: boolean)
}

class Accounting {
	-carnets: HashMap<String, Integer>
	-instance: Accounting

	-Accounting()
	+getInstance(): Accounting
	+getCarnets(): ArrayList<String>
	+addMoney(user: User): void
	+buyCarnet(type: String, User user)
	+extendCarnet(user: User)
	+returnCarnet(user: User)
}

class Carnet {
	-type: String
	-startTime: LocalDateTime
	-endTime: LocalDateTime
	-isActive: boolean

	+Carnet(type: String, startTime: LocalDateTime, endTime: LocalDateTime)
	+getStatus(): String
	+updateStatus(): void
}

interface CalendarTrainer {
	+addClass(class: Class): void
	+getClasses(): ArrayList<Class>
	+getUserClasses(user: User): ArrayList<Class>
}

interface MemberCalendar {
	+registerToClass(user: User): boolean
	+getClasses(): ArrayList<Class>
	+getUserClasses(user: User): ArrayList<Class>
}

class Calendar {
	-classes: ArrayList<Class>
	-instance: Calendar

	+addClass(class: Class): void
	+registerToClass(user: User): boolean
	+getClasses(): ArrayList<Class>
	+getUserClasses(user: User): ArrayList<Class>
}

class Class {
	-id: int
	-name: String
	-date: LocalDate
	-startTime: LocalTime
	-duration: int
	-trainer: User
	-members: ArrayList<User>

	+Class(name: String, date: LocalDate, startTime: LocalTime, duration: int)
	+getInfo(): String
}

UserInterface --> Authenticator
UserInterface --> Accounting
UserInterface --> Calendar
UserInterface --> User

Authenticator --> User : registers/logins
Accounting --> User : manages balance & carnet
User --> Carnet : owns >
User --> Calendar : uses >
Carnet --> "LocalDateTime" : start/end times
Calendar --> Class : manages >
Class --> User : trainer
Class --> User : members *
Calendar <|.. CalendarTrainer
Calendar <|.. MemberCalendar
```
