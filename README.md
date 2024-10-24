# Robotica

În această temă trebuie să simulați o stație de încărcare pentru un vehicul electric, folosind mai multe LED-uri și butoane. În cadrul acestui task, trebuie să țineți cont de stările butonului și să folosiți debouncing, dar și să coordonați toate componentele ca într-un scenariu din viața reală.

## Materiale necesare:
- 4x LED-uri (pentru a simula procentul de încărcare)
- 1x LED RGB (pentru starea de liber sau ocupat)
- 2x Butoane (pentru start încărcare și stop încărcare)
- 8x Rezistoare (6x 220/330 ohm, 2x 1K ohm)
- Breadboard
- Linii de legătură

LED-ul RGB reprezintă disponibilitatea stației. Dacă stația este liberă, LED-ul va fi verde, iar dacă stația este ocupată, acesta se va face roșu.

### Detalii tehnice:
- **1** LED-urile simple reprezintă gradul de încărcare al bateriei, simulat printr-un loader progresiv:
  - L1 = 25%
  - L2 = 50%
  - L3 = 75%
  - L4 = 100%
  
  Loader-ul se încarcă prin aprinderea succesivă a LED-urilor, la un interval fix de 3 secunde. LED-ul care indică procentul curent de încărcare va clipi, în timp ce LED-urile anterioare vor rămâne aprinse, iar cele ulterioare vor rămâne stinse.

- **2** Apăsarea scurtă a butonului de start va porni încărcarea. În timpul procesului de încărcare, apăsarea din nou a butonului nu va avea efect.

- **3** Apăsarea lungă a butonului de stop va opri încărcarea forțat și va reseta stația la starea liberă. Dacă stația este deja liberă, apăsarea butonului de stop nu va face nimic.

### Scenariul de funcționare:
1. Stația este în starea ‘liberă’. Loader-ul este stins, iar LED-ul pentru disponibilitate este verde.
2. Se apasă butonul pentru start.
3. LED-ul de disponibilitate devine roșu, iar încărcarea începe prin aprinderea primului LED (L1).
4. LED-ul L1 clipește timp de 3 secunde, celelalte fiind stinse.
5. După ce încărcarea ajunge la 25%, LED-ul L1 rămâne aprins, iar LED-ul L2 începe să clipească.
6. Acest proces continuă până la finalizarea încărcării.
7. La finalizarea încărcării, toate LED-urile vor clipi simultan de 3 ori, apoi se vor stinge pentru a semnaliza încheierea procesului.
8. LED-ul pentru disponibilitate revine la verde.

Dacă în timpul încărcării butonul de stop este apăsat lung (minim 1 secundă), încărcarea se va întrerupe, iar LED-urile vor clipi de 3 ori pentru a semnala oprirea forțată, după care LED-ul pentru disponibilitate va deveni verde.

### Poze:
![IMG_2566 2](https://github.com/user-attachments/assets/2ba989f8-85af-4a56-b9ec-02b854b7a389)
![IMG_2565](https://github.com/user-attachments/assets/476419c8-3201-446b-8dfe-a01e8a2f5e95)
![IMG_2562](https://github.com/user-attachments/assets/47259baf-78a5-4752-9ca8-4c2d3c6514b5)


https://github.com/user-attachments/assets/948320c7-91c8-4119-a232-e421793b10f4



https://github.com/user-attachments/assets/614d1478-1603-440c-8239-09efc97b6981

<img width="937" alt="Screenshot 2024-10-24 at 14 49 49" src="https://github.com/user-attachments/assets/aa615d00-a793-4867-84ab-81a2fa1cfd2c">






