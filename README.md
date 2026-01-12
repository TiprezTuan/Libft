📑 Libft - @42Paris

<p align="center"> <img src="https://img.shields.io/badge/Score-125%2F100-success?style=for-the-badge&logo=42" alt="Score 125/100"> <img src="https://img.shields.io/badge/Language-C-blue?style=for-the-badge&logo=c" alt="Language C"> <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Status Completed"> </p>
📝 Présentation

La Libft est le premier projet du cursus de 42. L'objectif est de recoder un ensemble de fonctions de la bibliothèque C standard (libc) ainsi que d'autres fonctions utilitaires que nous pourrons réutiliser tout au long de notre cursus.

    "Ce projet vous apprend à comprendre en profondeur les fonctions de manipulation de mémoire et de chaînes de caractères en C."

🛠️ Sommaire

    Partie 1 : Fonctions de la Libc

    Partie 2 : Fonctions supplémentaires

    Partie Bonus : Manipulation de listes

    Installation & Utilisation

📂 Contenu du projet
Partie 1 : Fonctions de la Libc

Ces fonctions imitent le comportement des fonctions standards originales.
Caractères	Mémoire	Chaînes	Conversion
ft_isalpha	ft_memset	ft_strlen	ft_atoi
ft_isdigit	ft_bzero	ft_strlcpy	ft_toupper
ft_isalnum	ft_memcpy	ft_strlcat	ft_tolower
ft_isascii	ft_memmove	ft_strchr	
ft_isprint	ft_memchr	ft_strrchr	
	ft_memcmp	ft_strncmp	
	ft_calloc	ft_strnstr	
		ft_strdup	
Partie 2 : Fonctions supplémentaires

Fonctions utilitaires ne faisant pas partie de la libc ou présentes sous une forme différente.

    ft_substr : Extrait une sous-chaîne.

    ft_strjoin : Concatène deux chaînes dans une nouvelle zone mémoire.

    ft_strtrim : Supprime des caractères spécifiques au début et à la fin.

    ft_split : Découpe une chaîne en tableau de chaînes selon un délimiteur.

    ft_itoa : Convertit un entier en chaîne de caractères.

    ft_strmapi / ft_striteri : Applique une fonction sur chaque caractère.

    ft_putchar_fd / ft_putstr_fd / ft_putendl_fd / ft_putnbr_fd : Écrit sur un descripteur de fichier.

Partie Bonus (Listes chaînées)

Structure utilisée :
C

typedef struct s_list
{
    void            *content;
    struct s_list   *next;
} t_list;

Fonctions : ft_lstnew, ft_lstadd_front, ft_lstsize, ft_lstlast, ft_lstadd_back, ft_lstdelone, ft_lstclear, ft_lstiter, ft_lstmap.
🚀 Installation & Utilisation
Compilation

Le projet utilise un Makefile qui compile une bibliothèque statique libft.a.
Bash

# Compiler les fonctions de base
make

# Compiler avec les bonus (listes chaînées)
make bonus

# Nettoyer les fichiers objets (.o)
make clean

# Nettoyer tout (objets + .a)
make fclean

# Recompiler à zéro
make re

Utilisation dans votre projet

Pour utiliser cette bibliothèque dans ton code, inclus le header et compile avec le fichier .a :

    Ajoute le header dans ton fichier .c :
    C

#include "libft.h"

Compile ton projet avec la bibliothèque :
Bash

    cc -Wall -Wextra -Werror main.c -L. -lft

🧪 Tests

Bien que ce dépôt ne contienne pas de testeur, le projet a été validé avec :

    Libft-unit-test

    libft-war-machine

    libftTester

👤 Auteur

    ttiprez - [Github](https://github.com/TiprezTuan)

Projet réalisé dans le cadre du tronc commun de l'école 42 Paris.