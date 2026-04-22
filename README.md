# Projet-info-S2


#include "sauvegarde.h"
#include <stdio.h>
#include <string.h>

/*
Format du fichier texte (1 sauvegarde par ligne)
pseudo;niveau
ex: Alice;3
*/

void sauvegarderPartie(const char *pseudo, int niveau)
{
    FILE *f = fopen(FICHIER_SAUVEGARDE, "r");
    FILE *temp = fopen("temp.txt", "w");

    char p[MAX_PSEUDO];
    int n;
    int trouve = 0;

    if (temp == NULL) {
        printf("Erreur ouverture fichier temporaire\n");
        return;
    }

    // Si le fichier de sauvegarde existe déjà
    if (f != NULL) {
        while (fscanf(f, "%49[^;];%d\n", p, &n) == 2) {
            if (strcmp(p, pseudo) == 0) {
                /* Mise à jour de la sauvegarde */
                fprintf(temp, "%s;%d\n", pseudo, niveau);
                trouve = 1;
            } else {
                /* Recopie des autres sauvegardes */
                fprintf(temp, "%s;%d\n", p, n);
            }
        }
        fclose(f);
    }

    // Si le pseudo n'existait pas, on l'ajoute
    if (!trouve) {
        fprintf(temp, "%s;%d\n", pseudo, niveau);
    }

    fclose(temp);

    /* Remplacement sécurisé du fichier */
    remove(FICHIER_SAUVEGARDE);
    rename("temp.txt", FICHIER_SAUVEGARDE);
}

int chargerPartie(const char *pseudo, int *niveau)
{
    FILE *f = fopen(FICHIER_SAUVEGARDE, "r");
    char p[MAX_PSEUDO];
    int n;

    if (f == NULL)
        return 0; // aucune sauvegarde

    while (fscanf(f, "%49[^;];%d\n", p, &n) == 2) {
        if (strcmp(p, pseudo) == 0) {
            *niveau = n; //on reprend le dernier niveau auquel le joueur s'était arrêté
            fclose(f);
            return 1; // sauvegarde trouvée
        }
    }

    fclose(f);
    return 0; // sauvegarde non trouvée
}

int pseudoExiste(const char *pseudo)
{
    FILE *f = fopen(FICHIER_SAUVEGARDE, "r");
    char p[MAX_PSEUDO];
    int n;

    if (f == NULL)
        return 0;

    while (fscanf(f, "%49[^;];%d\n", p, &n) == 2) {
        if (strcmp(p, pseudo) == 0) {
            fclose(f);
            return 1; // pseudo trouvé
        }
    }
    fclose(f);
    return 0; //pseudo non trouvé
}
