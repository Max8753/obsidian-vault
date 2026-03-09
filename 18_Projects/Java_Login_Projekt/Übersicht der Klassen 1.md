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
		1. user
		2. instance
	2. Methoden
		1. pruefen_ob_admin
2. SecurityUtil (Hashing, Registrieren und Überprüfen von Login)

Controller:
1. LoginController (nimmt LoginView entgegen und nutzt SecurityUtil und setzt die Session)
2. RegistrationController (Prüfung und gibt Befehl an UserRepository um den User in der DB zu speichern = Create. Das C von CRUD)
3. AdminController (Schutz von Löschung des letzten Admins usw.)

Views:
1. LoginView (Formulare für Anmelden und Registrieren)
	1. Attribute
		1. JTextField
	2. Methoden
2. RegistrationView( Formular für neue Nutzer)
3. DashboardView ( Hauptfenster nach dem Login - wenn Admin wird die Benutzerverwaltung geladen)
4. AdminManagementView (direkte Darstellung der User und ändern der Rechte, löschen der User)
5. User TableViewModel (Brauchen wir nur wegen Java Swing. Das JTable-Object kann nicht sagen ob Spalte 1 der Name ist oder Spalte 2 die Rolle. )

