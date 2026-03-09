Models & Hauptklassen
1. Main-Klasse (Startpunkt der Applikation)
	1. Attribute
		1. appStart = true;
	2. Methoden
		1. main-methode
		2. appStart-methode(while (appStart) {})

2. User (Das User Objekt. Eine Klasse, bekommt die UserRechte zugeteilt)
	1. Attribute
		1. id (PRIMARY_KEY - AUTO_INCREMENT)
		2. username
		3. pass
		4. rolle
	2. Methoden
	3. Konstruktor
		1. getter & setter
3. UserPool (Wer ist angemeldet? Aus technischer Sicht, keine View)
4. Database Connection
5. UserRepository (CRUD)

Hilfsklassen:
1. SessionContext/UserPool(Welcher User ist mit welcher Rolle angemeldet) (eventuell Löschen)
	1. Attribute
		1. private User user
		2. private static instance
	2. Methoden
		1. public static SessionContext getInstance()
		2. public void setUser(User user)
		3. public User getUser()
		4. public boolean isAdmin()
		5. public void logout()`
2. SecurityUtil (Hashing, Registrieren und Überprüfen von Login)
	1. Methoden
		1. String hashPassword(String password)
		2. boolean login(String username, String password)
		3. boolean validateRegistration(String username, String password, String confirmPassword)

Controller:
1. LoginController (nimmt LoginView entgegen und nutzt SecurityUtil und setzt die Session)
	1. **Attribute
		1. LoginView view
		2. UserRepository userRepository
	2. Methoden
		1. void login(String username, String password)
2. RegistrationController (Prüfung und gibt Befehl an UserRepository um den User in der DB zu speichern = Create. Das C von CRUD)
	1. Attribute
		1. RegistrationView view
		2. UserRepository userrepository
	2. Methoden
		1. void registerUser(String username, String password, String confirmPassword)
3. AdminController (Schutz von Löschung des letzten Admins usw.)
	1. Attribute
		1. AdminManagementView view
		2. UserRepository userRepository`
	2. Methoden
		1. void deleteUser(int userId)
		2. void changeUserRole(int userId, String role)
		3. List<User> getAllUsers()void changeUserRole(int userId, String role)
Views:
5. LoginView (Formulare für Anmelden und Registrieren)
	1. Attribute
		1. JFrame frame
		2. JTextField usernameField
		3. JPasswordField passwordField
		4. JButton loginButton
		5. JButton registerButton
		6. JLabel errorLabel`
	2. Methoden
		1. getUsername()
		2. getPassword()
		3. showError(String message)
		4. 
6. RegistrationView( Formular für neue Nutzer)
7. DashboardView ( Hauptfenster nach dem Login - wenn Admin wird die Benutzerverwaltung geladen)
8. AdminManagementView (direkte Darstellung der User und ändern der Rechte, löschen der User)
9. User TableViewModel (Brauchen wir nur wegen Java Swing. Das JTable-Object kann nicht sagen ob Spalte 1 der Name ist oder Spalte 2 die Rolle. )

