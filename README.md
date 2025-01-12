# Huge Framework – Messenger Stored Procedures

## Übersicht
Dieses Projekt erweitert das Huge Framework um eine Messenger-Anwendung, bei der alle SQL-Abfragen durch Stored Procedures ersetzt wurden, um die Sicherheit und Wartbarkeit zu verbessern:
- Nachrichtenarchiv in der Datenbank
- Verwendung von Stored Procedures zur Optimierung der Datenbankabfragen.

## Features
- **Stored Procedures:** Ersetzt direkte SQL-Befehle durch Stored Procedures.
- **Nachrichtenarchiv:** Alle Nachrichten werden in der Datenbank gespeichert und können eingesehen werden.

## Technologien
![PHP](https://img.shields.io/badge/PHP-8.1%2B-blue?logo=php&logoColor=white)
![Huge Framework](https://img.shields.io/badge/Huge_Framework-1.0-brightgreen)
![HTML](https://img.shields.io/badge/HTML-5-orange?logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-3-blue?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-yellow?logo=javascript&logoColor=white)
![PHPStorm](https://img.shields.io/badge/IDE-PHPStorm-purple?logo=phpstorm&logoColor=white)
![MySQL](https://img.shields.io/badge/Database-MySQL-lightblue?logo=mysql&logoColor=white)

⚠️**Hinweis:** In diesem Repository wurde ausschließlich der `application`-Ordner hochgeladen. Dies geschieht, um den Datenschutz zu gewährleisten und keine sensiblen Daten wie Serverkonfigurationen oder Zugangsdaten öffentlich bereitzustellen. Dateien wie `config.php` und andere Konfigurationsdateien, die möglicherweise sensible Informationen enthalten, wurden absichtlich nicht hochgeladen.

## Schritte zur Implementierung

1. **Erstellung von Stored Procedures:**
   - Integration der folgenden Stored Procedures in die bestehende Datenbankstruktur:
     - `getMessagesByUser`: Gibt alle Nachrichten zwischen zwei Benutzern zurück.
     - `sendMessage`: Speichert eine neue Nachricht.
     - `getUnreadMessagesCount`: Zählt die ungelesenen Nachrichten eines Benutzers.
     - `markMessagesAsRead`: Markiert alle ungelesenen Nachrichten in einem Gespräch als gelesen.

2. **Anpassung der MessengerModel.php:**
   - Ersetzen direkter SQL-Befehle durch `CALL`-Statements, die die oben genannten Stored Procedures aufrufen.

3. **Frontend-Integration:**
   - Sicherstellen, dass die Benutzeroberfläche mit den Änderungen kompatibel bleibt.

## Screenshots

### **Vorher-Nachher Vergleich der Code-Integration**

#### **Abfrage von Benutzerdaten (Namen des Absenders und Empfängers)**
Vorher:
![Vorher](./path_to_images/abfrage_benutzerdaten_namen_des_absenders_und_empfaengers.png)
Nachher:
![Nachher](./path_to_images/abfrage_benutzerdaten_namen_des_absenders_und_empfaengers_new.png)

#### **Zählen ungelesener Nachrichten**
Vorher:
![Vorher](./path_to_images/count_unread_messages.png)
Nachher:
![Nachher](./path_to_images/count_unread_messages_new.png)

#### **Stored Procedures in der Datenbank**
![Stored Procedures](./path_to_images/huge_db_stored_procedures.png)

#### **Nachricht als gelesen markieren**
Vorher:
![Vorher](./path_to_images/mark_messages_as_read.png)
Nachher:
![Nachher](./path_to_images/mark_messages_as_read_new.png)

#### **Neue Nachricht in der Tabelle speichern**
Vorher:
![Vorher](./path_to_images/neue_message_in_tabelle.png)
Nachher:
![Nachher](./path_to_images/neue_message_in_tabelle_new.png)

## Code-Referenzen

- [Messenger Controller](./path_to_repository/application/controller/MessengerController.php)
- [Model](./path_to_repository/application/model/MessengerModel.php)
- [View Messenger Index](./path_to_repository/application/view/messenger/index.php)

## Installation

Klone dieses Repository:

```bash
git clone https://github.com/your_repository/HUGE-Framework-Ue9.git
```

