
**După ce ai descărcat tot ce trebuie**, este momentul să înveți cum să implementezi un modul TeleOp folosind FTCLib. Aceasta este o bibliotecă robustă și flexibilă care îți simplifică procesul de programare și îți oferă acces la funcționalități avansate pentru a controla robotul.

Pentru a invata totul despre FTCLIB, trebuie sa te uiti pe documentatia oficiala:
https://docs.ftclib.org/ftclib

### **Ce este FTCLib?**

FTCLib este o bibliotecă dezvoltată pentru a îmbunătăți modul în care scrii cod pentru FTC. Aceasta aduce:

- **Abstracții mai intuitive** pentru componentele hardware (motoare, servo-uri, senzori etc.).
- O implementare simplificată a designului bazat pe comenzi, care ajută la crearea unor programe modulare și scalabile.
- Funcționalități extinse pentru gestionarea subsistemelor robotului.


#### **Ce putem folosi din FTCLib?**

1. **Componente hardware avansate**:
    
    - FTCLib oferă metode alternative pentru gestionarea componentelor electronice, cum ar fi:
        - Motoare cu encodere (cu metode pentru setarea vitezei, poziției și accelerării).
        - Senzori (inclusiv procesare ușoară a datelor).
        - Controlere gamepad optimizate.
2. **Subsisteme si Comenzi:
    
    - FTCLib adoptă un design modular, unde funcționalitățile robotului sunt împărțite în subsisteme.
    - Acest model permite gestionarea facilă a sarcinilor complexe, cum ar fi integrarea mai multor subsisteme într-un singur TeleOp.
3. **Tool-uri auxiliare**:
    
    - FTCLib include instrumente pentru control PID, ajustări de viteze, și alte optimizări avansate.

### **Avantajele FTCLib pentru TeleOp**

- **Integrare rapidă și eficientă**: Configurarea și utilizarea componentelor hardware sunt mult mai simple.
- **Design scalabil**: Adăugarea de funcționalități suplimentare este facilă datorită structurii bazate pe subsisteme și comenzi.
- **Flexibilitate**: Poți combina diferite comenzi și subsisteme pentru a crea programe complexe fără efort suplimentar.

### **CommandOpMode și CommandGroups**

FTCLib utilizează un framework bazat pe comenzi pentru a structura programele:

1. **CommandOpMode**:
    
    - Acesta este punctul central al programului tău TeleOp.
    - Permite gestionarea ușoară a subsistemelor și comenzilor.
    - Este folosit pentru a inițializa subsistemele și comenzile la începutul rundei TeleOp.
2. **CommandGroups**:
    
    - Oferă posibilitatea de a combina mai multe comenzi într-o secvență sau de a le rula în paralel.
    - Tipuri de CommandGroups:
        - **SequentialCommandGroup**: Comenzile sunt executate una după alta.
        - **ParallelCommandGroup**: Comenzile sunt executate simultan.


### **Subsistemele în FTCLib**

Un subsistem reprezintă o unitate logică a robotului (ex.: șasiu, braț, prindere).

- **Cum se creează un subsistem?**
    
    - Creezi o clasă care extinde `SubsystemBase`.
    - Definești metodele de control pentru subsistem (ex.: `moveForward()` pentru șasiu).
    - Integrezi subsistemul în `CommandOpMode`.
- **De ce să folosești subsisteme?**
    
    - Separația logică ajută la reducerea complexității codului.
    - Permite reutilizarea codului pentru diverse moduri de operare.