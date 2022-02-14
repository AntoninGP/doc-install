Mise à jour
======

.. note::

  Comme pour tout processus de mise à jour, vous devez sauvegarder certaines données avant de commencer le processus de mise à jour:
   * **sauvegardez votre base de donnée**;
   * sauvegardez votre répertoire `config`, pour votre fichier clé GLPI (`config/glpi.key` ou `config/glpicrypt.key`) qui est généré aléatoirement;
   * sauvegardez votre répertoire `files` , il contient les fichiers générés par les utilisateurs et les plugins, comme les document téléversés;
   * sauvegarder vos répertoires `marketplace` et `plugins`.

Voici les étapes pour mettre à jour GLPI:

* Téléchargez la dernière version de GLPI.
* Assurez vous que le répertoire de destination est vide et désarchivez les fichiers ici.
* Restaurez les répertoires `config`, `files`, `marketplace` et `plugins` précédemment sauvegardés.
* Ouvrez maintenant l'URL de l'instance GLPI dans votre navigateur, ou (recommandé) utilisez `php bin/console db:update` :doc:`command line tools <command-line>`.

.. attention::

   Dès qu'une nouvelle version des fichiers de GLPI est détectée, vous ne pourrez pas utiliser l'application tant que le processus de mise à jour n'est pas terminé.

.. attention::

    Vous ne devez pas essayer de restaurer votre sauvegarde de la basse de donnée sur une base de donnée non vide (Dit, une base de données à été partiellement migrée pour une raison inconnue).

    Spoyez sur que votre base de donnée est vide avant de restaurer votre sauvegarde et essayez de mettre à jout, répétez en cas d'échec.

.. note::

   Les processus de mise à jour désactivera automatiquement vos plugins.
