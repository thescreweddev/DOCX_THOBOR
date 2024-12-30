   **Pe lângă RoadRunner și PedroPathing, există o serie de alte soluții care pot fi utilizate pentru a implementa autonomia robotului în competițiile FTC. Acestea variază în complexitate și flexibilitate, oferind opțiuni pentru diverse niveluri de experiență și cerințe tehnice.
   




#### **1. Pure Pursuit Path Following**

  O metodă matematică simplă și eficientă pentru urmărirea traiectoriilor bazată pe puncte de referință. Este ideală pentru echipele care preferă să dezvolte soluții personalizate.
  
- **Avantaje**:
    - Ușor de implementat pentru traiectorii de bază.
    - Permite personalizări flexibile pentru specificul robotului.
- **Dezavantaje**:
    - Mai puțin precis decât soluții avansate precum RoadRunner.
    - Necesită cunoștințe matematice pentru o implementare eficientă.

---

#### **2. Vuforia și TensorFlow pentru navigare bazată pe viziune**
  
  FTC suportă utilizarea **Vuforia** (pentru localizarea pe baza imaginilor țintă) și **TensorFlow** (pentru recunoașterea obiectelor). Aceste instrumente permit navigația autonomă bazată pe informații vizuale.
  
- **Avantaje**:
    - Poate combina recunoașterea obiectelor cu navigația autonomă.
    - Ideal pentru adaptabilitate în timp real.
- **Dezavantaje**:
    - Poate fi influențată de condițiile de iluminare.
    - Necesită resurse hardware suplimentare, precum o cameră performantă.


#### **3. Autonomie bazată pe senzori (de la zero)**

   Construirea autonomiei folosind senzori precum giroscopul, encoder-ele motoarelor, senzorii de distanță și de culoare.
   
- **Avantaje**:
    - Control complet asupra comportamentului robotului.
    - O metodă excelentă de a învăța principiile de bază ale navigației autonome.
- **Dezavantaje**:
    - Necesită mai mult timp pentru dezvoltare și testare.
    - Poate fi mai puțin precisă fără algoritmi avansați.

--- 
