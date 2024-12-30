
   Dupa ce ai terminat testele de calibrare si ai reusit sa corectezi miscarile robotului, poti incepe sa faci traiectorii. 

Pentru a face traiectorii mai rapid, foloseste-te de Path Generator (https://pedro-path-generator.vercel.app).

### Codul e structurat astfel:
1.  (optional)Declararea Path-urilor si/sau pozitiei de inceput:

![[pose_example.png]]
2. Declararea subsistemelor utilizate:

![[subsistems.png]]

 3.Declararea path-urilor:

Un "path" reprezintă o secvență de puncte prin care robotul trebuie să treacă.

- **Ce este un path?**
    - Un set de puncte predefinite (x, y, unghi) pe care robotul le va urma.
    - Poate include curbe, linii drepte sau rotații.
- **Tipuri de path-uri**:
    - **Liniare**: Mișcări simple între două puncte.
    - **Curbe**: Mișcări fluide care conectează punctele într-un mod elegant.
    - **Mixte**: Combinații de linii drepte și curbe pentru o traiectorie mai complexă

### Path liniar:
![[Path.png]]

### Curve Path:
![[Path.spline.png]]


#### Dupa fiecare Path declarat, trebuie specificata tipul heading-ului pe care robotul il va urma.

Heading-ul poate fi:
     1. Constant: o sa mentina un unghi pe tot parcursul path-ului.
     2.Linear: o sa faca tranzitie de la un unghi la altul in decursul traiectoriei.
     3.Tangential: o sa isi ia heading-ul in functie de linia pe care o parcurge.
