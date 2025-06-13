# DDD + CQRS Strict Folder-Structure Architecture

---

## Vue d'ensemble du Projet

Cette architecture suit une **approche stricte DDD (Domain-Driven Design)** combinée au **pattern CQRS (Command Query Responsibility Segregation)**, tout en organisant le projet **par fonctionnalités (features)**.

Chaque **feature** est autonome et contient ses propres couches **Domain**, **Application**, **Infrastructure** et **Presentation**.  
Ce découpage favorise la **clarté**, la **scalabilité**, et un **alignement fort avec le métier**.


![Architecture DDD](https://shiftasia.com/community/content/images/size/w2000/2023/12/domain-driven-design-clean-architecture.png)

---


## Particularités


1.  **Structuration stricte par Feature**:
    * **Domain** : contient les Entités, Value Objects, Aggregats, Services, Événements, et Interfaces des Repositories.
    * **Application** : logique métier orientée cas d’usage (services), manipulation des DTO, séparation Command/Query.
    * **Infrastructure** : implémentation concrète (repositories, adaptateurs externes).
    * **Presentation ** : expose l’application via des contrôleurs, vues ou endpoints API/UI.

2.  **Intégration du Pattern CQRS**:
    * Séparation claire entre Command et Query dans chaque couche (Repository, Service, Controller, etc.).
    * Améliore la performance, la testabilité, et le découplage lecture/écriture.
