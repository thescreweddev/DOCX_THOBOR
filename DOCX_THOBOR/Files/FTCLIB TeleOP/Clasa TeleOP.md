
Aceasta este clasa principală pentru modul TeleOp, implementată folosind design-ul bazat pe comenzi.

#### **Principalele componente ale clasei:**

1. **Obiecte declarate:**
    
    - `DriveSubsystem driveSubsystem`: Subsistemul care gestionează mișcarea robotului.
    - `DriveCommand driveCommand`: Comanda care controlează subsistemul.
    - `GamepadEx gmp1, gmp2`: Obiecte care simplifică accesul la gamepad-uri.
2. **Metoda `initialize`:**
    
    - Configurează toate componentele necesare pentru TeleOp:
        - Inițializează subsistemul de conducere (`DriveSubsystem`).
        - Creează obiectele `GamepadEx` pentru acces ușor la intrările gamepad-ului.
        - Creează comanda `DriveCommand`, folosind valorile de intrare de la joystick-urile gamepad-ului 1 (`gmp1`).
        - Setează comanda `DriveCommand` ca **comandă implicită** (`setDefaultCommand`) pentru `DriveSubsystem`, astfel încât aceasta să fie activă în mod continuu.



