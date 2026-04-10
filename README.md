# LAB 5 - Navigation par Onglets (TabLayout) et Conversions

![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)

## À propos du projet
Ce projet représente le cinquième laboratoire de mon apprentissage en **Programmation Mobile : Android avec Java**. 

L'objectif de cette application est d'explorer la navigation horizontale (swipe) grâce à l'architecture **ViewPager2**. Le projet se présente sous la forme d'un utilitaire multi-outils, intégrant deux convertisseurs distincts séparés par des onglets dynamiques. Il met également l'accent sur la validation des entrées utilisateur et la sécurisation de l'application contre les plantages (crashs).

## Fonctionnalités
L'application est divisée en deux onglets principaux :
1. **Onglet Température :** Permet la conversion bidirectionnelle entre Celsius et Fahrenheit.
2. **Onglet Distance :** Permet la conversion bidirectionnelle entre Kilomètres et Miles.
3. **Sécurité et Validation :**
   - Empêche le calcul si le champ est vide (affichage d'un message `Toast`).
   - Bloque les erreurs de saisie (comme un point `.` isolé) pour éviter les crashs de l'application.
4. **Boîte de dialogue de confirmation :** L'interception du bouton "Retour" physique déclenche une fenêtre pop-up demandant à l'utilisateur de confirmer sa volonté de quitter l'application.


## Concepts techniques abordés
Ce laboratoire m'a permis de maîtriser les outils suivants :
* **ViewPager2 & TabLayout :** Mise en place d'une navigation par balayage horizontal fluide et synchronisation des onglets à l'aide de la classe `TabLayoutMediator`.
* **Conception UI Responsive :** Utilisation judicieuse de `android:layout_weight="1"` avec un `height="0dp"` pour s'assurer que le ViewPager occupe dynamiquement l'espace restant sans déborder de l'écran.
* **Gestion des Exceptions (Robustesse) :** Implémentation de blocs `try-catch` pour capturer les `NumberFormatException` lors de la conversion de chaînes de caractères (`String`) en nombres décimaux (`Double`).
* **Boîtes de Dialogue (AlertDialog) :** Utilisation de `AlertDialog.Builder` pour créer des interactions modales avec des boutons d'action positifs/négatifs.
* **Surcharge du cycle de vie :** Redéfinition de la méthode `onBackPressed()` pour altérer le comportement de navigation natif d'Android.

## Comment lancer le projet en local

1. Clonez ce dépôt sur votre machine locale :
   ```bash
   git clone [https://github.com/Sultan-zd/Lab5-ViewPager-Conversions.git](https://github.com/Sultan-zd/Lab5-ViewPager-Conversions.git)

2. Ouvrez Android Studio.

3. Sélectionnez File > Open et choisissez le dossier du projet cloné.

4. Laissez Gradle synchroniser les dépendances.

5. Cliquez sur le bouton Run (le triangle vert) pour lancer l'application sur un émulateur ou un appareil physique.
