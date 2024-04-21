# ESP32-BLE-SERVER
Initializing a BLE Server on an ESP32 to connect to trough a mobile device and request information about Game of Thrones characters from an API.
In functia setup se initializeaza cele 2 seriale Bluetooth si Arduino si se conecteaza la wifi.
In functia loop se verifica daca placuta s-a imperecheat cu un dispozitiv, daca aceasta s a
imperecheat se citeste requestul dat de catre dispozitiv. Daca requestul este de tipul
{"action":"getData"} inseamna ca noi trebuie sa afisam sub aceasta forma {id: int|string, name:
string, image: string (url|base64)}}. Conecteaza la api folosind protocolul http si se salveaza datele
intr un document json pe care il vom deserializa si formata pentru a obtine stringul dorit. Daca
requestul citit a fost de tipul {"action":"getDetails","id":"numarid"}; atunci trebuie sa deserializam
stringul pentru a extrage numarid. Dupa aceasta vom interoga api ul cu expresia “ id?= “ si vom
extrage datele intr un document json pe care il vom deserializa si formata pentru a obtine stringul
de forma {id: int|string, name: string, image: string (url|base64)},description: string,
teamId:string};
