Dokumentacja projektu

Domowe Laboratorium | Windows Server 2016 + Windows 10 (Hyper-V)

Projekt domowego laboratorium w celu nauki administracji systemami Windows oraz zapoznania się z narzędziem do wirtualizacji Hyper-V. Utworzyłem środowisko wirtualne w Hyper-V na moim komputerze osobistym z systemem Windows 10 Pro, składające się z serwera Windows Server 2016 oraz maszyny klienckiej Windows 10.

Cel projektu: utworzenie maszyn wirtualnych (wirtualne dyski, karty sieciowe, przydzielenie zasobów procesora i pamięci, instalacja systemów), instalacja Active Directory na serwerze i podłączenie klienta do domeny (użytkownicy, grupy, zasady grupy, profil mobilny, udostępnienie zasobów dyskowych), konfiguracja usługi DHCP oraz Routingu (żeby klient miał dostęp do internetu), konfiguracja DNS oraz serwera WWW, snapshoty/checkpointy w Hyper-V.

1. Konfiguracja Hyper-V:
- utworzenie maszyn oraz dysków wirtualnych
- przydzielenie zasobów procesora/pamięci
- utworzenie wirtualnych kart sieciowych

Serwer posiada 2 karty sieciowie, jedną w trybie pracy NAT, aby miał dostęp do internetu, druga karta pracuje w sieci wewnętrznej. Klient posiada tylko jedną kartę sieciową w sieci wewnętrznej, jak na razie nie ma dostępu do internetu.

<img width="235" height="369" alt="image" src="https://github.com/user-attachments/assets/0ebe51d9-fd30-4bca-8461-67fddce89264" />

<img width="240" height="323" alt="image" src="https://github.com/user-attachments/assets/b55f4f28-88e3-4522-a85c-fc6d4ebcc9e6" />

<img width="558" height="271" alt="image" src="https://github.com/user-attachments/assets/9838d895-d1a9-46c1-a398-6ca13749d159" />

2. Instalacja systemów:
- Windows Server 2016
- Windows 10 Pro

<img width="638" height="479" alt="image" src="https://github.com/user-attachments/assets/123842ac-d130-4838-bd8a-81360001d94b" />

<img width="635" height="475" alt="image" src="https://github.com/user-attachments/assets/da642532-2893-4608-a088-aa0cb27c0f10" />

3. Konfiguracja serwera:
- zmiana nazwy administratora i wyłączenie domyślnego konta admina
- ustawienie adresu ip

<img width="374" height="383" alt="image" src="https://github.com/user-attachments/assets/2f39a0c0-c9b3-4bea-ab3c-e6ca0f7417e9" />

<img width="524" height="393" alt="image" src="https://github.com/user-attachments/assets/0c8091c6-1896-44d8-bd51-a30ae4a3e00b" />

<img width="377" height="223" alt="image" src="https://github.com/user-attachments/assets/31022b48-fc97-4d04-b95b-367616c63904" />

<img width="395" height="449" alt="image" src="https://github.com/user-attachments/assets/db019065-c02f-4f80-acc2-609c097cc9f6" />

4. Konfiguracja klienta:
- ustawienie adresu ip, bramy domyślnej, serwera DNS
- test połączenia z serwerem

<img width="396" height="449" alt="image" src="https://github.com/user-attachments/assets/39e46f89-580c-4df0-a036-7bf71f03ed07" />
<img width="455" height="210" alt="image" src="https://github.com/user-attachments/assets/ce5944a4-6115-4054-841e-9820fa505c97" />

5. Active Directory:
- Instalacja
- Tworzenie lasu i domeny
- Jednostki organizacyjne, grupy, dodawanie użytkowników
- Profil mobilny
- Udostępnienie zasobu dyskowego


<img width="749" height="454" alt="image" src="https://github.com/user-attachments/assets/1ce5dfbd-25c0-4487-ba52-4ce911d9399f" />

<img width="432" height="170" alt="image" src="https://github.com/user-attachments/assets/4c9e384a-8a20-474d-ae66-df04d82b619d" />

<img width="439" height="218" alt="image" src="https://github.com/user-attachments/assets/0cee9d28-f0bb-47a4-86b6-edcf893ee99a" />

<img width="418" height="531" alt="image" src="https://github.com/user-attachments/assets/9f19d205-8b9a-4953-9042-39a5d84318bf" />

6. Ponowna konfiguracja klienta:
- przyłączenie komputera do domeny
- logowanie do systemu

<img width="609" height="482" alt="image" src="https://github.com/user-attachments/assets/b02af264-5556-4d5b-b90a-f4fd5042c972" />

<img width="499" height="553" alt="image" src="https://github.com/user-attachments/assets/08eb2533-9b73-4dfb-9b29-5949bf9d3c06" />

<img width="649" height="770" alt="image" src="https://github.com/user-attachments/assets/0f6fb4a3-8f76-410b-bb43-4a9528892037" />

<img width="271" height="168" alt="image" src="https://github.com/user-attachments/assets/40efcdc9-9331-449b-8837-03bbe3d1a5bd" />

