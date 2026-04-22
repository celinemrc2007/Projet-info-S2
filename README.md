#include <stdio.h>
#include <allegro.h>
#include "gestionGraphique.h"
void initialisation_allegro();

#DEFINE LARGEUR_ECRAN 1200 
#DEFINE HAUTEUR_ECRAN 800

#include <stdio.h>
#include <allegro.h>
void initialisation_allegro();

// Tableaux de sprites
// Pas de sprites bulles aplaties finalement pour faire un effet plus fluide lors du rebond
BITMAP *images[125];

void chargerSprites () {
		 image[1]=load_bitmap("../lara_debout_arme1.png",NULL);
		 image[2]=load_bitmap("../lara_court_a_gauche_arme1_1.png",NULL);
		 image[3]=load_bitmap("../lara_court_a_gauche_arme1_2.png",NULL);
		 image[4]=load_bitmap("../lara_court_a_gauche_arme1_3.png",NULL);
		 image[5]=load_bitmap("../lara_court_a_gauche_arme1_4.png",NULL);
		 image[6]=load_bitmap("../lara_court_a_droite_arme1_1.png",NULL);
		 image[7]=load_bitmap("../lara_court_a_droite_arme1_2.png",NULL);
		 image[8]=load_bitmap("../lara_court_a_droite_arme1_3.png",NULL);
		 image[9]=load_bitmap("../lara_court_a_droite_arme1_4.png",NULL);
		 image[10]=load_bitmap("../lara_tir_arme1_1.png",NULL);
		 image[11]=load_bitmap("../lara_tir_arme1_2.png",NULL);
		 image[12]=load_bitmap("../lara_tir_arme1_3.png",NULL);
		 image[13]=load_bitmap("../lara_debout_arme2.png",NULL);
		 image[14]=load_bitmap("../lara_court_a_gauche_arme2_1.png",NULL);
		 image[15]=load_bitmap("../lara_court_a_gauche_arme2_2.png",NULL);
		 image[16]=load_bitmap("../lara_court_a_gauche_arme2_3.png",NULL);
		 image[17]=load_bitmap("../lara_court_a_gauche_arme2_4.png",NULL);
		 image[18]=load_bitmap("../lara_court_a_droite_arme2_1.png",NULL);
		 image[19]=load_bitmap("../lara_court_a_droite_arme2_2.png",NULL);
		 image[20]=load_bitmap("../lara_court_a_droite_arme2_3.png",NULL);
		 image[21]=load_bitmap("../lara_court_a_droite_arme2_4.png",NULL);
		 image[22]=load_bitmap("../lara_tir_arme2_1.png",NULL);
		 image[23]=load_bitmap("../lara_tir_arme2_2.png",NULL);
		 image[24]=load_bitmap("../lara_tir_arme2_3.png",NULL);
		 image[25]=load_bitmap("../lara_debout_arme3.png",NULL);
		 image[26]=load_bitmap("../lara_court_a_gauche_arme3_1.png",NULL);
		 image[27]=load_bitmap("../lara_court_a_gauche_arme3_2.png",NULL);
		 image[28]=load_bitmap("../lara_court_a_gauche_arme3_3.png",NULL);
		 image[29]=load_bitmap("../lara_court_a_gauche_arme3_4.png",NULL);
		 image[30]=load_bitmap("../lara_court_a_droite_arme3_1.png",NULL);
		 image[31]=load_bitmap("../lara_court_a_droite_arme3_2.png",NULL);
		 image[32]=load_bitmap("../lara_court_a_droite_arme3_3.png",NULL);
		 image[33]=load_bitmap("../lara_court_a_droite_arme3_4.png",NULL);
		 image[34]=load_bitmap("../lara_tir_arme3_1.png",NULL);
		 image[35]=load_bitmap("../lara_tir_arme3_2.png",NULL);
		 image[36]=load_bitmap("../lara_tir_arme3_3.png",NULL);
		 image[37]=load_bitmap("../lara_debout_arme4.png",NULL);
		 image[38]=load_bitmap("../lara_court_a_gauche_arme4_1.png",NULL);
		 image[39]=load_bitmap("../lara_court_a_gauche_arme4_2.png",NULL);
		 image[40]=load_bitmap("../lara_court_a_gauche_arme4_3.png",NULL);
		 image[41]=load_bitmap("../lara_court_a_gauche_arme4_4.png",NULL);
		 image[42]=load_bitmap("../lara_court_a_droite_arme4_1.png",NULL);
		 image[43]=load_bitmap("../lara_court_a_droite_arme4_2.png",NULL);
		 image[44]=load_bitmap("../lara_court_a_droite_arme4_3.png",NULL);
		 image[45]=load_bitmap("../lara_court_a_droite_arme4_4.png",NULL);
		 image[46]=load_bitmap("../lara_tir_arme4_1.png",NULL);
		 image[47]=load_bitmap("../lara_tir_arme4_2.png",NULL);
		 image[48]=load_bitmap("../lara_tir_arme4_3.png",NULL);
		 image[49]=load_bitmap("../lara_debout_bazuka.png",NULL);
		 image[50]=load_bitmap("../lara_court_a_gauche_bazuka_1.png",NULL);
		 image[51]=load_bitmap("../lara_court_a_gauche_bazuka_2.png",NULL);
		 image[52]=load_bitmap("../lara_court_a_gauche_bazuka_3.png",NULL);
		 image[53]=load_bitmap("../lara_court_a_gauche_bazuka_4.png",NULL);
		 image[54]=load_bitmap("../lara_court_a_droite_bazuka_1.png",NULL);
		 image[55]=load_bitmap("../lara_court_a_droite_bazuka_2.png",NULL);
		 image[56]=load_bitmap("../lara_court_a_droite_bazuka_3.png",NULL);
		 image[57]=load_bitmap("../lara_court_a_droite_bazuka_4.png",NULL);
		 image[58]=load_bitmap("../lara_tir_bazuka_1.png",NULL);
		 image[59]=load_bitmap("../lara_tir_bazuka_2.png",NULL);
		 image[60]=load_bitmap("../lara_tir_bazuka_3.png",NULL);
		 image[61]=load_bitmap("../lara_perd_1.png",NULL);
		 image[62]=load_bitmap("../lara_perd_2.png",NULL);
		 image[63]=load_bitmap("../lara_perd_3.png",NULL);
		 image[64]=load_bitmap("../lara_perd_4.png",NULL);
		 image[65]=load_bitmap("../lara_perd_5.png",NULL);
		 image[66]=load_bitmap("../lara_perd_6.png",NULL);
		 image[67]=load_bitmap("../lara_gagne_1.png",NULL);
		 image[68]=load_bitmap("../lara_gagne_2.png",NULL);
		 image[69]=load_bitmap("../lara_gagne_3.png",NULL);
		 image[70]=load_bitmap("../lara_gagne_4.png",NULL);
		 image[71]=load_bitmap("../lara_gagne_5.png",NULL);
		 image[72]=load_bitmap("../lara_gagne_6.png",NULL);
		 image[73]=load_bitmap("../lara_gagne_7.png",NULL);
    	 image[74]=load_bitmap("../arme2.png",NULL);
    	 image[75]=load_bitmap("../arme3.png",NULL);
    	 image[76]=load_bitmap("../arme4.png",NULL);
    	 image[77]=load_bitmap("../bazuka.png",NULL);
    	 image[78]=load_bitmap("../balle.png",NULL);
    	 image[79]=load_bitmap("../bombe.png",NULL);
    	 image[80]=load_bitmap("../obstacle_petit.png",NULL);
    	 image[81]=load_bitmap("../obstacle_grand.png",NULL);
    	 image[82]=load_bitmap("../bulle_petite_pleine.png",NULL);
    	 image[83]=load_bitmap("../bulle_moyenne_pleine.png",NULL);
    	 image[84]=load_bitmap("../bulle_grande_pleine.png",NULL);
    	 image[85]=load_bitmap("../boss_mouvement_ailes_1.png",NULL);
    	 image[86]=load_bitmap("../boss_mouvement_ailes_2.png",NULL);
    	 image[87]=load_bitmap("../boss_mouvement_ailes_3.png",NULL);
    	 image[88]=load_bitmap("../boss_mouvement_ailes_4.png",NULL);
    	 image[89]=load_bitmap("../boss_mouvement_ailes_5.png",NULL);
    	 image[90]=load_bitmap("../boss_mouvement_ailes_6.png",NULL);
    	 image[91]=load_bitmap("../boss_perd_1.png",NULL);
    	 image[92]=load_bitmap("../boss_perd_2.png",NULL);
    	 image[93]=load_bitmap("../boss_perd_3.png",NULL);
    	 image[94]=load_bitmap("../boss_perd_4.png",NULL);
    	 image[95]=load_bitmap("../boule_de_feu_petite_pleine.png",NULL);
    	 image[96]=load_bitmap("../boule_de_feu_petite_aplatie.png",NULL);
    	 image[97]=load_bitmap("../boule_de_feu_moyenne_pleine.png",NULL);
    	 image[98]=load_bitmap("../boule_de_feu_moyenne_aplatie.png",NULL);
    	 image[99]=load_bitmap("../boule_de_feu_grande_pleine.png",NULL);
    	 image[100]=load_bitmap("../boule_de_feu_grande_aplatie.png",NULL);
}

//Pour afficher un sprite, nous appelons cette fct avec le numéro du sprite à afficher et sa position passé en paramètre.
void afficherSprite (float x, float y, int numero_sprite) {
	BITMAP *image = images[numero_sprite];
	blit(image,screen,0,0, (int)(x - image->w / 2), (int)(y - image->h / 2), image->w, image->h);
}
