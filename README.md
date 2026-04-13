typedef struct {

float  x; 
float y; 
float vitesse vx;
float vitesse vy;
float largeur; 
float hauteur;
bool actif;
} Position;

typedef struct bulle {
int rayon;
int objet;
struct bulle *suivant;
} Bulle;
