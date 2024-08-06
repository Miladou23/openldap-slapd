openldap-slapd
==============

Prévu pour être déployé sur une Debian assez standard, actuellement Debian 12.

Note: sur Debian 12 `ppolicy.schema` n'est plus déployé, les objets ont l'air chargés dynamiquement par le module. Vu qu'on utilise simplement les objets, le schema est ajouté ici.

OpenLDAP slapd géré à l'ancienne avec configuration dans `slapd.conf`. À voir si on passe à slapd.d, ou même la config dans l'annuaire (pas pratique à éditer, mais prise en compte à chaud).

Initialisation
==============

Supprime la configuration slapd.d (par défaut), les données et passe '-u' à slaptest.

`$ ansible-playbook -i hosts -l dev playbook.yml -e 'slapd_reset=true'`
