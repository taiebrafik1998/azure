# azure cloud

## TO DO LIST
### 1 creation d'une vm 



faut se rendre sur azure cloud et s'authentifier
puis cliquer sur ressource apres ça on clique sur machine virtuelle

<img width="929" alt="machinevirtuelcree" src="https://github.com/taiebrafik1998/azure/assets/84631421/a437c639-6b77-40d9-85ed-0e6e94c7be66">

apres avoir cliquer sur machine virtuel on tombe sur cette page ou on peut configurer notre VM (virtual machine) et qu'on a terminer la configuration des different parties on appuie sur le button verifier+ creer 

<img width="960" alt="Capture d'écran 2023-12-22 105111" src="https://github.com/taiebrafik1998/azure/assets/84631421/47cb1142-73d9-4320-b06c-18f6cff78ed0">

et on trouve notre machine virtual qu'on a cree ici ( ainsi que les autre si on le cree)

<img width="914" alt="Capture d'écran 2023-12-21 102148" src="https://github.com/taiebrafik1998/azure/assets/84631421/a9d8abd8-4a61-4d33-b693-71ff9d666f89">

si on appuie sur l'une des vm cree on tombe sur cette interface ou on peut faire certain action sur la machine selectionner tel que la demarrer la supprimer ...etc

<img width="931" alt="Capture d'écran 2023-12-22 110038" src="https://github.com/taiebrafik1998/azure/assets/84631421/57a7d77d-cc02-4b98-a0c5-16333c2f0570">

### 2 cree une alerte 

sachant que tout est payant sur le cloud ça sera inteligent de faire des alerte budgetaire pour qu'on depense pas tous nous credit azure (les gerer inteligement )
et pour parvenir on va aller sur cost management comme le montre l'image suivante

