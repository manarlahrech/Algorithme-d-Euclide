#include <stdio.h>

int main() {
    int a, b, r;  // Déclaration des variables pour les deux nombres et le reste

    // Demander à l'utilisateur de saisir le premier nombre
    printf("Veuillez entrer le premier nombre : ");
    scanf("%d", &a);  // Lire la valeur saisie et la stocker dans a

    // Demander à l'utilisateur de saisir le deuxième nombre
    printf("Veuillez entrer le deuxième nombre : ");
    scanf("%d", &b);  // Lire la valeur saisie et la stocker dans b

    printf("\nEtapes de calcul\n");

    // Boucle pour appliquer l'algorithme d'Euclide avec affichage des étapes intermédiaires
    while (b != 0) {
        r = a % b;   // Calculer le reste de la division de a par b
        printf("a = %d, b = %d, reste = %d\n", a, b, r);
        a = b;       // Mettre à jour a avec la valeur de b
        b = r;       // Mettre à jour b avec la valeur du reste
    }

    // Afficher le résultat final
    printf("\nLe PGCD est : %d\n", a);

    return 0;
}
