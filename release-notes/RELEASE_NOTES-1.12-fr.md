# Octobre 2021 - Version 1.12.0

# C'est corrigé

- La TVA est correctement recalculée dans un certain nombre de cas très particuliers:
    - lorsqu'un groupe de facturation devient une CESSION (la marge est alors aussi adaptée),
    - lorsque l'acheteur d'un véhicule est changé pour un contact exonéré de TVA,
    - lorsqu'une vente de véhicule se fait depuis un dealer file avec un contact exonéré de TVA.
- Après avoir édité ou modifié les prix d'un véhicule, les changements sont visibles lorsqu'on revient sur le catalogue.
- Après avoir modifié un véhicule (une instance ou un dossier), les changements sont visibles lorsqu'on revient sur la liste.
