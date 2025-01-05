
Această clasă reprezintă o **comandă** care controlează mișcarea robotului într-un mod centrat pe robot (robot-centric).

#### **Principalele componente ale clasei:**

1. **Câmpurile clasei:**
    
    - `DriveSubsystem driveSubsystem`: Subsistemul responsabil pentru mișcarea robotului.
    - `DoubleSupplier strafeSpeed, forwardSpeed, turnSpeed`: Funcții lambda care preiau valorile de mișcare (pentru strafe, mers înainte/înapoi și rotire) de la gamepad.
2. **Constructor:**
    
    - Inițializează subsistemul de conducere și vitezele de mișcare.
    - Folosește metoda `addRequirements` pentru a specifica faptul că această comandă utilizează `DriveSubsystem`.
3. **Metoda `execute`:**
    
    - Se execută continuu cât timp comanda este activă.
    - Apelează metoda `driveRobotCentric` din subsistem, trimițând valorile de mișcare de la gamepad (inversate pentru a reflecta orientarea corectă).