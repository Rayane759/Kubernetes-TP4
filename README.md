# Kubernetes-TP4

## Notes globales du TP

Ce TP a été réalisé une première fois lors de la séance de cours du 10 février.

J'avais pris des captures d'écran (présentes dans le dépôt sous le dossier "images/"), mais je n'ai pas crée de repo Git pour ce TP.

J'ai donc recrée ce dépôt en recopiant les fichiers que j'avais en local. 

Par ailleurs, le compte-rendu ci-dessous a également été rédigé, à l'origine, lors de la séance de cours. Seule cette partie "Notes globales du TP" a été rédigée après coup.


## Notes détaillées du TP

Je n'ai pas rencontré de difficulté majeure lors de ce TP. En effet, l'ajout du StatefulSet se situe bien dans la continuité des TP et n'a pas causé de problème majeur en terme de réalisation et de compréhension du StatefulSet.

En revanche, je n'avais pas tout de suite compris que le `volumeClaimTemplates` générait automatiquement un `PersistentVolumeClaim`. Ainsi, au début, j'avais crée un fichier `PVC.yaml` à part pour le StatefulSet, tout en créant en même temps le `volumeClaimTemplates` dans le fichier `postgres-statefulset.yaml`.

En dehors de cette incompréhension technique, le TP s'est globalement bien passé.

Les captures d'écran prises lors du TP se trouvent dans le dossier "images/".


## Deployment vs StatefulSet

Avec un `Deployment` classique, si notre pod est supprimé, alors on perd nos données.

En revanche, avec un `StatefulSet`, on a un stockage persistant (grâce au PVC) qui est attaché au pod. Ainsi, même si notre pod est supprimé, on conserve nos données.