7. Zasady grupy (Group Policy):
- blokujemy pracownikom dostęp do wiersza poleceń oraz panelu sterowania

<img width="898" height="601" alt="image" src="https://github.com/user-attachments/assets/6497d928-e363-4909-b0fd-e9e4f112b376" />

<img width="936" height="492" alt="image" src="https://github.com/user-attachments/assets/d39f69a5-8c68-46aa-9656-d4b2080b3bf9" />

<img width="413" height="95" alt="image" src="https://github.com/user-attachments/assets/60e96226-6c7f-42ab-b1ec-3a0bb3da4b99" />

Klient po aktualizacji zasad:

<img width="518" height="139" alt="image" src="https://github.com/user-attachments/assets/8288e4e1-88ef-40e6-b99a-68f73aa8adb7" />

<img width="795" height="484" alt="image" src="https://github.com/user-attachments/assets/ee985172-237c-48c4-a97b-ffe0a4ab542b" />

8. DHCP & Routing:
- instalacja usługi DHCP i routingu
- tworzenie nowego zakresu
- przydzielenie adresu ip klientowi
- konfiguracja routingu i uzyskanie dostępu do internetu przez klienta

<img width="764" height="460" alt="image" src="https://github.com/user-attachments/assets/1ccd4fdb-c2ee-468e-8b99-963e5cc01c4f" />

<img width="774" height="510" alt="image" src="https://github.com/user-attachments/assets/d577a867-c40b-4555-9056-aed49f539c53" />

<img width="588" height="498" alt="image" src="https://github.com/user-attachments/assets/681cfcef-9ef5-4fce-a490-b7c3ca9d8855" />

<img width="632" height="466" alt="image" src="https://github.com/user-attachments/assets/262161b6-f09b-4098-a7b4-5c319a569aa5" />

<img width="619" height="441" alt="image" src="https://github.com/user-attachments/assets/f8e86fd2-751b-4f83-ab1a-10bff9999c43" />

Klient:

<img width="398" height="450" alt="image" src="https://github.com/user-attachments/assets/71921d36-2e38-43d6-9115-167acc42a721" />

<img width="549" height="207" alt="image" src="https://github.com/user-attachments/assets/a0bf6b82-f786-4d2d-9d5e-a76685123fda" />

Klient uzyskał dostęp do internetu:

<img width="246" height="126" alt="image" src="https://github.com/user-attachments/assets/4f2fa819-2a9d-44a2-b492-e8f1b711d4d3" />

9. DNS:
- stworzenie strefy wyszukiwania do przodu
- stworzenie stefy wyszukiwania wstecznego
- dodanie nowego hosta
- wskazanie rekordu jako główny serwer dla strefy
- klient korzysta z usługi DNS

<img width="752" height="526" alt="image" src="https://github.com/user-attachments/assets/ce6d6bf6-0939-4621-ae84-344556e7f4ac" />

<img width="748" height="521" alt="image" src="https://github.com/user-attachments/assets/6a41f50c-c6b4-43ba-9a3f-598d801726aa" />

<img width="755" height="522" alt="image" src="https://github.com/user-attachments/assets/c2ce722e-4cf2-4a6c-b008-dc4d84a2c995" />

<img width="750" height="530" alt="image" src="https://github.com/user-attachments/assets/5f37a089-24aa-47b3-b3d1-4a920d3b22b4" />

Klient:

<img width="446" height="168" alt="image" src="https://github.com/user-attachments/assets/957fb496-8f6b-4d38-b528-d0caaddac5a8" />

10. IIS:
- utworzenie nowej witryny na serwerze
- dodanie rekordu www w strefie
- wyświetlenie witryny na kliencie

<img width="773" height="592" alt="image" src="https://github.com/user-attachments/assets/bb858388-2b38-41a0-b38d-c39f0a71ac75" />

<img width="751" height="530" alt="image" src="https://github.com/user-attachments/assets/9b1154d8-fc5c-40db-a604-2dba27f13942" />

Strona www po stronie klienta:

<img width="470" height="240" alt="image" src="https://github.com/user-attachments/assets/7a4f7a0a-fee5-4524-ad08-b0aa353286e5" />

11. Snapshoty/Checkpointy w Hyper-V:
- utworzenie checkpointu
- dodanie nowych plików na serwerze
- powrót do checkpointu
- udany powrót (pliki zniknęły)

<img width="554" height="348" alt="image" src="https://github.com/user-attachments/assets/2af16b13-95b9-421b-9974-57445d70dd7c" />

<img width="543" height="178" alt="image" src="https://github.com/user-attachments/assets/43a1ca59-f3d7-4658-9ccf-919c37446674" />

<img width="558" height="237" alt="image" src="https://github.com/user-attachments/assets/b8ca2abe-d8d9-4bc5-9575-7f98e887db12" />

<img width="511" height="129" alt="image" src="https://github.com/user-attachments/assets/31f7c441-9598-4ad3-929c-529bca17d9b9" />

















































