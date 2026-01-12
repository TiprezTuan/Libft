# libft

Ma première bibliothèque en C - Projet de l'école 42 Paris

## 📋 Description

**libft** est le premier projet du cursus de 42. L'objectif est de recoder certaines fonctions de la bibliothèque standard du C (`libc`), ainsi que d'autres fonctions utilitaires qui serviront tout au long du cursus.

Ce projet permet de mieux comprendre le fonctionnement de ces fonctions standard et d'acquérir une base solide en programmation C.

## 🎯 Objectifs pédagogiques

- Comprendre le fonctionnement interne des fonctions de la `libc`
- Manipuler les pointeurs, la mémoire et les chaînes de caractères
- Respecter la Norme de 42
- Créer une bibliothèque réutilisable pour les futurs projets

## 📚 Fonctions implémentées

### Partie 1 : Fonctions de la libc

#### Manipulation de caractères
- `ft_isalpha` - Vérifie si le caractère est alphabétique
- `ft_isdigit` - Vérifie si le caractère est un chiffre
- `ft_isalnum` - Vérifie si le caractère est alphanumérique
- `ft_isascii` - Vérifie si le caractère est ASCII
- `ft_isprint` - Vérifie si le caractère est imprimable
- `ft_toupper` - Convertit en majuscule
- `ft_tolower` - Convertit en minuscule

#### Manipulation de chaînes
- `ft_strlen` - Calcule la longueur d'une chaîne
- `ft_strchr` - Recherche un caractère dans une chaîne
- `ft_strrchr` - Recherche un caractère depuis la fin
- `ft_strncmp` - Compare deux chaînes (n caractères)
- `ft_strnstr` - Recherche une sous-chaîne
- `ft_strlcpy` - Copie une chaîne de manière sécurisée
- `ft_strlcat` - Concatène une chaîne de manière sécurisée

#### Gestion de la mémoire
- `ft_memset` - Remplit la mémoire avec une valeur
- `ft_bzero` - Met à zéro une zone mémoire
- `ft_memcpy` - Copie une zone mémoire
- `ft_memmove` - Copie une zone mémoire (avec chevauchement)
- `ft_memchr` - Recherche un caractère en mémoire
- `ft_memcmp` - Compare deux zones mémoires

#### Conversion et allocation
- `ft_atoi` - Convertit une chaîne en entier
- `ft_calloc` - Alloue et initialise la mémoire
- `ft_strdup` - Duplique une chaîne

### Partie 2 : Fonctions supplémentaires

- `ft_substr` - Extrait une sous-chaîne
- `ft_strjoin` - Concatène deux chaînes
- `ft_strtrim` - Supprime les caractères spécifiés aux extrémités
- `ft_split` - Découpe une chaîne selon un délimiteur
- `ft_itoa` - Convertit un entier en chaîne
- `ft_strmapi` - Applique une fonction à chaque caractère
- `ft_striteri` - Applique une fonction à chaque caractère (avec index)
- `ft_putchar_fd` - Écrit un caractère sur un fd
- `ft_putstr_fd` - Écrit une chaîne sur un fd
- `ft_putendl_fd` - Écrit une chaîne suivie d'un retour à la ligne
- `ft_putnbr_fd` - Écrit un nombre sur un fd

### Bonus : Manipulation de listes chaînées

- `ft_lstnew` - Crée un nouvel élément
- `ft_lstadd_front` - Ajoute un élément au début
- `ft_lstsize` - Compte le nombre d'éléments
- `ft_lstlast` - Retourne le dernier élément
- `ft_lstadd_back` - Ajoute un élément à la fin
- `ft_lstdelone` - Supprime un élément
- `ft_lstclear` - Supprime toute la liste
- `ft_lstiter` - Applique une fonction à chaque élément
- `ft_lstmap` - Applique une fonction et crée une nouvelle liste

## 🛠️ Compilation et utilisation

### Compilation

```bash
# Compiler la bibliothèque
make

# Compiler avec les bonus
make bonus

# Nettoyer les fichiers objets
make clean

# Nettoyer tous les fichiers générés
make fclean

# Recompiler complètement
make re
```

### Utilisation dans un projet

```c
#include "libft.h"

int main(void)
{
    char *str = ft_strdup("Hello, 42!");
    ft_putendl_fd(str, 1);
    free(str);
    return (0);
}
```

**Compilation avec libft :**
```bash
gcc -Wall -Wextra -Werror main.c -L. -lft -o program
```

## 📁 Structure du projet

```
libft/
├── Makefile
├── libft.h
├── ft_*.c          (fichiers sources)
└── README.md
```

## ⚙️ Makefile

Le Makefile contient les règles suivantes :
- `all` : Compile la bibliothèque
- `clean` : Supprime les fichiers objets
- `fclean` : Supprime les fichiers objets et la bibliothèque
- `re` : Recompile entièrement
- `bonus` : Compile avec les fonctions bonus

## ✅ Normes et contraintes

- Respect strict de la Norme de 42
- Aucune variable globale autorisée
- Utilisation de `Makefile` pour la compilation
- Gestion de la mémoire sans fuites (`valgrind`)
- Flags de compilation : `-Wall -Wextra -Werror`

## 🧪 Tests

Pour tester votre libft, vous pouvez utiliser :
- [francinette](https://github.com/xicodomingues/francinette)

## 📝 Notes

Ce projet est réalisé dans le cadre du cursus de 42 Paris. Il constitue la base pour de nombreux projets futurs et sera réutilisé tout au long du tronc commun.

## 👤 Auteur

Projet réalisé par ttiprez à 42 Paris

## 📜 Licence

Ce projet est réalisé à des fins éducatives dans le cadre du cursus de l'école 42.