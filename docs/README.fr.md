# Ansible Terraform Config
Lisez ceci dans d'autres langues: :us:[ English/Anglais](README.md)

---

Ce référentiel contient le code Terraform pour provisionner la VM sur les différents fournisseurs de cloud.

Ce référentiel fait partie du [Démo de déploiement de VM Ansible Terraform Cloud](https://github.com/froberge/ansible_terraform_cloud_vm_deployment)

#### Comment exécuter le provisionnement Terraform localement

###### Prérequis

- CLI Terraform
- :warning: __FORK Le référentiel pour chiffrer vos propres fichiers__

###### Étapes

1.  Entrez la valeur appropriée dans le fichier terraform.tfvars.
```
access_key = ""
secret_key = ""
```


1.  Initialisé le répertoire de travail actuel
            terraform init

2.  Obtenez un aperçu de ce que fera le code
        terraform plan -var-file="terraform.tfvars"

3.  Appliquer les modifications souhaitées
        terraform apply -var-file="terraform.tfvars" -auto-approve

4.  :avertissement : étapes supplémentaires pour détruire ce que vous venez de créer


    terraform destroy -var-file="terraform.tfvars" -auto-approve

* * *

Crypter et décrypter le fichier important dans`Ansible Vault`

-   **Crypter**
        ansible-vault encrypt terraform.tfstate terraform.tfstate.backup terraform.tfvars

-   **Décrypter**
        ansible-vault decrypt terraform.tfstate terraform.tfstate.backup terraform.tfvars

* * *
