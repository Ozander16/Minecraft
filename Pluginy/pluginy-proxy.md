# PlUGINY NA PROXY

## Spis Treści:
- [LuckPermsBungee](https://github.com/vBagieta/Minecraft/blob/main/Pluginy/pluginy-proxy.md#luckpermsbungee---menad%C5%BCer-globalnych-permisji)
  - [Podpinanie bazy danych](https://github.com/vBagieta/Minecraft/blob/main/Pluginy/pluginy-proxy.md#jak-podpi%C4%85%C4%87-baze-danych-w-luckpermsie)

- [SparkBungee](https://github.com/vBagieta/Minecraft/blob/main/Pluginy/pluginy-proxy.md#sparkbungee---kontrola-dzia%C5%82ania-serwera-proxy)
  - [Permisje Sparka](https://github.com/vBagieta/Minecraft/blob/main/Pluginy/pluginy-proxy.md#permisje-pluginu-sparkbungee)

- [PlayerBalancer](https://github.com/vBagieta/Minecraft/blob/main/Pluginy/pluginy-proxy.md#playerbalancer---balansuj-graczy-pomi%C4%99dzy-serwerami)
  - [Zasady przełączania graczy](https://github.com/vBagieta/Minecraft/blob/main/Pluginy/pluginy-proxy.md#gracze-mog%C4%85-by%C4%87-prze%C5%82%C4%85czani-pomi%C4%99dzy-serwerami-za-pomoc%C4%85-zasad)
  - [Permisje PlayerBalancer](https://github.com/vBagieta/Minecraft/blob/main/Pluginy/pluginy-proxy.md#permisje-pluginu-player-balancer)

- [BMsg](https://github.com/vBagieta/Minecraft/blob/main/Pluginy/pluginy-proxy.md#bmsg---globalne-wiadomo%C5%9Bci-prywatne-i-wi%C4%99cej)
  - [Permisje BMsg](https://github.com/vBagieta/Minecraft/blob/main/Pluginy/pluginy-proxy.md#permisje-pluginu-bmsg)

## Pluginy:

# LuckPermsBungee - Menadżer globalnych Permisji
Plugin pozwalający utworzyć grupy permisji dla graczy. Jeżeli nie użyjemy go na Proxy (Tylko na podserwerach), nikt nie będzie mógł używać pluginów z Proxy. Aby wszystkie serwery wczytywały te same Permisje, musimy podpiąc je pod Baze Danych. Kliknij [tutaj](https://luckperms.net/download) aby pobrać.

### Jak podpiąć Baze danych w LuckPermsie
Przejdź do katalogu głównego serwera, a następnie wyszukaj folder `Plugins`. Wejdź do katalogu Pluginu LuckPerms i otwórz plik `config.yml`.
Zlokalizuj ten fragment: i zacznij go edytować.
```
storage-method: MySQL #Do jakiej bazy danych Plugin będzie podpięty. (MySQL, MariaDB, PostgreSQL, MongoDB)

data:
  address: mysql.twojserwer.pl:3306 #Host Bazy Danych, zawsze musisz zapisać jako host:port_bazy
  database: xyz #Nazwa Bazy danych
  
  username: ROOT #Nazwa użytkownika
  password: 'HasloMaslo' #Haslo logowania bazy danych
  ```
  Sposób zapisywania `DB` oraz `SQLite` jest lokalny, nie można go użyc w tworzeniu sieci.
  
# SparkBungee - Kontrola działania serwera Proxy
**Spark** to **najlepszy** plugin na kontrlowanie kondycji serwera, Plugin pobierzesz [tutaj](https://spark.lucko.me/download). 

- **Profiler procesora:** Możesz zdiagnozować problemy z działaniem CPU

- **Kontrola pamięci:** Możesz kontrolować stan pamięci RAM

- **Raportowanie kondycji serwera:** Możesz monitorować ogólny stan kondycji serwera

### Permisje pluginu SparkBungee
- `spark.*` - nadaje wszystkie permisje.
- `spark.profiler` - nadaje możliwość sprawdzenia kondycji serwera na [tej](https://spark.me.lucko) stronie.
- `spark.tps` - nadaje możliwość sprawdzenia aktualnych TPSów serwera.
- `spark.ping` - nadaje możliwość sprawdzenia PINGu.
- `spark.healthreport` - nadaje możliwość sprawdzenia kondycji serwera na czacie.
- `spark.tickmonitor` - nadaje możwliosć sprawdzenia responsywnośći serwera.
- `spark.gc` `spark.gcmonitor` - nadaje możliwość sprawdzenia statsytyk GC.
- `spark.heapsummary` - nadaje możlwiosć sprawdzenia podsumowanych staytsyk.
- `spark.heapdump` - nadaje możliwość sprawdzenia Ticków serwera.
- `spark.activity` - nadaje możliwość sprawdzenia aktywnośći serwera i gracza.


# PlayerBalancer - Balansuj graczami pomiędzy serwerami!

Posiadasz pare lobby, a gracze są przenoszeni tylko na jedno? Chcesz dodac komendy typu /lobby? A może chcesz aby graczy po wyrzuceniu z podserwera nie byli wyrzucani z sieci? Dobrze trafiłeś! To wszytko pozwala plugin PlayerBalancer! Dodatkowo wspiera Pluginy na [Party](https://www.spigotmc.org/resources/party-and-friends-for-bungeecord-supports-clients-from-1-7-to-1-9.9531/) oraz [Znajomych](https://www.spigotmc.org/resources/ultimate-friends.3964/)! Plugin pobierzesz [tutaj!](https://www.spigotmc.org/resources/playerbalancer.55011/updates)
### Gracze mogą być przełączani pomiędzy serwerami za pomocą zasad:
  - `NONE` - Gracz zostanie przełączony do serwera z którym się łączył.
  - `RANDOM` - Losowy serwer.
  - `RANDOM_LOWEST` - Losowy serwer z najmniejszą ilością graczy.
  - `RANDOM_FILLER` - Losowy serwer z największą ilością osób, ale nie pełny.
  - `PROGRESSIVE` - Pierwszy serwer który nie jest pełny.
  - `PROGRESSIVE_LOWEST` - Pierwszy serwer z najmniejszą ilością osób.
  - `PROGRESSIVE_FILLER` - Pierwszy serwer z największą ilośćią osób, ale nie pełny.
  - `EXTERNAL` - Przezuca gracza według innego pluginu.

### Permisje pluginu Player Balancer
 - `playerbalancer.bypass` - gracz z tą permisją nie może byc przenoszony na inny serwer. Zalecamy ustawienie tej Permisji na `false`.

# BMsg - Globalne wiadomości prywatne, i więcej!
BMsg to plugin dodający wiadomośći prywatne, system zgłoszeń /helpop, tryb "detektywa", czat administarcji oraz Alertów na całe Proxy.

Tłumaczenie znajdziesz [tutaj]()

![HelPOP](https://i.imgur.com/u9ge3hL.png)

### Permisje pluginu BMsg

- `bmsg.command.msg` - dodaje możliwość wysyłania wiadomośći prywatntch.
- `bmsg.command.reply` - dodaje możliwość szybkiego odpowiadania na wiadomość `/r [text]`.
- `bmsg.command.staffchat` - dodaje możliwość wysyłania wiadomości na admin czat.
- `bmsg.command.socialspy` - dodaje możliwość widzenia wiadomości prywatnych innych graczy.   
- `bmsg.command.helpop` - dodaje możliwość wysyłania wiadomości Helpop.
- `bmsg.command.helpop.receive` - dodaje możliwość dostawamia wiadomości Helpop.
- `bmsg.command.togglemsg` - dodaje możliwość wyłączenia wiadomości prywatnych.
- `bmsg.command.broadcast` - dodaje możliwość wysyłania alertów na całą sieć. 
- `bmsg.command.info` - dodaje możliwość zobaczenia inforamcji o wszystkich komendach
