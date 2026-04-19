#include <allegro.h>
#include <time.h>
void initialisation_allegro();

void afficherSprite (float x, float y, int numero_sprite) {
	switch (numero_sprite) {
	case 1 :
		 image=load_bitmap("../lara_debout_arme1.bmp",NULL);
		 break;
	case 2 :
		 image=load_bitmap("../lara_court_a_gauche_arme1_1.bmp",NULL);
		 break;
	case 3 :
		 image=load_bitmap("../lara_court_a_gauche_arme1_2.bmp",NULL);
		 break;
	case 4 :
		 image=load_bitmap("../lara_court_a_gauche_arme1_3.bmp",NULL);
		 break;
	case 5 :
		 image=load_bitmap("../lara_court_a_gauche_arme1_4.bmp",NULL);
		 break;
	case 6 :
		 image=load_bitmap("../lara_court_a_droite_arme1_1.bmp",NULL);
		 break;
	case 7 :
		 image=load_bitmap("../lara_court_a_droite_arme1_2.bmp",NULL);
		 break;
	case 8 :
		 image=load_bitmap("../lara_court_a_droite_arme1_3.bmp",NULL);
		 break;
	case 9 :
		 image=load_bitmap("../lara_court_a_droite_arme1_4.bmp",NULL);
		 break;
	case 10 :
		 image=load_bitmap("../lara_tir_arme1_1.bmp",NULL);
		 break;	
	case 11 :
		 image=load_bitmap("../lara_tir_arme1_2.bmp",NULL);
		 break;	
	case 12 :
		 image=load_bitmap("../lara_tir_arme1_3.bmp",NULL);
		 break;	
	case 13 :
		 image=load_bitmap("../lara_debout_arme2.bmp",NULL);
		 break;
	case 14 :
		 image=load_bitmap("../lara_court_a_gauche_arme2_1.bmp",NULL);
		 break;
	case 15 :
		 image=load_bitmap("../lara_court_a_gauche_arme2_2.bmp",NULL);
		 break;
	case 16 :
		 image=load_bitmap("../lara_court_a_gauche_arme2_3.bmp",NULL);
		 break;
	case 17 :
		 image=load_bitmap("../lara_court_a_gauche_arme2_4.bmp",NULL);
		 break;
	case 18 :
		 image=load_bitmap("../lara_court_a_droite_arme2_1.bmp",NULL);
		 break;
	case 19 :
		 image=load_bitmap("../lara_court_a_droite_arme2_2.bmp",NULL);
		 break;
	case 20 :
		 image=load_bitmap("../lara_court_a_droite_arme2_3.bmp",NULL);
		 break;
	case 21 :
		 image=load_bitmap("../lara_court_a_droite_arme2_4.bmp",NULL);
		 break; 
	case 22 :
		 image=load_bitmap("../lara_tir_arme2_1.bmp",NULL);
		 break;	
	case 23 :
		 image=load_bitmap("../lara_tir_arme2_2.bmp",NULL);
		 break;	
	case 24 :
		 image=load_bitmap("../lara_tir_arme2_3.bmp",NULL);
		 break;	
	case 25 :
		 image=load_bitmap("../lara_debout_arme3.bmp",NULL);
		 break;
	case 26 :
		 image=load_bitmap("../lara_court_a_gauche_arme3_1.bmp",NULL);
		 break;
	case 27 :
		 image=load_bitmap("../lara_court_a_gauche_arme3_2.bmp",NULL);
		 break;
	case 28 :
		 image=load_bitmap("../lara_court_a_gauche_arme3_3.bmp",NULL);
		 break;
	case 29 :
		 image=load_bitmap("../lara_court_a_gauche_arme3_4.bmp",NULL);
		 break;
	case 30 :
		 image=load_bitmap("../lara_court_a_droite_arme3_1.bmp",NULL);
		 break;
	case 31 :
		 image=load_bitmap("../lara_court_a_droite_arme3_2.bmp",NULL);
		 break;
	case 32 :
		 image=load_bitmap("../lara_court_a_droite_arme3_3.bmp",NULL);
		 break;
	case 33 :
		 image=load_bitmap("../lara_court_a_droite_arme3_4.bmp",NULL);
		 break; 
	case 34 :
		 image=load_bitmap("../lara_tir_arme3_1.bmp",NULL);
		 break;	
	case 35 :
		 image=load_bitmap("../lara_tir_arme3_2.bmp",NULL);
		 break;	
	case 36 :
		 image=load_bitmap("../lara_tir_arme3_3.bmp",NULL);
		 break;	
	case 37 :
		 image=load_bitmap("../lara_debout_arme4.bmp",NULL);
		 break;
	case 38 :
		 image=load_bitmap("../lara_court_a_gauche_arme4_1.bmp",NULL);
		 break;
	case 39 :
		 image=load_bitmap("../lara_court_a_gauche_arme4_2.bmp",NULL);
		 break;
	case 40 :
		 image=load_bitmap("../lara_court_a_gauche_arme4_3.bmp",NULL);
		 break;
	case 41 :
		 image=load_bitmap("../lara_court_a_gauche_arme4_4.bmp",NULL);
		 break;
	case 42 :
		 image=load_bitmap("../lara_court_a_droite_arme4_1.bmp",NULL);
		 break;
	case 43 :
		 image=load_bitmap("../lara_court_a_droite_arme4_2.bmp",NULL);
		 break;
	case 44 :
		 image=load_bitmap("../lara_court_a_droite_arme4_3.bmp",NULL);
		 break;
	case 45 :
		 image=load_bitmap("../lara_court_a_droite_arme4_4.bmp",NULL);
		 break; 
	case 46 :
		 image=load_bitmap("../lara_tir_arme4_1.bmp",NULL);
		 break;	
	case 47 :
		 image=load_bitmap("../lara_tir_arme4_2.bmp",NULL);
		 break;	
	case 48 :
		 image=load_bitmap("../lara_tir_arme4_3.bmp",NULL);
		 break;	
	case 49 :
		 image=load_bitmap("../lara_debout_bazuka.bmp",NULL);
		 break;
	case 50 :
		 image=load_bitmap("../lara_court_a_gauche_bazuka_1.bmp",NULL);
		 break;
	case 51 :
		 image=load_bitmap("../lara_court_a_gauche_bazuka_2.bmp",NULL);
		 break;
	case 52 :
		 image=load_bitmap("../lara_court_a_gauche_bazuka_3.bmp",NULL);
		 break;
	case 53 :
		 image=load_bitmap("../lara_court_a_gauche_bazuka_4.bmp",NULL);
		 break;
	case 54 :
		 image=load_bitmap("../lara_court_a_droite_bazuka_1.bmp",NULL);
		 break;
	case 55 :
		 image=load_bitmap("../lara_court_a_droite_bazuka_2.bmp",NULL);
		 break;
	case 56 :
		 image=load_bitmap("../lara_court_a_droite_bazuka_3.bmp",NULL);
		 break;
	case 57 :
		 image=load_bitmap("../lara_court_a_droite_bazuka_4.bmp",NULL);
		 break; 
	case 58 :
		 image=load_bitmap("../lara_tir_bazuka_1.bmp",NULL);
		 break;	
	case 59 :
		 image=load_bitmap("../lara_tir_bazuka_2.bmp",NULL);
		 break;	
	case 60 :
		 image=load_bitmap("../lara_tir_bazuka_3.bmp",NULL);
		 break;	
	case 61 :
		 image=load_bitmap("../lara_perd_1.bmp",NULL);
		 break;
	case 62 :
		 image=load_bitmap("../lara_perd_2.bmp",NULL);
		 break;
	case 63 :
		 image=load_bitmap("../lara_perd_3.bmp",NULL);
		 break;
	case 64 :
		 image=load_bitmap("../lara_perd_4.bmp",NULL);
		 break;
	case 65 :
		 image=load_bitmap("../lara_perd_5.bmp",NULL);
		 break;
	case 66 :
		 image=load_bitmap("../lara_perd_6.bmp",NULL);
		 break;
	case 67 :
		 image=load_bitmap("../lara_gagne_1.bmp",NULL);
		 break;
	case 68 :
		 image=load_bitmap("../lara_gagne_2.bmp",NULL);
		 break;
	case 69 :
		 image=load_bitmap("../lara_gagne_3.bmp",NULL);
		 break;
	case 70 :
		 image=load_bitmap("../lara_gagne_4.bmp",NULL);
		 break;
	case 71 :
		 image=load_bitmap("../lara_gagne_5.bmp",NULL);
		 break;
	case 72 :
		 image=load_bitmap("../lara_gagne_6.bmp",NULL);
		 break;
	case 73 :
		 image=load_bitmap("../lara_gagne_7.bmp",NULL);
		 break;
    case 75 :
    	 image=load_bitmap("../arme2.bmp",NULL);
    	 break;
    case 76 :
    	 image=load_bitmap("../arme3.bmp",NULL);
    	 break;
    case 77 :
    	 image=load_bitmap("../arme4.bmp",NULL);
    	 break;
    case 78 :
    	 image=load_bitmap("../bazuka.bmp",NULL);
    	 break;
    case 79 :
    	 image=load_bitmap("../balle.bmp",NULL);
    	 break;
    case 80 :
    	 image=load_bitmap("../bombe.bmp",NULL);
    	 break;
    case 81 :
    	 image=load_bitmap("../obstacle_petit.bmp",NULL);
    	 break;	
    case 82 :
    	 image=load_bitmap("../obstacle_grand.bmp",NULL);
    	 break;	
    case 83 :
    	 image=load_bitmap("../bulle_petite_pleine.bmp",NULL);
    	 break;
    case 84 :
    	 image=load_bitmap("../bulle_petite_aplatie.bmp",NULL);
    	 break;
    case 85 :
    	 image=load_bitmap("../bulle_moyenne_pleine.bmp",NULL);
    	 break;
    case 86 :
    	 image=load_bitmap("../bulle_moyenne_aplatie.bmp",NULL);
    	 break;
    case 87 :
    	 image=load_bitmap("../bulle_grande_pleine.bmp",NULL);
    	 break;
    case 88 :
    	 image=load_bitmap("../bulle_grande_aplatie.bmp",NULL);
    	 break;
    case 89 :
    	 image=load_bitmap("../boss_mouvement_ailes_1.bmp",NULL);
    	 break;
    case 90 :
    	 image=load_bitmap("../boss_mouvement_ailes_2.bmp",NULL);
    	 break;
    case 91 :
    	 image=load_bitmap("../boss_mouvement_ailes_3.bmp",NULL);
    	 break;
    case 92 :
    	 image=load_bitmap("../boss_mouvement_ailes_4.bmp",NULL);
    	 break;
    case 93 :
    	 image=load_bitmap("../boss_mouvement_ailes_5.bmp",NULL);
    	 break;
     case 94 :
    	 image=load_bitmap("../boss_mouvement_ailes_6.bmp",NULL);
    	 break;
    case 95 :
    	 image=load_bitmap("../boss_perd_1.bmp",NULL);
    	 break;
    case 96 :
    	 image=load_bitmap("../boss_perd_2.bmp",NULL);
    	 break;
    case 97 :
    	 image=load_bitmap("../boss_perd_3.bmp",NULL);
    	 break;	  
    case 98 :
    	 image=load_bitmap("../boss_perd_4.bmp",NULL);
    	 break;
    case 99 :
    	 image=load_bitmap("../boule_de_feu_petite_pleine.bmp",NULL);
    	 break;
    case 100 :
    	 image=load_bitmap("../boule_de_feu_petite_aplatie.bmp",NULL);
    	 break;
    case 101 :
    	 image=load_bitmap("../boule_de_feu_moyenne_pleine.bmp",NULL);
    	 break;
    case 102 :
    	 image=load_bitmap("../boule_de_feu_moyenne_aplatie.bmp",NULL);
    	 break;
    case 103 :
    	 image=load_bitmap("../boule_de_feu_grande_pleine.bmp",NULL);
    	 break;
    case 104 :
    	 image=load_bitmap("../boule_de_feu_grande_aplatie.bmp",NULL);
    	 break;
	}

}
