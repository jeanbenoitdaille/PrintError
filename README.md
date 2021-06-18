# PrintError
Erreur dans  déclaration variable 
Le problème qui survient dans le script de départ vient du fait que nous assignons 'range(3)' dans une variable qui est déjà utilisée par Python pour convertir un objet en liste (la fonction list).

Ainsi, quand nous essayons de convertir la liste 'list2', avec la fonction list, nous avons une erreur :

    >>> list = range(3)
    >>> list2 = range(5)
    >>> list(list2)
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: 'range' object is not callable

En écrasant le mot réservé 'list' par 'range(3)', nous écrasons la fonction list et quand nous voulons l'utiliser plus loin dans notre script, Python essaie de convertir notre liste 'list2' avec l'objet 'range' contenu à l'intérieur de la variable 'list' au lieu d'utiliser la fonction list.
