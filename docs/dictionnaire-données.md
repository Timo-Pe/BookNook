# Dictionnaire de données

## BOOK (livre)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|book_identifier|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|Book's ID|
|isbn|VARCHAR(20)|NOT NULL|Book's ISBN|
|title|VARCHAR(255)|NOT NULL|Book's title|
|price|DOUBLE|NOT NULL, UNSIGNED|Book's price|
|picture|VARCHAR(255)||Book's cover|
|summary|VARCHAR(255)||Book's summary|
|editor|VARCHAR(255)|NOT NULL|Book's editor|
|nb_pages|INT|NOT NULL, UNSIGNED|Book's number of pages|
|format|VARCHAR(255)|NOT NULL|Book's format|
|status|INT|NOT NULL, UNSIGNED|Book's status - in or out of stock|

## AUTHOR (auteur)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|author_identifier|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|Author's ID|
|name|VARCHAR(255)|NOT NULL|Author's name|

## CATEGORY (categorie)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|category_identifier|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|Category's ID|
|name|VARCHAR(255)|NOT NULL|Category's name|

## REVIEW (avis)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|review_identifier|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|Review's ID|
|comment|VARCHAR(255)|NOT NULL|User comment in review|
|publicationDate|VARCHAR(255)|NOT NULL|Publication date of the review|
|rating|INT|NOT NULL, UNSIGNED|User rating to a book - from 1 to 5|

## USER (utilisateur)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|user_identifier|INT|PRIMARY KEY, NOT NULL, UNSIGNED, AUTO_INCREMENT|User's ID|
|name|VARCHAR(255)|NOT NULL|User's name|
|email|VARCHAR(255)|NOT NULL|User's email|
|password|VARCHAR(255)|NOT NULL|User's password|
|roles|LONGTEXT|NOT NULL|User's table of roles|
|address|VARCHAR(255)||User's address|

## RELATIONS BETWEEN ENTITIES (association entre les entités)

|Champ|Type|Spécificités|Description|
|-|-|-|-|
|book_author|ENTITY|FOREIGN KEY, NOT NULL|The book's author|
|book_category|ENTITY|FOREIGN KEY, NOT NULL|The book's category|
|book_review|ENTITY|FOREIGN KEY, NOT NULL|A book's review|
|review_user|ENTITY|FOREIGN KEY, NOT NULL|The user who wrote the review|
