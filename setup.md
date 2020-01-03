# Setup

[[toc]]

::: warning
Deze setup guide is alleen geldig voor MinetopiaSDB v2.0 of hoger!
:::

## Dependencies

| Serverversie    | WorldEdit                                                                    | WorldGuard                                                                    | Essentials                                                                              | Vault                                                                    | Citizens (optioneel!)                                      |
| :-------------- | :--------------------------------------------------------------------------- | :---------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------- | :----------------------------------------------------------------------- | :--------------------------------------------------------- |
| 1.9.4           | [Download](https://dev.bukkit.org/projects/worldedit/files/956525/download)  | [Download](https://dev.bukkit.org/projects/worldguard/files/956770/download)  | [Download](https://www.spigotmc.org/resources/essentialsx.9089/download?version=286847) | [Download](https://dev.bukkit.org/projects/vault/files/894359/download)  | [Download](https://ci.citizensnpcs.co/job/citizens2/1371/) |
| 1.10.2          | [Download](https://dev.bukkit.org/projects/worldedit/files/2597538/download) | [Download](https://dev.bukkit.org/projects/worldguard/files/956770/download)  | [Download](https://www.spigotmc.org/resources/essentialsx.9089/download?version=286847) | [Download](https://dev.bukkit.org/projects/vault/files/894359/download)  | [Download](https://ci.citizensnpcs.co/job/Citizens2/1552/) |
| 1.11.2          | [Download](https://dev.bukkit.org/projects/worldedit/files/2597538/download) | [Download](https://dev.bukkit.org/projects/worldguard/files/956770/download)  | [Download](https://www.spigotmc.org/resources/essentialsx.9089/download?version=286847) | [Download](https://dev.bukkit.org/projects/vault/files/894359/download)  | [Download](https://ci.citizensnpcs.co/job/Citizens2/1552/) |
| 1.12.2          | [Download](https://dev.bukkit.org/projects/worldedit/files/2597538/download) | [Download](https://dev.bukkit.org/projects/worldguard/files/2610618/download) | [Download](https://www.spigotmc.org/resources/essentialsx.9089/download?version=286847) | [Download](https://dev.bukkit.org/projects/vault/files/894359/download)  | [Download](https://ci.citizensnpcs.co/job/citizens2/1552/) |
| 1.13.2          | [Download](https://dev.bukkit.org/projects/worldedit/files/2760373/download) | [Download](https://dev.bukkit.org/projects/worldguard/files/2723606/download) | [Download](https://www.spigotmc.org/resources/essentialsx.9089/download?version=286847) | [Download](https://dev.bukkit.org/projects/vault/files/2704903/download) | [Download](https://ci.citizensnpcs.co/job/citizens2/1687/) |
| 1.14.4          | [Download](https://dev.bukkit.org/projects/worldedit/files/2760373/download) | [Download](https://dev.bukkit.org/projects/worldguard/files/2831137/download) | [Download](https://www.spigotmc.org/resources/essentialsx.9089/download?version=286847) | [Download](https://dev.bukkit.org/projects/vault/files/2704903/download) | [Download](https://ci.citizensnpcs.co/job/citizens2/1752/) |

## Hoe moet ik beginnen?

Heel makkelijk, je downloadt de goede versie van alle dependencies (en natuurlijk MinetopiaSDB zelf) en zet deze in jouw ``plugins`` mapje. Als je dit hebt gedaan, kun je jouw server opstarten. Als alles lijkt te werken kun je een wereld toevoegen met /mtworld add \<Wereld\> en kun je echt van start met jouw Minetopia server!

## Database setup

::: tip
Wil je MinetopiaSDB met meerdere servers via Bungeecord gebruiken? Kijk dan even op [deze](./bungeecord.md) pagina.
:::


Een van de leukste nieuwe features aan MinetopiaSDB v2 is de ondersteuning voor MySQL databases. Het is nu mogelijk om data op te slaan in een database en op die manier jouw data in meerdere servers te gebruiken (en op die manier jouw spelers ook over verschillende servers te verspreiden.) 

Het is niet verplicht om een database in te stellen, als je niets instelt maak je automatisch gebruik van een lokale SQLite database. De standaard MySQL instellingen zien er zo uit:
```yml
MySQL:
  Enabled: false
  Username: root
  Password: password
  Database: Minetopia
  IP: localhost
  Port: 3306
```
Om gebruik te maken van MySQL moet je ``Enabled:`` op true zetten waarna je jouw MySQL inloggegevens in kan voeren bij de andere velden.



## Data migratie

Het opslaan van data is in de v2 update van MinetopiaSDB een stuk efficiënter geworden. Dit betekent helaas ook dat de oude v1 data niet zomaar overgezet kan worden. Hiervoor moet de data omgezet worden. Om dit probleem op te lossen hebben we een datamigratie dienst gelanceerd. Met deze dienst is het mogelijk om tegen een kleine betaling jouw data te laten converteren naar de v2 data waardoor je alle spelerdata behoudt.


### Waarom kost dit geld? Ik dacht dat MinetopiaSDB gratis was?

MinetopiaSDB is en blijft gratis. Het migreren van data is immers vrijwillig. Je kunt prima door gaan met jouw server zonder data om te zetten, alhoewel dit zal betekenen dat jouw spelers weer vanaf 0 moeten beginnen.


### Ik wil mijn data laten migreren naar v2 data, hoe moet dat?

Dat kan door een emailtje te sturen naar [datamigratie@minetopiasdb.nl](mailto:datamigratie@minetopiasdb.nl).

| Spelersaantal   | Prijs   |
| --------------- | ------- |
| < 100           | Gratis* |
| < 2.000         | € 2     |
| < 10.000        | € 4     |
| > 10.000        | € 6     |

\* = alleen wanneer jouw server niet commercieel is en geen webshop heeft.