# Mesh Detect

[![Status: Development](https://img.shields.io/badge/Status-Development-orange.svg)]()
[![Hardware: Meshy V1](https://img.shields.io/badge/Hardware-Meshy%20V1-blue.svg)]()
[![Network: LoRa Mesh](https://img.shields.io/badge/Network-LoRa%20Mesh-green.svg)]()
[![License: TBD](https://img.shields.io/badge/License-TBD-lightgrey.svg)]()

## O Projekcie

Tworzymy platformę **Mesh Detect**, która zamienia dźwięk otoczenia w natychmiastowe, geolokalizowane alerty operacyjne. Nasz system to zdecentralizowana sieć urządzeń terenowych (Meshy V1), która wykrywa i klasyfikuje incydenty w czasie rzeczywistym – od wypadków drogowych i aktów przemocy po drony i zdarzenia kryzysowe. 

**Privacy by Design:** System gwarantuje pełną prywatność. Przetwarzanie dźwięku odbywa się w 100% na urządzeniu (Edge Computing). System nie nagrywa, nie zapisuje i nie streamuje żadnego sygnału audio. Ponadto urządzenie fizycznie nie ma możliwości rozpoznawania ludzkiej mowy – reaguje wyłącznie na wyuczone sygnatury zdarzeń akustycznych.

---

## Architektura Techniczna

Architektura projektu została podzielona na fazę prototypową oraz docelowe rozwiązanie oparte na autorskim sprzęcie.

### Wersja Docelowa (Produkcyjna)
* **Urządzenie Meshy V1:** W pełni autorskie PCB (Custom PCB) zoptymalizowane pod kątem niskiego poboru mocy i przetwarzania brzegowego.
* **Edge AI & Model AST:** Do analizy sygnału wykorzystujemy model **AST (Audio Spectrogram Transformer)**. Cała inferencja (wnioskowanie) odbywa się lokalnie na urządzeniu.
* **Komunikacja:** Brak jakiegokolwiek streamingu audio. Urządzenia komunikują się wyłącznie w zamkniętej sieci **Mesh (np. LoRa)**, przesyłając do centrali jedynie lekkie metadane (typ zagrożenia, czas, koordynaty GPS, pewność detekcji).

### Faza MVP (Obecna)
* **Sprzęt:** Wykorzystujemy **Respeaker Core V2** jako platformę przejściową do walidacji koncepcji.
* **Transmisja:** Komunikacja i tunelowanie TCP są używane **wyłącznie** na etapie MVP w celach deweloperskich i testowych.

---

## Kluczowe Funkcje (Features)

* **Przetwarzanie brzegowe (Edge Computing):** Natychmiastowa analiza akustyczna bez opóźnień sieciowych i bez polegania na chmurze obliczeniowej.
* **Zaawansowana detekcja AST:** Wykorzystanie Audio Spectrogram Transformer do precyzyjnej klasyfikacji dźwięków (np. strzały, drony, tłuczone szkło).
* **Bezpieczeństwo i Prywatność (Zero Audio):** Architektura uniemożliwiająca podsłuchiwanie, nagrywanie czy rozpoznawanie mowy.
* **Autonomiczna sieć Mesh:** Urządzenia tworzą samonaprawiającą się sieć z wykorzystaniem technologii LoRa, uniezależniając się od klasycznej infrastruktury GSM/Wi-Fi.
* **Bezszwowa Integracja:** Zamiast tworzyć kolejne powiadomienia SMS, dostarczamy API i webhooki do integracji z już istniejącymi systemami dyspozytorskimi, VMS (Video Management Systems) oraz centrami dowodzenia (C2).

---

## Zastosowania (Use Cases)

1.  **Bezpieczeństwo Publiczne (Smart City):** Integracja z miejskim monitoringiem wizyjnym w celu automatycznego nakierowywania kamer PTZ na miejsce zdarzenia.
2.  **Ochrona Infrastruktury Krytycznej:** Monitorowanie rozległych terenów (np. rurociągów, granic) z użyciem rozproszonej sieci Mesh bez dostępu do internetu.
3.  **Zastosowania Obronne:** Detekcja dronów i obiektów nisko lecących w trudnym terenie.
4.  **Monitoring Środowiskowy:** Autonomiczne czujniki wykrywające nielegalną wycinkę drzew lub kłusownictwo, działające miesiącami na zasilaniu bateryjnym.

---

## Nasz Zespół

<table align="center" width="100%">
  <tr>
    <td align="center" width="33%">
      <img width="120" alt="zuza" src="https://github.com/user-attachments/assets/03371df1-593f-4f29-9ce6-c73cb86f9ee6" /><br><br>
      <strong>Zuzanna Żyła</strong><br>
      <em>Co-Founder</em><br><br>
      <a href="mailto:hi@zuza.cc"><kbd>hi@zuza.cc</kbd></a> &nbsp; 
      <a href="https://www.linkedin.com/in/hi-zuzanna-zyla/"><kbd>linkedin.com/in/hi-zuzanna-zyla</kbd></a>
    </td>
    <td align="center" width="33%">
      <img width="120" alt="julek" src="https://github.com/user-attachments/assets/d0ee135c-2acf-47be-ab86-ed5af0e61441" /><br><br>
      <strong>Julian Stanisławek</strong><br>
      <em>Co-Founder</em><br><br>
      <a href="mailto:hi@infox.dev"><kbd>hi@infox.dev</kbd></a> &nbsp; 
      <a href="https://linkedin.com/in/infox1337/"><kbd>linkedin.com/in/infox1337</kbd></a>
    </td>
    <td align="center" width="33%">
      <img width="120" alt="timmy" src="https://github.com/user-attachments/assets/96433452-fa50-489e-9a69-663bb1ba2899" /><br><br>
      <strong>Tymoteusz Marzec</strong><br>
      <em>Co-Founder</em><br><br>
      <a href="mailto:tymoteusz.marzec.dev@gmail.com"><kbd>tymoteusz.marzec.dev@gmail.com</kbd></a> &nbsp; 
      <a href="https://linkedin.com/in/tymoteusz-marzec-dev/"><kbd>linkedin.com/in/tymoteusz-marzec-dev</kbd></a>
    </td>
  </tr>
</table>

---

## Kontakt i Zapytania

Jesteś zainteresowany wdrożeniem systemu lub współpracą? Zapraszamy do kontaktu:

* **Ogólne zapytania projektowe:** [support@infox.dev](mailto:support@infox.dev)
* **Wsparcie techniczne:** [support@infox.dev](mailto:support@infox.dev)

---

## Licencja

Obecny status licencji: **#TBD** (To Be Determined).
Wszystkie prawa do kodu źródłowego i schematów architektury są zastrzeżone do momentu publikacji oficjalnej licencji.