![alertmanagement](https://github.com/taiebrafik1998/azure/assets/84631421/8c1cc5bf-6d17-4f61-93cb-7e46ce4ba288)

apres avoir cliquer sur cost management on vas etre rederiger vers une autre page et on selection budget dans le menu de gauche 

![budget](https://github.com/taiebrafik1998/azure/assets/84631421/5757fc9b-5c96-4e0c-a4bf-3c25cd2ce362)

apres ça on appuis sur add pour cree notre alerte

<img width="928" alt="addbuget" src="https://github.com/taiebrafik1998/azure/assets/84631421/4e95ada0-fe87-4055-80cc-4fe5c75c85d0">

On remplies les champs de cree budget et set l'alert
<img width="932" alt="Capture d'écran 2023-12-22 115242" src="https://github.com/taiebrafik1998/azure/assets/84631421/12ca8669-b839-4ddc-ad98-9aab365d48ef">

<img width="936" alt="Capture d'écran 2023-12-22 115328" src="https://github.com/taiebrafik1998/azure/assets/84631421/9dd2e86a-e3ca-4353-b028-42c23cb3162d">

apres avoir remplie les champ on appuie sur create on attend un petit peux et voila notre alerte budgetaire est creer
<img width="912" alt="Capture d'écran 2023-12-21 103431" src="https://github.com/taiebrafik1998/azure/assets/84631421/7ab7775b-9521-4f3e-8112-96e8a00563f7">



### 3 APP services
dans la barre de recherche on ecrit app service puis on selection app service
sur la page app service on appuie sur le button creer
<img width="928" alt="Capture d'écran 2023-12-22 120750" src="https://github.com/taiebrafik1998/azure/assets/84631421/f40424da-6af5-4db1-a994-3b8859c6a020">
apres avoir cliquer sur create une nouvelle page s'affiche qui nous permettra de configurer notre application 
<img width="918" alt="Capture d'écran 2023-12-21 115150" src="https://github.com/taiebrafik1998/azure/assets/84631421/e3f706c9-f721-43d6-bde3-761b6e54df36">
qu'on a terminer de configurer les differents champ de notre serviceapp on appuie sur create pour cree notre service app
une fois terminer notre ressource est pret au deploiment (pour le pricing planing j'ai utiliser le plan basic b1)
<img width="916" alt="Capture d'écran 2023-12-21 115324" src="https://github.com/taiebrafik1998/azure/assets/84631421/311370b8-5295-4611-a2e7-b2c15ead3d91">
pour deployer une application il nous faut une app de ce fait j'ai telecharger un use case de microsoft ecrit en python pour le lancer comme un microservice

<img width="881" alt="Capture d'écran 2023-12-21 120633" src="https://github.com/taiebrafik1998/azure/assets/84631421/d1e5f1d6-1049-4811-8dcc-74558fb6e91b">
on va cree un fichier zip de l'app qu'on vas deployer
<img width="960" alt="Capture d'écran 2023-12-21 131403" src="https://github.com/taiebrafik1998/azure/assets/84631421/e7e0d3b3-15d1-4ec8-9d49-690fc7a49330">

Une fois que nous disposons d’un fichier ZIP, le fichier peut être chargé sur Azure à l’aide d’Azure CLI ou d’un client HTTP tel que Postman ou cURL.dans notre cas on a optez pour azurecli 

```
# Change les valeurs vers celle utiliser lors de la creation de l'app Service.
RESOURCE_GROUP_NAME='msdocs-python-webapp-quickstart'
APP_SERVICE_NAME='msdocs-python-webapp-quickstart-123'

az webapp deploy --name $APP_SERVICE_NAME --resource-group $RESOURCE_GROUP_NAME --src-path <zip-file-path> #chemin vers zip file creer
```

Accédez à l’application déployée à l’aide de votre navigateur web à l’URL http://<app-name>.azurewebsites.net. Si vous voyez s’afficher une page d’application par défaut, attendez une minute, puis actualisez le navigateur.

<img width="960" alt="Capture d'écran 2023-12-21 140744" src="https://github.com/taiebrafik1998/azure/assets/84631421/e3b094a9-5630-434b-8551-6efcb33fc62e">


<img width="960" alt="Capture d'écran 2023-12-21 141244" src="https://github.com/taiebrafik1998/azure/assets/84631421/8af5079f-9067-4725-b24d-bc473f20aafe">


L’exemple de code Python exécute un conteneur Linux dans App Service avec une image intégrée.

### 4 cls
Set Up Blob Storage
pour ça nous devons d'abord creer a storage account
<img width="930" alt="Capture d'écran 2023-12-22 150443" src="https://github.com/taiebrafik1998/azure/assets/84631421/9026aa35-2885-4946-8a19-32bc06d1bc35">

et on lance le powershell

<img width="934" alt="Capture d'écran 2023-12-22 150949" src="https://github.com/taiebrafik1998/azure/assets/84631421/2ad3292b-e078-4cb9-9736-c638de134009">
voici template de storage account

```
{
    "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {
        "storageAccounts_storageaccountrafik1_name": {
            "defaultValue": "storageaccountrafik1",
            "type": "String"
        }
    },
    "variables": {},
    "resources": [
        {
            "type": "Microsoft.Storage/storageAccounts",
            "apiVersion": "2023-01-01",
            "name": "[parameters('storageAccounts_storageaccountrafik1_name')]",
            "location": "francecentral",
            "sku": {
                "name": "Standard_LRS",
                "tier": "Standard"
            },
            "kind": "StorageV2",
            "properties": {
                "dnsEndpointType": "Standard",
                "defaultToOAuthAuthentication": false,
                "publicNetworkAccess": "Enabled",
                "allowCrossTenantReplication": false,
                "minimumTlsVersion": "TLS1_2",
                "allowBlobPublicAccess": false,
                "allowSharedKeyAccess": true,
                "networkAcls": {
                    "bypass": "AzureServices",
                    "virtualNetworkRules": [],
                    "ipRules": [],
                    "defaultAction": "Allow"
                },
                "supportsHttpsTrafficOnly": true,
                "encryption": {
                    "requireInfrastructureEncryption": false,
                    "services": {
                        "file": {
                            "keyType": "Account",
                            "enabled": true
                        },
                        "blob": {
                            "keyType": "Account",
                            "enabled": true
                        }
                    },
                    "keySource": "Microsoft.Storage"
                },
                "accessTier": "Hot"
            }
        },
        {
            "type": "Microsoft.Storage/storageAccounts/blobServices",
            "apiVersion": "2023-01-01",
            "name": "[concat(parameters('storageAccounts_storageaccountrafik1_name'), '/default')]",
            "dependsOn": [
                "[resourceId('Microsoft.Storage/storageAccounts', parameters('storageAccounts_storageaccountrafik1_name'))]"
            ],
            "sku": {
                "name": "Standard_LRS",
                "tier": "Standard"
            },
            "properties": {
                "cors": {
                    "corsRules": []
                },
                "deleteRetentionPolicy": {
                    "allowPermanentDelete": false,
                    "enabled": true,
                    "days": 7
                },
                "isVersioningEnabled": false,
                "changeFeed": {
                    "enabled": false
                },
                "restorePolicy": {
                    "enabled": false
                },
                "containerDeleteRetentionPolicy": {
                    "enabled": true,
                    "days": 7
                }
            }
        },
        {
            "type": "Microsoft.Storage/storageAccounts/fileServices",
            "apiVersion": "2023-01-01",
            "name": "[concat(parameters('storageAccounts_storageaccountrafik1_name'), '/default')]",
            "dependsOn": [
                "[resourceId('Microsoft.Storage/storageAccounts', parameters('storageAccounts_storageaccountrafik1_name'))]"
            ],
            "sku": {
                "name": "Standard_LRS",
                "tier": "Standard"
            },
            "properties": {
                "protocolSettings": {
                    "smb": {}
                },
                "cors": {
                    "corsRules": []
                },
                "shareDeleteRetentionPolicy": {
                    "enabled": true,
                    "days": 7
                }
            }
        },
        {
            "type": "Microsoft.Storage/storageAccounts/queueServices",
            "apiVersion": "2023-01-01",
            "name": "[concat(parameters('storageAccounts_storageaccountrafik1_name'), '/default')]",
            "dependsOn": [
                "[resourceId('Microsoft.Storage/storageAccounts', parameters('storageAccounts_storageaccountrafik1_name'))]"
            ],
            "properties": {
                "cors": {
                    "corsRules": []
                }
            }
        },
        {
            "type": "Microsoft.Storage/storageAccounts/tableServices",
            "apiVersion": "2023-01-01",
            "name": "[concat(parameters('storageAccounts_storageaccountrafik1_name'), '/default')]",
            "dependsOn": [
                "[resourceId('Microsoft.Storage/storageAccounts', parameters('storageAccounts_storageaccountrafik1_name'))]"
            ],
            "properties": {
                "cors": {
                    "corsRules": []
                }
            }
        }
    ]

```

