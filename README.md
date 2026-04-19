#include <stdio.h>
#include <stdlib.h>
#include <windows.h>
#include <time.h>
#include <conio.h>

#include "gestionGraphique.h"
#include "gestionNiveau.h"
#include "logiqueJeu.h"
#include "sauvegarde.h"



/* ================= VARIABLES GLOBALES ================= */

int niveau = 1;                 // niveau courant
char pseudo[MAX_PSEUDO];

/* ================= PERMET DE PASSER LE PARAMETRE NIVEAU A CERTAINES SOUS-PROGRAMMES ================= */

int recupererNiveau() {
    return niveau;
}

/* ================= LANCEMENT NIVEAU ================= */

void lancerNiveau() {
    system("cls");
    copie_contrat = compteurs_contrat;

    /* Initialisation du contrat selon le niveau */
    for (int i = 1; i <= 5; i++)
        compteurs_contrat[i] = 0;

    switch (niveau) {
        case 1:
            temps_restant = 120; // 2 min
            bulle->objet = rand () % 2;
            break;

        case 2:
            temps_restant = 105; // 1 min 45
            bulle->objet = rand () % 3;
            break;

        case 3:
            temps_restant = 90; // 1 min 30
            bulle->objet = rand () % 5;
            break;
        case 4:
            temps_restant = 75; // 1 min 15
            bulle->objet = rand () % 6;
            break;

          case 5:
            temps_restant = 60; // 1 min
            bulle->objet = rand () % 9;
            break;
    }

    afficherNumeroNiveau(niveau);
    int resultat_jeu = jeu();
    if (resultat_jeu==true) {
        if (niveau != 4) {
            gererVictoireNiveau ();
        } else {
          jeu();
          gererBoss();  
        }  
    } else {
        gererEchecNiveau();
    }
}

/* ================= FIN NIVEAU APRES ANIMATION ================= */
void finNiveau {
    system("cls");
    int choix;
    text_color(FOREGROUND_RED | FOREGROUND_GREEN | FOREGROUND_BLUE);
    printf("\nQue souhaites-tu faire ?\n");
    printf("1. Continuer\n");
    printf("2. Sauvegarder et revenir au menu\n");
    printf("3. Sauvegarder et quitter le jeu\n");
    printf("4. Quitter le jeu sans sauvegarder\n");
    printf("Votre choix : ");
    scanf("%d", &choix);
    
    switch(choix) {
        case 1:
            lancerNiveau();
            break;

        case 2:
            sauvegarderPartie();
            menu();
            break;

        case 3:
            sauvegarderPartie();
            exit(0);
            break;
        case 4:
            exit(0)
            break;
    }
}

/* ================= VICTOIRE NIVEAU ================= */

void gererVictoireNiveau() {
    if (niveau == 5) {
        gererVictoirePartie();
    } else {
        niveau++;
        afficherVictoireNiveau();
        finNiveau();
    }
}

/* ================= ECHEC NIVEAU ================= */

void gererEchecNiveau() {
        afficherEchecNiveau();
        finNiveau();
}

/* ================= VICTOIRE PARTIE ================= */

void gererVictoirePartie() {
    afficherVictoirePartie();
    menu();
}

void gererBoss (Boss *boss, Joueur *joueur) {
    while (boss->nb_tirs_recus == (boss->nb_tirs_recus)++) {
        Bulle *ajouterBulle (Bulle **tete, Bulle *nouveau);
    }
        // à ajouter : si collision entre le joueur et le boss, appeler gererEchecNiveau
    int direction = rand() % 4; 

    switch(direction) {
        case 0: // à droite
            boss->position.x += 10;
            break;

        case 1: // à gauche
            boss->position.x -= 10;
            break;

        case 2: // en bas
            boss->position.y += 10;
            break;

        case 3: // en haut
            boss->position.y -= 10;
            break;
    }
}

void bonusBouclier () {

}

void malusMultiplication () {
    
}
