
Această clasă este un **subsistem** care gestionează motoarele șasiului și logica de mișcare mecanum.

#### **Principalele componente ale clasei:**

1. **Declarația motoarelor și configurarea acestora:**
    
    - Creează patru motoare cu encodere: `leftFront`, `rightFront`, `leftRear`, `rightRear`.
    - Fiecare motor este configurat cu comportamentul `BRAKE`, care oprește robotul imediat după ce comanda încetează să fie activă.
    - Se folosește enum-ul `Motor.GoBILDA.RPM_435` pentru a seta specificațiile motoarelor.
2. **MecanumDrive:**
    
    - Se inițializează un obiect `MecanumDrive`, care preia cele patru motoare pentru a implementa logica de mișcare mecanum.
3. **Metoda `driveRobotCentric`:**
    
    - Permite robotului să se deplaseze într-un mod centrat pe robot (robot-centric).
    - Primește vitezele pentru strafe, mers înainte/înapoi și rotire și le transmite lui `MecanumDrive`.