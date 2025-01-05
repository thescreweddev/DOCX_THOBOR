### **Cum funcționează împreună?**

1. **Inițializare:**
    
    - La început, `TeleOP` configurează subsistemul și comanda, apoi le conectează între ele.
    - Comanda `DriveCommand` preia intrările gamepad-ului pentru a controla robotul.
2. **Execuție:**
    
    - În timpul rulării TeleOp, metoda `execute` din `DriveCommand` este apelată constant.
    - Aceasta transmite valorile de mișcare (`strafeSpeed`, `forwardSpeed`, `turnSpeed`) subsistemului, care le folosește pentru a deplasa robotul.
3. **Design modular:**
    
    - Logica de mișcare este separată în subsistem (`DriveSubsystem`), iar logica de comandă este în clasa `DriveCommand`.
    - Aceasta permite reutilizarea și extinderea ușoară a codului.

Aici o sa gasesti tot codul:

