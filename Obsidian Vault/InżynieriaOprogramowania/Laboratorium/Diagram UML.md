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
	+getCarnetStatus(): void
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
	+balance: String
	+carnet: Carnet

	+User(username: String, email: String, password: String, isTrainer: boolean)
	+getUsername(): String
	+getPassword(): String
}

class Accounting {
	-carnets: HashMap<String, Integer>
	-instance: Accounting

	-Accounting()
	+getInstance(): Accounting
	+getCarnets(): HashMap<String, Integer>
	+addMoney(user: User, double amount): void
	+getBalance(user: User): double
	+buyCarnet(type: String, User user): Carnet
	+extendCarnet(user: User): boolean
	+returnCarnet(user: User): boolean
}

class Carnet {
	-type: String
	-startTime: LocalDateTime
	-endTime: LocalDateTime
	-isActive: boolean

	+Carnet(type: String, startTime: LocalDateTime, endTime: LocalDateTime)
	+getStatus(): String
	+isActive(): boolean
	+updateStatus(): void
	+getEndTime(): LocalDateTime
	+setEndTime(): void
	+getType(): String
}

interface CalendarTrainer {
	+addClass(class: Class): void
	+getClasses(): ArrayList<Class>
	+getUserClasses(user: User): ArrayList<Class>
}

interface CalendarMember {
	+registerToClass(user: User, classId: int): boolean
	+getClasses(): ArrayList<Class>
	+getUserClasses(user: User): ArrayList<Class>
}

class Calendar {
	-classes: ArrayList<Class>
	-instance: Calendar

	+addClass(id: int, name: String, date: LocalDate, startTime: LocalTime, duration: int, maxSpaces: int, trainer: User): void
	+registerToClass(user: User, classID: int): boolean
	+getClasses(): ArrayList<Class>
	+getUserClasses(user: User): ArrayList<Class>
}

class Class {
	+id: int
	-name: String
	-date: LocalDate
	-startTime: LocalTime
	-duration: int
	-trainer: User
	+members: ArrayList<User>

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
``